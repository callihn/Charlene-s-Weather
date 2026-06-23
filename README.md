# 🌤️ Charlene's Weather

> *Created by Matthew Callihan in loving memory of his wife Charlene — a devoted wife, California native, Skywarn Weather Spotter, and lifelong weather enthusiast.*

Powered by NOAA/NWS data (US Only), Charlene's Weather delivers accurate, hyperlocal weather information with a clean, intuitive interface.

---

### 📥 Download the Latest Version
Because this app is developed independently and distributed as an APK outside of the Google Play Store, the installation file is hosted right here on the project's release page:

[![Get the App](https://img.shields.io/github/v/release/callihn/Charlene-s-Weather?style=for-the-badge&label=%F0%9F%9A%80%20Get%20the%20App&color=2ea44f)](https://github.com/callihn/Charlene-s-Weather/releases/latest)

**To Install:** Click the release link above (or click **Releases** on the right side of this page if you are on a desktop browser). Scroll down to the **Assets** section at the bottom of that release page, tap the `.apk` file to download it, and select "Install Anyway" if prompted by your Android device.

---

# 📸 Screenshots

<details>
<summary>Click here to expand app screenshots</summary>

<!-- Row 1: Core App Dashboards (Light & Dark Main Views, Hourly Toggle) -->
<img width="32%" alt="Main Dashboard - Light Theme" src="https://github.com/user-attachments/assets/21ef48f1-7745-4760-9be6-1551c1f38143" /><img width="32%" alt="Main Dashboard - Dark Theme" src="https://github.com/user-attachments/assets/77c2c875-edcd-421c-98de-425091a12248" /><img width="32%" alt="Hourly Forecast Mode Toggle" src="https://github.com/user-attachments/assets/83d563de-565f-4623-a936-09584f05993c" />

<!-- Row 2: Location Search & Custom Views (Station Search, NWS Web View, Skywarn Info) -->
<img width="32%" alt="US Weather Station Search" src="https://github.com/user-attachments/assets/fba326fd-becd-4947-a078-33456b23eb1c" /><img width="32%" alt="NWS Forecast Web View" src="https://github.com/user-attachments/assets/c4e613e0-4d3e-43aa-bff6-0e29f544cc64" /><img width="32%" alt="Skywarn Program Info Dialog" src="https://github.com/user-attachments/assets/3c017095-9cba-46e6-aa35-159f3a526443" />

<!-- Row 3: Widget & System Integration (Home Screen Widget, Notification Bar EAS Tone, Alert Toggles) -->
<img width="32%" alt="Nova Launcher Home Screen Widget" src="https://github.com/user-attachments/assets/694a581e-4c6f-469c-bab2-20f29d9fb4bd" /><img width="32%" alt="System UI Weather Alert Notification" src="https://github.com/user-attachments/assets/06a2c6bb-7ad9-410f-8fad-e58f8f14e0ba" /><img width="32%" alt="NWS Alert Category Configuration" src="https://github.com/user-attachments/assets/2981cb36-d12d-425f-98c8-41e6058e1a9d" />

<!-- Row 4: Core App Settings (General Configuration, Location Options, Info/Credits) -->
<img width="32%" alt="General App Settings" src="https://github.com/user-attachments/assets/481cea41-3ce0-4320-851e-0975676c2a1c" /><img width="32%" alt="Advanced Location and Refresh Paths" src="https://github.com/user-attachments/assets/f187daa4-c325-429a-8275-3f0227ad5c06" /><img width="32%" alt="App Build Version Information" src="https://github.com/user-attachments/assets/c81b65df-be83-4674-9205-01e18a01025c" />

<!-- Row 5: Additional Views & Overlays -->
<img width="32%" alt="Detailed System Permissions Info" src="https://github.com/user-attachments/assets/f15ead15-e266-4bbc-9ed4-2b3e561d29a5" /><img width="32%" alt="NWS Station Properties" src="https://github.com/user-attachments/assets/0b4065f4-55fb-40fb-b5fa-d15e860f0673" />

</details>

---

## 🪄 Features

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

## 📚 How to Use

- **Refresh weather** — Weather data fetches from the National Weather Service each time the app opens. Swipe down on the main screen or tap the GPS icon to manually refresh your location and weather data. Refreshes are limited to once every 5 minutes unless your location changes.
- **Open the menu** — Tap the three-dot menu icon (`⋮`) to search locations, toggle themes, view the about page, or donate.
- **Widget** — Add the Charlene's Weather widget to your home screen for at-a-glance weather. Tap it to open the app and trigger a fresh data fetch.
- **Current conditions** — Tap the current weather icon to open the detailed NWS forecast page for your location.
- **Radar** — The radar preview on the main screen automatically shows your local NWS radar. Tap the preview to open the full live radar site. The menu lets you toggle between local and national views.
- **Forecast** — Scroll horizontally through the 7-day forecast tiles with day/night details.
- **Search** — Use the search option in the menu to find any US weather station by city name or station ID with real-time, live-filtering results.

---

## 🔐 Permissions

To provide accurate data and home screen updates, the app requires the following standard Android permissions:

| Permission | Purpose |
| :--- | :--- |
| `INTERNET` | Required to securely fetch live weather maps and forecasts directly from NOAA/NWS servers. |
| `ACCESS_FINE_LOCATION` | Allows the app to pinpoint your exact location for precise, hyperlocal neighborhood weather. |
| `ACCESS_COARSE_LOCATION` | Used as a baseline fallback to determine your general city/region for regional weather reports. |
