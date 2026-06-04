# 🌤️ Charlene's Weather App

> *Created by Matthew Callihan in loving memory of his wife Charlene — a devoted wife, California native, Skywarn Weather Spotter, and lifelong weather enthusiast.*

Powered by NOAA/NWS data (US Only), Charlene's Weather delivers accurate, hyperlocal weather information with a clean, intuitive interface.

---

### 📥 Download the Latest Version
Because this app is developed independently and distributed as an APK outside of the Google Play Store, the installation file is hosted right here on the project's release page:

* 🚀 **Get the App:** [Go to the Latest Release Page](https://github.com/callihn/Charlene-s-Weather/releases/latest)

**To Install:** Click the release link above (or click **Releases** on the right side of this page if you are on a desktop browser). Scroll down to the **Assets** section at the bottom of that release page, tap the `.apk` file to download it, and select "Install Anyway" if prompted by your Android device.

---

## 🌟 Features

- **Pull-to-Refresh** — Swipe down on the main screen to refresh GPS location, weather data, forecast, and radar. Horizontal scroll of the 7-day forecast won't accidentally trigger a refresh.
- **NWS API Compliance** — All API requests to `api.weather.gov` include a proper User-Agent identity header. A built-in 5-minute throttle (respecting server `Cache-Control` hints) prevents excessive requests. The throttle is bypassed automatically when your location changes significantly, ensuring fresh data when you move.
- **Live Weather Data** — Current conditions with temperature, humidity, wind speed, and chance of rain, all sourced directly from the National Weather Service.
- **7-Day Forecast** — Scroll horizontally through daily forecasts with day/night icons, high/low temperatures, and color-coded temperature displays.
- **Interactive Radar** — Animated NWS radar preview on the main screen. Tap to open the full live `radar.weather.gov` site with your local station pre-loaded. Use the site's built-in controls for zoom, pan, and product switching (reflectivity, velocity, precipitation, etc.).
- **GPS Location** — Automatically detects your location and resolves the nearest city name. Also supports manual city search.
- **Light & Dark Themes** — Toggle between a warm tan/royal blue light theme and a pure black dark theme.
- **Home Screen Widget** — At-a-glance weather with current conditions and a 3-day forecast. Weather data refreshes when the app is opened and periodically in the background (every 15 minutes via `WorkManager`).
- **Tablet Optimized** — Automatic tablet layout with larger text, icons, and spacious design for 7"+ devices.
- **Amazon App Store** — Fire tablet compatible.
- **US Station Search** — Find any US ASOS weather station with live filtering as you type, powered by the built-in stations database for instant offline results.
- **Temperature Color Coding** 
  * 🟪 **Purple:** Below 33°F
  * 🟦 **Blue:** 33–67°F
  * 🟩 **Green:** 68–74°F
  * 🟧 **Orange:** 75–82°F
  * 🟥 **Red:** Above 82°F

---

## 📱 How to Use

- **Refresh weather** — Weather data fetches from the National Weather Service each time the app opens. Swipe down on the main screen or tap the GPS icon to manually refresh your location and weather data. Refreshes are limited to once every 5 minutes unless your location changes.
- **Open the menu** — Tap the three-dot menu icon (`⋮`) to search locations, toggle themes, view the about page, or donate.
- **Widget** — Add the Charlene's Weather widget to your home screen for at-a-glance weather. Tap it to open the app and trigger a fresh data fetch.
- **Current conditions** — Tap the current weather icon to open the detailed NWS forecast page for your location.
- **Radar** — The radar preview on the main screen automatically shows your local NWS radar. Tap the preview to open the full live radar site. The menu lets you toggle between local and national views.
- **Forecast** — Scroll horizontally through the 7-day forecast tiles with day/night details.
- **Search** — Use the search option in the menu to find any US weather station by city name or station ID with real-time, live-filtering results.

---

## 🛠️ Technical Details & Permissions

To provide accurate data and home screen updates, the app requires the following standard Android permissions:

| Permission | Purpose |
| :--- | :--- |
| `INTERNET` | Required to securely fetch live weather maps and forecasts directly from NOAA/NWS servers. |
| `ACCESS_FINE_LOCATION` | Allows the app to pinpoint your exact location for precise, hyperlocal neighborhood weather. |
| `ACCESS_COARSE_LOCATION` | Used as a baseline fallback to determine your general city/region for regional weather reports. |

---

## 📸 Screenshots

<details>
<summary>📐 Click here to expand app screenshots</summary>
<br />

<img width="1080" height="2400" alt="Screenshot_20260531-192456_Charlene&#39;s Weather" src="https://github.com/user-attachments/assets/514be1cf-1ee0-4416-885f-12e6f677cfef" />
<img width="1080" height="2400" alt="Screenshot_20260531-192507_Charlene&#39;s Weather" src="https://github.com/user-attachments/assets/f06440f9-3902-4eed-bb84-c3fce4937d4d" />
<img width="1080" height="2400" alt="Screenshot_20260531-192522_Charlene&#39;s Weather" src="https://github.com/user-attachments/assets/be60aab0-8c0f-4a2d-9571-4d2ac63272dc" />
<img width="1080" height="2400" alt="Screenshot_20260531-192551_Charlene&#39;s Weather" src="https://github.com/user-attachments/assets/44ad41ac-7bc8-4da2-b833-b8b7b0a060c7" />
<img width="1080" height="2400" alt="Screenshot_20260531-192605_Charlene&#39;s Weather" src="https://github.com/user-attachments/assets/48a662e2-14f3-4515-9ae1-3b7b997f355d" />
<img width="1080" height="2400" alt="Screenshot_20260531-192618_Charlene&#39;s Weather" src="https://github.com/user-attachments/assets/37bbed6a-047c-44fb-a084-5d4826055f49" />
<img width="1080" height="2400" alt="Screenshot_20260531-192734_Charlene&#39;s Weather" src="https://github.com/user-attachments/assets/7669414e-28e2-4c97-9564-4fd0f3d1809f" />
<img width="1080" height="2400" alt="Screenshot_20260531-192747_Charlene&#39;s Weather" src="https://github.com/user-attachments/assets/1ad07ffb-7829-4f44-821b-0a1370526067" />
<img width="1080" height="2400" alt="Screenshot_20260531-192820_Charlene&#39;s Weather" src="https://github.com/user-attachments/assets/891c7bb9-58e3-442e-a9ab-2c0378638315" />
<img width="1080" height="2400" alt="Screenshot_20260531-192950_Charlene&#39;s Weather" src="https://github.com/user-attachments/assets/ec194b18-4303-47f8-b334-0e2c2cc65742" />
<img width="1080" height="2400" alt="Screenshot_20260531-205521_Nova Launcher" src="https://github.com/user-attachments/assets/3798f64e-4218-4e1a-af16-c46e90f6a083" />

</details>
