double-click `index.html` — you'll see a warning banner in that case. To test
# Sampled Locations Map

A Leaflet map that plots the coordinates encoded in WebP filenames, displays
each image in a marker popup, and lists locations in a fly-to sidebar. It also
shows two toggleable polygon overlays on OpenStreetMap.

## Files

- `index.html` redirects the published site to the map.
- `my-story-map/index.html` contains the map application.
- `annotation_png/` contains optimized September WebP images and `manifest.json`.
- `Convention_1_png/` contains optimized Convention 1 WebP images and `manifest.json`.
- `Polygons.geojson` and `Polygons_1.geojson` provide the polygon overlays.
- `.venv/` is local-only and excluded from Git.

The manifest is used instead of a directory listing because static hosts such
as GitHub Pages do not generate browsable file listings. If images are added
or removed, regenerate the relevant manifest from the WebP filenames.

## Run locally

Start a server from the repository root:

```powershell
python -m http.server 8000
```

Open `http://localhost:8000/` in a browser.

## Publish with GitHub Pages

Push the repository to the `main` branch and enable **Settings → Pages → GitHub
Actions**. The workflow deploys the site from the repository root. Original PNG
files are kept locally but excluded from Git; the optimized WebP files total
about 418 MB.
