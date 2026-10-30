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

## Troubleshooting

Use these as diagnostic checks; they do not indicate known problems.

1. Confirm you opened the root `index.html`, the page’s entry point.
2. If audio does not load, compare its reference in `index.html` with the local `pro.mp3` file. Preserve the relative path and check filename capitalization, especially when hosted.
3. Inspect the browser console for errors and the network panel for failed audio, page, or font requests. Try playback through the controls; mobile browsers may require a user gesture.
4. `pro.mp3` is a local project asset; Google Fonts are an external network request. A font request failure is distinct from a missing audio file and may affect typography instead.

## Configuration and data handling

The listed root files contain no `.env.example` or separate configuration file. This static page has no server-side environment in which to keep secrets: anything placed in its HTML or delivered browser files can be viewed by visitors. Do not put passwords, tokens, or other secrets in the page or tracked files.

The page and `pro.mp3` are project content. Review them before publishing, and do not include private information or audio you do not have permission to distribute.

## Review checklist

These are review steps, not verified test results.

- Review the page and mathematical imagery at narrow and wide viewport sizes, including on mobile hardware where practical.
- Use play and replay and observe whether audio starts after interaction and replay behaves as intended.
- After changing audio or layout, repeat the path and browser-console checks above.

## Accessibility review checklist

These are future review checks, not verified accessibility results.

- Use Tab and Shift+Tab to check keyboard access to play, replay, and other interactive elements. Check focus order and visible focus indicators.
- Review controls for accessible names that communicate their actions. Consider whether the mathematical imagery needs a text alternative or is decorative.
- Check text and control-label contrast, including with the linked font unavailable.
- If the page includes moving or animated visual effects, check them with the operating system’s reduced-motion preference enabled. Ensure visitors can choose whether to start or replay audio.