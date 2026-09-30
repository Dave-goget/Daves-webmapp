# Dave project webmap

The map uses OpenStreetMap tiles, coordinate-based September and Convention 1 image markers, and two polygon overlays. The root page redirects to `my-story-map/`.

## Local preview

From the repository root, run:

```powershell
python -m http.server 8000
```

Open http://localhost:8000/ in a browser. This address works only on the computer running the server; it is not a public sharing link.

## Map assets

- `annotation_png/` and its `manifest.json` contain optimized September WebP images.
- `Convention_1_png/` and its `manifest.json` contain optimized Convention 1 WebP images.
- Original PNG files are preserved locally and ignored by Git because they total over 2.8 GB.
- `Polygons.zip` and `Polygons_1.zip` are the original shapefiles.
- `Polygons.geojson` and `Polygons_1.geojson` are the map-ready polygon overlays.

The optimized WebP images total about 418 MB, within GitHub Pages' 1 GB published-site limit. After creating a GitHub repository, push this project to its `main` branch and enable **Settings → Pages → GitHub Actions**. The workflow in `.github/workflows/pages.yml` deploys the site; the public URL will be `https://<your-github-username>.github.io/<repository-name>/`.