# Cryptoville-Home-Asssistant-Smartphone-Card
A curated collection of mobile-friendly Home Assistant cards optimised for smartphones.
Includes UI-ready YAML snippets for TRVs, climate views, gauges, sensors,and more
![IMG_5269](https://github.com/user-attachments/assets/b57fa4b0-9bc8-4c46-80e8-df9309a57f3d)

📦
1. Temperature Swing – Multi-TRV Gauge Set
A compact, expandable mobile card showing °C/hr heat-gain and heat-loss for multiple TRVs.
Features:
Animated circular LED gauge
Colour severity mapping
Shadow glow based on temperature slope
Optional TRV control popups (Browser Mod)
Fully responsive for smartphones
Files:
cards/temperature_swing_trv_set.yaml
packages/dropdown_mod.yaml
🧩 Requirements
Available through HACS:
bubble-card
button-card
custom-gauge-card
Optional (for popups):
browser_mod
versatile-thermostat-ui-card
⚙️ Installation
1. Enable Home Assistant Packages
In configuration.yaml:
homeassistant:
  packages: !include_dir_named packages
Create a folder in your config:
/config/packages/
Add the helper file:
packages/dropdown_mod.yaml
Restart Home Assistant.
2. Import the Card
In your dashboard:
Edit Dashboard → Add Card → Manual Card
Paste the content from:
cards/temperature_swing_trv_set.yaml
Replace the example entities with your own:
sensor.vt_livingroom_temperature_slope
sensor.vt_kitchen_temperature_slope
sensor.vt_hallway_temperature_slope
sensor.vt_bedroom_temperature_slope
sensor.vt_kids_temperature_slope
sensor.vt_landing_temperature_slope
And matching climate entitles.
That’s it — the dropdown header will toggle the full TRV gauge grid.
📝 Notes
You can safely delete unused booleans from dropdown_mod.yaml
The gauges are optimised for mobile dashboards
Fits perfectly into minimalist or neon-style themes
