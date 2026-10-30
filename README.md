# Maths-v2

A short creative web experiment titled “Maths is not romantic.” The root `index.html` combines mathematical imagery with play and replay controls for the included audio file, `pro.mp3`.

## Preview locally

Open `index.html` in a browser, or serve the project folder over HTTP:

```sh
python -m http.server 8000
```

Then visit <http://localhost:8000>.

## Personalize the page and audio

The page content and presentation are defined in `index.html`. Its Google Fonts link is external; changing or removing it may affect the typography. If replacing `pro.mp3`, keep its path aligned with the page reference, or update the reference if you rename or move the file. Keep the audio file in the project folder when hosting the static page so the relative path continues to work.

Mobile browsers may require a user gesture before audio can play, so use the controls when checking audio.