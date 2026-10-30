# Maths-v2

Maths-v2 is a short creative web experiment titled “Maths is not romantic.” The root `index.html` combines mathematical imagery with play and replay controls for the included `pro.mp3` audio file.

## Preview locally

Open `index.html` in a browser, or serve the project folder over HTTP:

```sh
python -m http.server 8000
```

Then visit <http://localhost:8000>. Use the audio controls when checking playback; mobile browsers may require a user gesture before audio can play.

## Customize and troubleshoot

Page content and presentation are defined in `index.html`. If replacing `pro.mp3`, keep its path aligned with the page reference, or update the reference if you rename or move the file. Keep the local audio file in the project at the referenced location. When audio does not load, compare the page reference with the published filename and location, including capitalization.

The page links to Google Fonts, which require network access. A failed font request may affect typography and is distinct from a missing local audio file. No deployment host or publishing configuration is documented.

## Project files

- `index.html` — page entry point, presentation, and audio controls.
- `pro.mp3` — local audio asset.