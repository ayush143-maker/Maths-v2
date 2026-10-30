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

## Asset and loading review checklist

This is a checklist of actions to perform, not a record of verified results.

- Check the audio reference in `index.html` against the root `pro.mp3` file and confirm the referenced file is present and plays when started with the page controls.
- Keep only media that the page uses. If replacing the audio or adding imagery, choose files sized for their role rather than keeping unnecessarily large originals or unused variants.
- Review the Google Fonts link in `index.html`; retain it only if the page intentionally uses that font. Check the page typography if the external request is unavailable.
- Inspect `index.html` for other local media and external font or script references. Confirm each is intentional and that local paths resolve.

## Manual review checklist

This is a checklist of actions to perform, not a record of verified results.

- Open the root `index.html` in a browser, or use the local preview steps above, and review the page and mathematical imagery.
- Use the play and replay controls. Check whether audio starts after interaction and whether replay behaves as intended; mobile browsers may require a user gesture.
- Inspect the page at a narrow mobile-sized viewport and a wide desktop-sized viewport. Check that the imagery and controls remain visible and usable.
- If you changed the Google Fonts link, review the typography with that change in place.

## Accessibility review checklist

These are future review checks, not verified accessibility results.

- Use Tab and Shift+Tab to check whether the play and replay controls and any other interactive elements can be reached and operated without a pointer. Check that focus order is sensible.
- Check that each focused control has a clearly visible focus indicator, including while using the audio controls.
- Review the play and replay controls for meaningful accessible names that communicate their actions. Check whether the mathematical imagery conveys information that needs a text alternative; if it is decorative, review whether it is identified as such.
- Check the text and control-label contrast against their backgrounds, including at narrow viewports and with the linked font unavailable.
- If the page includes moving or animated visual effects, check their behavior with the operating system's reduced-motion preference enabled. Review the audio controls separately so visitors can choose whether to start or replay audio.