[View on GitHub](https://aimanbintemaqsood999-cyber.github.io/WebGIS-Navigation-Dashboard/)
# WebGIS Parks Navigation & Routing Dashboard (Rawalpindi)

An interactive web map that shows major parks in Rawalpindi and gives driving directions to any of them from the user's current location.

**Live demo:** https://aimanbintemaqsood999-cyber.github.io/WebGIS-Navigation-Dashboard/

## Features

- Interactive map with markers for each park (click a marker or pick a park from the list)
- Live location tracking using the browser's HTML5 Geolocation API
- Driving route drawn on the map using the OSRM routing API
- Route summary with distance and estimated drive time
- Turn-by-turn directions listed in the sidebar
- Click anywhere on the map to set a start point if location access is denied or unavailable
- Clear-route button and a layout that adapts to mobile screens

## Built with

- HTML, CSS and JavaScript
- [Leaflet.js](https://leafletjs.com/) for the map
- [OpenStreetMap](https://www.openstreetmap.org/) base layer
- [OSRM](https://project-osrm.org/) (Open Source Routing Machine) public API for routing

## How it works

1. The page loads the map centered on Rawalpindi and places a marker for each park.
2. The browser asks for location permission and tracks the user's position.
3. When a park is selected, the app sends the start and destination coordinates to the OSRM API.
4. The returned route geometry is drawn on the map, and its distance, duration and steps are shown in the sidebar.

## Run locally

1. Download or clone this repository.
2. Open `index.html` in a browser and allow location access.

An internet connection is required for the map tiles and routing. When opened as a local file, the page uses a fallback base map, because OpenStreetMap tiles are only served to hosted sites.

## Customize

Parks are stored in the `PARKS` array near the top of the script in `index.html`. Add or edit entries with a `name`, `lat` and `lng` to change the locations.

## Notes

- Routing uses the free public OSRM server, which is intended for demos and may occasionally be slow.
- Routes are calculated when a park is selected and are not recalculated as the user moves.

## Data and credits

Map data © OpenStreetMap contributors. Routing by OSRM. Map library by Leaflet.
