# Maths-v2

A short creative web experiment titled “Maths is not romantic.” The root `index.html` combines mathematical imagery with play and replay controls for the included local audio asset, `pro.mp3`, also in the project root.

## Preview locally

Open `index.html` in a browser. Alternatively, serve the project folder over HTTP by running:

    python -m http.server 8000

Then visit http://localhost:8000. Reload the page after editing to review the result.

## Making changes

The page and its interaction are defined in `index.html`. Keep the audio path intact if replacing `pro.mp3`. Mobile browsers may require a user gesture before sound can play, so use the controls when checking audio in the browser.