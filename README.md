# SmartCane

This repository contains an accessible, interactive SmartCane IoT simulation implemented as a single-page HTML demo.

Features
- Interactive simulation area showing a person and obstacles
- Adjustable sensor range (slider)
- Audio cues via SpeechSynthesis
- Vibration (navigator.vibrate) if supported by the device
- Keyboard controls and visible/high-contrast UI for low-vision users
- ARIA live regions and labels for screen-reader users

Quick start
1. Open `index.html` in your browser (double-click or use a local web server).
2. Use the controls on the right or keyboard to interact.

Keyboard Shortcuts
- Arrow Up: Move forward
- Space: Add an obstacle at a random position
- S: Send an SOS signal
- R: Reset the simulation

Accessibility Notes
- The demo uses `aria-live` regions and `role="status"` to announce events to screen readers.
- Audio announcements use the browser's SpeechSynthesis API; disable audio using the toggle if undesired.
- Vibration support requires a device with the Vibration API (typically mobile).

Map & GPS
- The demo includes a small OpenStreetMap view powered by Leaflet showing real-world streets.
- Click the small map to add an obstacle at that real-world location; a draggable marker will be added and will synchronize to the simulation area.
- Clicking on the simulation area also adds an obstacle — the demo keeps map and sim coordinates in sync when possible.
- If you prefer Google Maps instead of Leaflet/OSM, you can replace the map block in `index.html` with the Google Maps JavaScript API — that requires obtaining an API key and enabling billing for some Google accounts. The demo uses Leaflet/OpenStreetMap to avoid requiring an API key.

Development
- The demo is a single file: `index.html`. Edit it to tweak simulation logic, add obstacles, or localize the language.

License
This demo is provided for educational purposes.
