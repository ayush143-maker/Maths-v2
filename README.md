# Maths-v2

Maths-v2 is a short creative web experiment titled “Maths is not romantic.” Its root `index.html` draws labeled axes and two advancing curves on a canvas, with equation labels and timed lyric text. The animation timeline is configured for 15 seconds and includes a title and a visual effect where the curves meet.

The initial overlay offers Play. Clicking the overlay starts the sequence, and a Replay control is shown at the end. The audio source is the local file `pro.mp3`; the script checks whether audio data loads and can run its animation timeline using the performance clock. These source details do not guarantee successful audio playback in every browser.

## Preview locally

Open `index.html` in a browser, or serve the project folder over HTTP:

```sh
python -m http.server 8000
```

Then visit <http://localhost:8000>. Use the controls when checking the animation and audio; mobile browsers may require a user gesture before audio can play.

## Customize and troubleshoot

Page content and presentation are defined in `index.html`. If replacing `pro.mp3`, keep its path aligned with the page reference, or update the reference if you rename or move the file. Keep the local audio file in the project at the referenced location. When audio does not load, compare the page reference with the actual filename and location, including capitalization.

The page loads Caveat and Poppins from Google Fonts. It adjusts the canvas and lyric positions on window and visual-viewport resize. A failed font request may affect typography and is separate from a missing local audio file.

## Project files

- `index.html` — page entry point, canvas animation, lyrics, and controls.
- `pro.mp3` — local audio asset.

No build scripts or deployment configuration are documented.