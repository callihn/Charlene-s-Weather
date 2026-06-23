# 📋 Changelog

---

## 🚀 2.3.0 — 2026-06-23

### ✨ Added
- **🕐 Hourly forecast** — Tap the "7-Day Forecast" title to toggle between 7-day and 24-hour hourly views. Automatically scrolls to and centers the tile matching the current hour. Each tile shows a 3-letter day abbreviation rotated on the left edge
- **📟 Tablet-optimized forecast tiles** — Separate `layout-sw600dp` variants for 7-day and hourly forecast tiles at 150dp x 210dp for better proportions on larger screens
- **⚡ Faster weather display** — Current conditions, forecast, and radar all load in parallel and display as soon as each piece arrives. No more waiting for everything to finish before anything shows up
- **🆘 Skywarn Program Info** — "Join Skywarn" menu option with official logo, program description, NOAA attribution, and link to your local NWS office Skywarn page
- **🌙 Split widget icons** — Widget forecast tiles show separate day and night icons side by side
- **🌡️ Temperature-colored borders** — Current conditions card and forecast tiles have borders color-coded to match the temperature (purple <33F, blue 33-67F, green 68-74F, orange 75-82F, red >82F)
- **🔄 Pull-to-refresh** — Swipe down anywhere to refresh GPS, weather, forecast, and radar all at once
- **📍 Widget GPS** — Widget fetches its own GPS location on each 5-minute refresh cycle, showing weather for where you actually are
- **📱 Three-dot menu on WebViews** — Both Skywarn and NWS Forecast pages have menu options for "Open in Browser" and "Refresh"
- **🖼️ Rounded icons** — 12dp rounded corners on all weather icons throughout the app and widget
- **📇 Current conditions card** — Icon, temperature, high/low, humidity, wind, and rain chance in a rounded card with temperature-colored border
- **🔓 Widget on device unlock** — Widget refreshes weather data automatically when the device is unlocked
- **🔀 MapClick fallback** — Falls back to forecast.weather.gov data when NWS API returns incomplete observation data, filling in missing fields while preserving existing API data
- **🌙 Dark splash screen** — Launch background changed to dark, eliminating the white/tan flash when starting the app in dark mode
- **🔔 Weather alert notifications** — Configurable NWS alert notifications for watches, advisories, statements, and more. Select categories in Settings. Uses system alarm sound with custom EAS tone support
- **📞 911 System down alerts (NWS)** — Standalone option to get notified when 911 service is disrupted in your area, separate from weather alert categories
- **📡 Intelligent observation fallback** — If the closest observation station returns incomplete data, the app automatically tries the nearest major ASOS or ASOS-HFM station. Both API observations fire in parallel with MapClick at the fallback station's location as a last resort
- **📅 First forecast tile** — Shows "Today" or "Tonight" based on NWS `isDaytime` flag
- **📊 Forecast averages** — Average high/low shown beneath the 7-Day Forecast title
- **🔘 Radar preview badge** — Added "Tap ↓" hint on radar preview
- **🎨 Radar rounded corners** — 12dp rounded corners on radar preview
- **🔲 Widget icon backgrounds** — Dark rounded backgrounds behind widget icons for better contrast
- **🧩 Unified location provider** — Single code path for all location requests across app and widget
- **🔀 Station selection** — Primary station is the closest overall; secondary station is the closest ASOS-HFM or ASOS airport for maximum data reliability
- **⏳ 6-minute throttle** — Minimum interval between fetches for the same location to be friendly to NWS servers
- **🌐 Desktop viewport on Skywarn** — Skywarn pages load in mobile viewport so weather.gov shows its native "Desktop View" button

### 🔧 Fixed
- **📍 Location on newer Android** — Replaced deprecated `LocationManager.requestSingleUpdate()` with Google Play Services `FusedLocationProviderClient.getCurrentLocation()` using `CurrentLocationRequest` + `Priority.PRIORITY_BALANCED_POWER_ACCURACY`
- **🖼️ Current weather icon** — Now always comes from real-time observations, never from forecast data
- **📱 Android 16 compatibility** — Updated deprecated API checks
- **⏲️ Widget refresh race** — Fixed race condition that could miss the 5-minute mark for widget refresh
- **📭 Forecast placeholder** — Shows `--°` instead of empty space when data is unavailable
- **🎯 GPS race condition** — Fixed duplicate fetches when GPS fix arrives milliseconds after last-known location path
- **⬇️ Pull-to-refresh** — No longer switches to GPS location; stays on the currently displayed location
- **🚫 Throttle bypass on location change** — Location changes properly bypass the minimum fetch interval

