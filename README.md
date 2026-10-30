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

## Configuration and data handling

The listed root files contain no `.env.example` or separate configuration file. This static page has no server-side environment in which to keep secrets: anything placed in its HTML or delivered browser files can be viewed by visitors. Do not put passwords, tokens, or other secrets in the page or tracked files.

The page and `pro.mp3` are project content. Review them before publishing, and do not include private information or audio you do not have permission to distribute.

## Browser and platform reliability review checklist

This is a checklist for a future review, not a record of completed testing or verified results.

- Review the page in current desktop browsers relevant to your audience and on mobile browsers such as Safari on iOS and Chrome on Android where applicable. Consider actual mobile hardware for audio behavior; no compatibility results are recorded here.
- Open developer tools and inspect the console and network panel while loading the page and using play and replay. Look for runtime errors, failed audio or font requests, and responses that indicate the browser could not load the requested resource.
- Confirm that the audio reference in `index.html` resolves to the root `pro.mp3` file. If hosted, check the deployed path and filename capitalization as well as the local path. Start playback through the controls; mobile browsers may require a user gesture.
- Review the Google Fonts request and check that the page remains legible if the external font service is unavailable.
- Compare a narrow mobile-sized viewport with a wide desktop-sized viewport. Check that the mathematical imagery and controls remain visible and usable.

## Manual review checklist

These are review steps, not verified results.

- Open the root `index.html` or use the local preview steps above and review the page and mathematical imagery.
- Use play and replay, observing whether audio starts after interaction and replay behaves as intended.
- After changing audio, fonts, or layout, repeat the path, network, and viewport checks above.

## Accessibility review checklist

These are future review checks, not verified accessibility results.

- Use Tab and Shift+Tab to check keyboard access to play, replay, and other interactive elements. Check focus order and visible focus indicators.
- Review the controls for accessible names that communicate their actions. Check whether the mathematical imagery needs a text alternative or is decorative.
- Check text and control-label contrast, including with the linked font unavailable.
- If the page includes moving or animated visual effects, check them with the operating system's reduced-motion preference enabled. Ensure visitors can choose whether to start or replay audio.