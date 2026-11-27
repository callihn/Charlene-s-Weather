<h1><sub><img src="https://codeberg.org/callihn/CharlenesWeather/raw/branch/main/icon.png" height="40" width="40" alt="Charlene's Weather Icon"></sub>&nbsp;<b>Charlene's Weather</b></h1>

*Created by Matthew Callihan in loving memory of his wife Charlene — a devoted wife, California native, Skywarn Weather Spotter and lifelong weather enthusiast.*

Powered by NOAA / National Weather Service data. No third-party weather services. No ads. No tracking.

---

🪄 Features

**Live Conditions** — Temperature, humidity, wind, rain chance, high/low — all from NWS

**Updated Timestamp** — "Updated: [time]" text between the current conditions card and the 7-day forecast, showing when the station data was last fetched. The reporting station's ID (for example KLIT) sits at the right end of that same line, in the app and on the widget's timestamp line

**Weather Backgrounds** — Dynamic backgrounds on the main screen that change based on current conditions: Clear, Few Clouds, Partly Cloudy, Broken Clouds, Overcast, Rain, Thunderstorm, Snow, Fog, Windy, and Severe. Each has day and night variants. 22 backgrounds total. Toggle in Settings. Preview all backgrounds from the Settings page

**7-Day Forecast** — Scrollable day/night tiles with color-coded temperatures. Average high/low shown beneath the title

**Hourly Forecast** — 24-hour breakdown with day labels, time, temp, icon, and short forecast. Tap the forecast title to toggle between 7-day and hourly views

**Live Radar** — Animated NWS radar preview on main screen. Tap for full interactive radar.weather.gov with local station pre-loaded

**GPS Location** — Tap the GPS icon for a one-shot location fetch. Never saves GPS location when GPS mode is OFF.

  **Persist Location setting** (Settings gear):
  - **OFF** (default): App always starts with fresh GPS. The GPS location is not persisted; searched locations work in-session only
  - **ON**: Saved location persists across restarts. GPS runs in background without overwriting it

**Light & Dark Themes** — Warm tan/royal blue light theme or pure black dark theme. Weather backgrounds adapt to the current theme

**Rainbow Title** — Rainbow-colored title text with contrasting outline for readability against any background. Semi-transparent scrim backdrop when weather backgrounds are active

**Skywarn Program** — "Join Skywarn" dialog with official logo, program info, NOAA notice, and link to your local NWS office Skywarn page

**Home Screen Widget** — At-a-glance current conditions + 3-day forecast with split day/night icons. Displays condition-based backgrounds matching the main app (independently toggleable). Widget theme can be set separately: Match App, Dark, or Light. Red alert triangle when NWS alerts are active. Auto-refreshes every 5 minutes, on device unlock, and when you open the app. If an update can't complete, the status line shows why: No Network, No Location, No GPS, or No Fix

**US Station Search** — 2,600+ NWS/FAA official stations — filter by name or ID as you type

**NWS Forecast View** — Full forecast.weather.gov with pinch-to-zoom, desktop mode toggle, and three-dot menu (Open in Browser / Refresh)

**Weather Alert Notifications** — Configurable NWS alert notifications for watches, advisories, warnings, marine, fire weather, statements, and more. Select categories in Settings. Alerts automatically filtered to only those covering your specific county. Warnings and watches ring through with EAS alarm sound by default; advisories and statements post silently. Each category has its own sound toggle if you want to override the defaults. Do Not Disturb bypass link in Settings lets critical alerts sound through even in DND mode

**NWS 911 System Down Alerts** — Standalone option to get notified when 911 service is disrupted in your area, separate from weather alert categories

**Pet Temperature Alerts** — Get notified when temperatures are unsafe for your pet. Alerts at 32F (quick potty breaks only), 68F (chilly — watch for shivering), 75F (limit heavy exercise, seek shade), and 82F (bring inside — heat stress risk). Optional sound and morning forecast alerts

**Freeze Alert** — Separate toggle for freezing temperature notifications at 32F with optional sound

**Rain Alert** — Simple on/off switch in Settings. Fires a silent notification when rain is expected or already occurring nearby, judged from the hourly forecast, the station's own weather report, active NWS alerts, and chance of precipitation. Nothing to tune — fires once per onset and re-arms once the rain clears

**Temperature Colors** — Purple below 33F, Blue 33-67F, Green 68-74F, Orange 75-82F, Red above 82F

**Temperature-Colored Borders** — Current conditions card and forecast tiles have thin borders color-coded to match the temperature

**Rounded Icons** — 12dp rounded corners on all weather icons throughout the app and widget

**Tablet Ready** — Optimized layout for 7"+ tablets

**Pull to Refresh** — Swipe down to refresh everything — GPS, weather, forecast, radar

**Per-Station Cache** — Weather data cached in per-station folders on disk. Forecast, hourly, and observation data served from cache when still fresh. Cache capped at 5MB with automatic cleanup of stale entries

**Loading Indicator** — Centered overlay with app icon, cloud progress indicators, and step-by-step status messages while weather loads. Shows error states with Retry and Close App buttons. Station fallback status updates in real time

**Notification Shade Weather** — Persistent notification showing current temperature (color-coded), rain chance, humidity, wind, location name, and last update time with station ID at a glance in the notification shade

---

📚 How to Use

**Refresh weather** — Weather data is refreshed from the National Weather Service every 5 minutes (the NWS API policy limit), so it's always as fresh as possible. Swipe down to refresh weather for the current location, or tap the GPS icon to re-locate and load that location's weather

**Open menu** — Tap the menu icon for search, theme toggle, what's new, read me, Skywarn info, About, Support. Gear icon opens Settings

**Current conditions** — Tap the weather icon to open the detailed NWS forecast page

**Toggle forecast mode** — Tap "7-Day Forecast" title to switch between 7-day and hourly views

**Radar** — Tap radar preview for full interactive radar. Menu lets you toggle local/national

**Search** — Menu > Search Location — type any US station name or ID

**Widget** — Add to home screen with condition-based backgrounds and red alert triangle when warnings active. Tap to open the app. Auto-updates every 5 minutes

**Settings** — Tap the gear icon in the menu to configure alert notifications, pet temperature alerts, persistent location, background location, and more

---

🌎 NWS API Compliance

Identity — All requests include "Charlene's Weather" User-Agent

Throttle — Minimum 5-minute wait between fetches for the same station; bypassed on station change. Per-station file cache handles data freshness with file timestamps

Reliability — Automatic retries with smart timing ensure data loads even on slow connections

GPS fresh fix — Each widget cycle requests a fresh high-accuracy GPS fix. No cached or stale location is ever reused

---

💽 Data Source

National Weather Service / NOAA / FAA — api.weather.gov

Observations come from the nearest official weather stations reported by the National Weather Service. A station is only used when it reports a current-conditions icon, a temperature, and at least two of humidity, wind speed, and chance of precipitation — so no half-empty cards. If the closest station is one reading short (many report a wind speed but no humidity), the app asks forecast.weather.gov to complete it, the same way it already completes a missing icon. If the closest station still can't be completed, the app automatically tries nearby stations for better data.

No third-party weather APIs, no ads, no analytics, no data collection.

📦 Download:

<a href="https://apkpure.com/charlene-s-weather/com.matts.weather"><img src="https://codeberg.org/callihn/CharlenesWeather/raw/branch/main/apkpure_button.png" height="50" alt="Charlene's Weather Download"></a>
