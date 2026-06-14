# 🔐 Privacy Policy — 🌥️ Charlene's Weather

Last updated: June 14, 2026

## 💿 Data Collection ✅

🌥️ Charlene's Weather does not collect, store, or transmit any personal data. The app does not use analytics, crash reporting, or advertising SDKs.

## 📍 Location Data ✅

The app requests location permission (ACCESS_FINE_LOCATION and ACCESS_COARSE_LOCATION) for one purpose only: to determine the nearest NOAA/NWS weather station so it can display weather data for your current location.

- Location data is used **locally on your device** and is never sent to any server controlled by the app developer
- The only network requests made are directly to the National Weather Service API (`api.weather.gov`) and radar.weather.gov, which receive your approximate lat/lon coordinates as part of standard weather data requests
- You can manually search for a city instead of using GPS location

## 🌐 Network Access ✅

The app requires internet access solely to fetch weather data from the National Weather Service and to load radar imagery.

## Third-Party Services

The app communicates with the following services:
- **National Weather Service API** (`api.weather.gov`) — weather data
- **NOAA Radar** (`radar.weather.gov`) — radar imagery
- **NWS Forecast** (`forecast.weather.gov`) — detailed forecast view (user-initiated)
- **NWS Skywarn** (`weather.gov/skywarn`) — spotter program info (user-initiated)
- **Cash App** (`cash.app`) — donation link (user-initiated)

These services have their own privacy policies. The app sends only the minimum data required (coordinates for weather lookup). User-initiated services are only contacted when you tap the corresponding button.

## 💿 Data Storage ✅

The app stores the following locally on your device:
- Your selected or last-known location (city name, lat/lon)
- Theme preference (light/dark)
- Widget display data (current temp, high/low, humidity, wind, rain, forecast tiles)
- Alert notification preferences (which categories to notify for, 911 outage toggle)
- Tracked alert IDs (to avoid re-notifying about the same alert)
- Fetch throttle timestamps (to respect NWS caching limits)
- Cached weather data (current conditions, forecast, observation) so the app and widget have something to display immediately while fresh data loads
- Cached weather icons for the app and widget

The app fetches weather data from the National Weather Service when opened (subject to a short cache to be NWS-friendly) and periodically for the widget. Cached data is used only to fill in while loading and is overwritten each time fresh data arrives.

No stored data ever leaves your device.

## 📝 Changes

If this policy changes, the updated date at the top will be revised.

## 📨 Contact

If you have questions about this privacy policy, contact the developer via the app's "Donate" or "About" section.
