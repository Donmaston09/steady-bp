# Steady: BP Companion

A free blood pressure checker and diary that works offline. It explains readings in plain language, based on published clinical guidelines.

**Created by Anthony Onoja, PhD**
School of Health Sciences, University of Surrey, UK
Contact: donmaston09@gmail.com

---

## What it does

- **Explains each reading in plain language.** Results show as a traffic light (Low, Normal, A little high, High, Too high, Dangerously high) with clear next steps. A "Read this aloud" button helps people who find reading hard.
- **Emergency safety net.** Readings of 180/120 or higher, together with symptoms such as chest pain, weakness, or trouble speaking or seeing, bring up an emergency alert with a call button: 112 in Nigeria, 999 in the UK.
- **7-day home check** using the NICE home-monitoring method: morning and evening readings for 7 days, with day 1 left out. This gives the average that clinicians use.
- **Trend chart and history**, with averages, highest and lowest readings, and heart rate.
- **Reminders** for blood pressure checks, moving more and medicines. Users are also guided to set phone alarms, which work offline when the app is closed.
- **Stress and activity tools**: a calm-breathing guide, a wall-sit or hand-squeeze timer, a walk timer and an activity log.
- **Share with a health worker** by WhatsApp, text message, copied text or a CSV file for spreadsheets.
- **Backup and restore**, because all data stays on the user's phone.
- **Settings by country**: Nigeria, the UK, or another country. This sets the emergency number, the wording of advice and the default guideline.
- **Accessibility**: large touch targets, three text sizes, light and dark themes, and system fonts.

## Built for low-connectivity, low-power settings

- **Installable app (PWA).** After one visit with internet, it installs to the home screen and runs with no data or Wi-Fi.
- **Small download.** Everything is in one small HTML file plus icons, with no external fonts, libraries or trackers, so it suits low-cost Android phones and expensive mobile data.
- **Light on battery.** There is no background processing, and dark mode saves power on OLED screens.
- **Private by design.** Nothing is sent to a server. Data is stored only on the device.

## Guidelines and evidence

| Guideline | Used for |
|---|---|
| [2020 ISH Global Hypertension Practice Guidelines](https://doi.org/10.1161/HYPERTENSIONAHA.120.15026) | Default for Nigeria and other countries (written for low- and high-resource settings) |
| [NICE NG136](https://www.nice.org.uk/guidance/ng136) | UK default; 7-day home monitoring method |
| [2024 ESC Guidelines](https://doi.org/10.1093/eurheartj/ehae178) | Optional |
| [2025 AHA/ACC Guideline](https://doi.org/10.1161/HYP.0000000000000249) | Optional |

Lifestyle advice is backed by: Edwards et al., *Br J Sports Med* 2023 (exercise, 270 RCTs); Appel et al., *NEJM* 1997 (DASH diet); He et al., *BMJ* 2013 (salt); Neter et al., *Hypertension* 2003 (weight); Roerecke et al., *Lancet Public Health* 2017 (alcohol); and WHO salt guidance.

## Running and hosting

There's no build step. Serve the folder from any static host over HTTPS. Offline mode needs HTTPS, which GitHub Pages provides.

**GitHub Pages:** in the repository, go to Settings → Pages, choose "Deploy from a branch", then select `main` and `/ (root)`.

**Local test:** `python3 -m http.server 8000` and open http://localhost:8000

After changing `index.html`, increase `CACHE` in `sw.js` (for example `steady-v3`) so installed copies update.

## Disclaimer

Steady gives general health information based on published guidelines. It doesn't diagnose, it isn't a certified medical device, and it doesn't replace advice from a doctor, nurse, pharmacist or community health worker. It isn't designed for pregnancy or children. In an emergency, call your local emergency number (112 in Nigeria, 999 in the UK).
