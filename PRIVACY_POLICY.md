# 🔐 Privacy Policy — 🌥️ Charlene's Weather

Last updated: November 27, 2026

## 💿 Data Collection ✅

Charlene's Weather does not collect, store, or transmit any personal data. The app does not use analytics, crash reporting, or advertising SDKs.

## 📍 Location Data ✅

The app requests location permission for one purpose only: to determine the nearest NOAA/NWS weather station so it can display weather data for your current location.

- Location data is used **locally on your device** and is never sent to any server controlled by the app developer
- The only network requests made are directly to the National Weather Service API (`api.weather.gov`) and radar.weather.gov, which receive your approximate lat/lon coordinates as part of standard weather data requests
- Background location permission is requested solely to keep widget and background weather updates working when the app is not in the foreground
- You can manually search for a city or use a persistent second location instead of GPS

## 🔔 Notifications ✅

The app uses the `POST_NOTIFICATIONS` permission to deliver:
- NWS weather alert notifications (watches, advisories, warnings) — optional, configurable in Settings
- Pet temperature alerts — optional, configurable in Settings
- Freeze alerts — optional, configurable in Settings
- Boot permission reminder — a one-time notification after device restart if location permissions have not been granted

## 🌐 Network Access ✅

The app requires internet access solely to fetch weather data from the National Weather Service and to load radar imagery.

## Third-Party Services

The app communicates with the following services:
- **National Weather Service API** (`api.weather.gov`) — weather data
- **NOAA Radar** (`radar.weather.gov`) — radar imagery
- **NWS Forecast** (`forecast.weather.gov`) — detailed forecast view (user-initiated)
- **NWS Skywarn** (`weather.gov/skywarn`) — spotter program info (user-initiated)
- **Cash App** (`cash.app`) — optional donation link (user-initiated). Included in versions distributed directly by the developer; not included in the Google Play copy

These services have their own privacy policies. The app sends only the minimum data required (coordinates for weather lookup). User-initiated services are only contacted when you tap the corresponding button.

## 💿 Data Storage ✅

The app stores the following locally on your device:
- Your selected or last-known location (city name, lat/lon)
- Theme preference (light/dark)
- Widget theme preference (match app, light, dark)
- Widget display data (current temp, high/low, humidity, wind, rain, forecast tiles)
- Hourly mode preference
- Alert notification preferences (which categories to notify for, 911 outage toggle)
- Pet temperature alert preferences (enabled, sound, threshold levels)
- Freeze alert preferences (enabled, sound)
- Persistent second location setting and coordinates
- Tracked alert and temperature alert IDs (to avoid re-notifying about the same alert)
- Per-station weather cache folders on disk (e.g., `weather_cache/KLIT/`). File timestamps handle expiration — data served from cache when still fresh
- County and zone UGC codes for alert filtering

The app fetches weather data from the National Weather Service when opened (subject to a 5-minute throttle per station to be NWS-friendly) and periodically for the widget. Cached data is served from per-station file cache when still fresh.

No stored data ever leaves your device.

## 📝 Changes

If this policy changes, the updated date at the top will be revised.

## 📨 Contact

If you have questions about this privacy policy or encounter issues with the app, contact the developer on Telegram: **@LittleRockNative**
