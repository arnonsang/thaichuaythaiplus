# ไทยช่วยไทยพลัส: ตัวช่วยคำนวณสิทธิ (Helper)

A single-page, offline-first helper for the Thai government **ไทยช่วยไทยพลัส (60/40)**
co-payment subsidy (1 Jun – 30 Sep 2569 / 2026). Enter a purchase amount, see how
much the government pays vs. how much you pay, record it, and track your remaining
daily / monthly / campaign subsidy. All data stays on your device (IndexedDB).

> เครื่องมือช่วยคำนวณอย่างไม่เป็นทางการ: ยอดสิทธิจริงให้ยึดตามแอปเป๋าตัง

## Rules implemented

| Cap | Value |
|---|---|
| Government share | **60%** of each purchase |
| Gov per day | **฿200** (spend ฿333.33 → gov ฿200 + you ฿133.33) |
| Gov per month | **฿1,000** (no rollover) |
| Gov whole campaign | **฿4,000** (Jun–Sep 2569) |

`govPays = min(0.60 × amount, ฿200−todayGov, ฿1,000−monthGov, ฿4,000−totalGov)`
Overspend beyond the daily ฿200 gov cap is 100% on you and does **not** consume
the monthly budget. Daily resets each day, monthly resets each new month
(derived automatically from saved records).

## Run

**Just open it**: double-click `index.html`. It works fully offline from disk;
all data is saved locally and persists across reloads.

## Install as an app (optional PWA)

"Add to home screen" requires the file to be **served over http(s)** with the
companion `sw.js` (browsers won't install from `file://`). Easiest local host:

```bash
python -m http.server 8080
# open http://localhost:8080  →  browser shows "Install" / use the 📲 button
```

Or deploy the folder to any static host (GitHub Pages, Netlify, Vercel) for a
real installable, offline PWA.

## Files

- `index.html`: the entire app (HTML + CSS + JS, no dependencies).
- `sw.js`: tiny cache-first service worker, used only when hosted.
- `README.md`: this file.

## Backup

Use **ส่งออก (JSON)** to download your records, and **นำเข้า** to restore them on
a new device/browser (replace or merge). Recommended before clearing browser data.