### 🎨 Changed
- **📈 Version** — 1.5.0 → **2.3.0** (code 8 → 16)

### 🗑 Removed
- **🗑️ Deprecated location code** — All `requestSingleUpdate`, `LocationListener`, and `NETWORK_PROVIDER` code removed
- **🗑️ WorkManager dependency** — Unused library removed
- **🗑️ Unused permissions** — `SCHEDULE_EXACT_ALARM` and `USE_EXACT_ALARM` removed from manifest

---

## 🚀 1.5.0 — 2026-06-02

### ✨ Added
- **🔄 MapClick fallback** — Falls back to `forecast.weather.gov/MapClick.php?FcstType=json` for icons, temp, humidity, and wind when NWS observation API returns incomplete data
- **🔀 Smart merge** — Only missing fields are filled from MapClick; existing API data preserved

### 🎨 Changed
- METAR text fallback replaced with structured MapClick JSON (includes proper NWS weather icons)
- **Version** 1.4.0 → **1.5.0** (code 7 → 8)

---

## 🚀 1.4.0 — 2026-06-01

### 🎨 Changed
- Widget refresh interval 15 min → 5 min
- Auto-refresh on app resume if data is stale
- Widget syncs on GPS update
- **Version** 1.3.0 → **1.4.0** (code 6 → 7)

---

## 🚀 1.3.0 — 2026-06-01

### ✨ Added
- **📟 Tablet layout** — Optimized for 7"+ tablets
- **🔥 Amazon App Store** — Fire Tablet compatible

### 🎨 Changed
- Background update mechanism overhauled — AlarmManager (broken on Android 12+) → WorkManager (later replaced by persistent foreground service in 2.3.0)
- **Version** 1.2.2 → **1.3.0** (code 5 → 6)

---

## 🚀 1.2.2 — 2026-05-31

### ✨ Added
- **🏙️ Local station search** — 2,661 US ASOS stations in offline database
- **📅 First tile** — Shows "Today" or "Tonight" based on NWS `isDaytime` flag
- **📊 Forecast averages** — Average high/low beneath 7-Day Forecast title

### 🔧 Fixed
- **🔄 Icon cross-contamination** — Cache keyed by URL hash (not positional), preventing stale icons across location changes
- **🖼️ Observation icon incorrectly used forecast icon** — When observation station returned `"icon": null`, the app mistakenly fell back to forecast data instead of using only real-time observation data
- **🏷️ LoadImageTask tag check** — Discards stale download results when ImageView recycled to a different URL
- **⬇️ Pull-to-refresh** — Doesn't switch to GPS location; stays on current displayed location

### 🎨 Changed
- User-agent centralized in `AppConstants.USER_AGENT`
- Rainbow title bars on Radar and NWS Forecast activities
- Version in title bar via `BuildConfig.VERSION_NAME`
- **Version** 1.2.1 → **1.2.2** (code 4 → 5)

---

## 🚀 1.1 — 2026-05-30

### ✨ Added
- **🔄 Pull-to-refresh** — Swipe down on main screen to refresh weather
- **📍 GPS re-acquisition** — Refresh also triggers fresh GPS fix
- **⏱️ Centralized throttle** — 5-minute minimum cache with location-change bypass
- **👆 Horizontal scroll fix** — Forecast `HorizontalScrollView` won't trigger pull-to-refresh

### 🎨 Changed
- User-Agent updated to NWS-recommended format
- Widget timestamp reflects last successful API fetch, not last render
- **Version** 1.0 → **1.1** (code 1 → 2)

---

## 🚀 1.0 — 2026-05-28

### ✨ Added
- **🎉 Initial release** — Live weather, 7-day forecast, radar, widget, GPS location, search, light/dark themes, donate

### 🎨 Changed
- RadarActivity rewritten with NWS bookmark API for high-res local radar with pinch-to-zoom
- Donate simplified to direct Cash App URL
- `compileSdk` / `targetSdk` → 36 (Android 16)
- Edge-to-edge on all activities (API 35+)

### 🗑 Removed
- **🗑️ WorkManager dependency** — Unused library removed from build.gradle
- **🗑️ SCHEDULE_EXACT_ALARM & USE_EXACT_ALARM permissions** — Removed from manifest; widget uses `setWindow()` without special permissions
- Stale docs: `VERIFICATION_INDEX.md`, `VERIFICATION_REPORT.md`, `VERIFICATION_SUMMARY.md`, `CODE_REFACTORING.md`
