# Maths-v2

A short creative web experiment titled “Maths is not romantic.” The root `index.html` combines mathematical imagery with play and replay controls for the included audio file, `pro.mp3`.

## Preview locally

Open `index.html` in a browser, or serve the project folder over HTTP:

```sh
python -m http.server 8000
```

Then visit <http://localhost:8000>.

## Making changes

The page and its interaction are defined in `index.html`. If replacing `pro.mp3`, keep its path aligned with the page reference. Mobile browsers may require a user gesture before audio can play, so use the controls when checking audio. Keep the audio file in the project folder when hosting the static page.