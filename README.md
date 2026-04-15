# Satellites Tracker

A 2D orbital tracker on a web page dedicated to Italian satellites and the ISS.
The project is intended as a professional prototype for presentations and theses, with TLE support from CelesTrak and SGP4 propagation via `satellite.js`.

## Main File

- `index.html` — complete interface with Leaflet, map view, ISS live, satellite list, and orbital tracks.

## How to Use

### Option 1: GitHub Pages
1. Create a repository on GitHub.
2. Upload `index.html` and `README.md` to the main branch.
3. Activate GitHub Pages from the repository settings, setting the source to `main` / `root`.
4. Open the GitHub Pages URL provided by GitHub.

### Option 2: Local Server
The file uses HTTPS fetch to download TLEs from CelesTrak, so it's recommended to run it from a local server.

With Python:

Powershell
cd "c:\Users\andre\OneDrive\Desktop\Github and projects\satellites-tracker"
python -m http.server 8000

Then open http://localhost:8000 in your browser.

## Key Features

- 2D map with high-quality Leaflet
- Real-time visualization and tracking of the ISS
- Satellite data from official TLEs via CelesTrak
- Professional orbit propagation with `satellite.js` (SGP4)
- TLE/ISS status badges and orbital information
- Robust fallback for unavailable APIs or TLEs

## Thesis Notes

- For the thesis, please include in your submission:
- that the system uses official TLEs from `celestrak.org`
- that SGP4 propagation is handled by `satellite.js`
- the data source and the TLE epoch displayed in the UI
- model limitations (atmospheric perturbations and dynamic accuracy)

## External Dependencies

The project uses public CDNs:

- `Leaflet 1.9.4`
- `satellite.js 4.0.0`

For a true offline package, the CDN files can be downloaded locally and referenced in `index.html`.
