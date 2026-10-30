# Maths-v2

A short creative web experiment titled “Maths is not romantic.” The project’s root `index.html` combines mathematical imagery with play and replay controls for the included `pro.mp3` audio file.

## Project files

- `index.html` — page entry point and presentation.
- `pro.mp3` — audio asset.
- The page links to Google Fonts, an external resource.

## Preview locally

Open `index.html` in a browser, or serve the project folder over HTTP:

```sh
python -m http.server 8000
```

Then visit <http://localhost:8000>. Use the audio controls when checking playback; mobile browsers may require a user gesture before audio can play.

## Deployment-readiness checklist

The following are recommendations, not verified deployment results. No deployment host or publishing configuration is specified here.

- [ ] **Choose the correct published root/output.** The entry point is the root `index.html`. Configure the publishing process to serve the project folder containing `index.html` and `pro.mp3` as its output. Check that the published root does not point to a folder that omits these files.
- [ ] **Keep asset paths valid.** Keep `pro.mp3` at the path referenced by `index.html`, or update the page reference if the file is renamed or moved. Preserve filename capitalization and relative paths; check that the published copy includes the audio file.
- [ ] **Account for external fonts.** The Google Fonts link requires network access. If it cannot load, typography may differ; the page and local audio should not be confused with that external dependency.
- [ ] **Review content and configuration for safety.** The supplied root-file inventory lists no `.env.example` or separate configuration file. This static page has no server-side environment in which to keep secrets: anything placed in its HTML or delivered browser files can be viewed by visitors. Do not put passwords, tokens, or other secrets in the page or tracked files. Review the page and audio for private information, and publish audio only if you have permission to distribute it.
- [ ] **Preview after publishing.** Open the published page and check that it loads from the intended root, the layout appears as expected, and play and replay work after interaction. Check the browser console and network panel for failed page, audio, or font requests. This is a recommended manual review, not a completed check.

## Customize and troubleshoot

Page content and presentation are defined in `index.html`. If replacing `pro.mp3`, keep its path aligned with the page reference, or update that reference if you rename or move the file. When a resource is missing, compare its reference in `index.html` with the published filename and location, including capitalization. A failed Google Fonts request is distinct from a missing local audio file and may affect typography instead.

## Accessibility review checklist

These are future review checks, not verified accessibility results.

- [ ] Use Tab and Shift+Tab to check keyboard access, focus order, and visible focus indicators for play, replay, and other interactive elements.
- [ ] Check that controls have accessible names that communicate their actions. Consider whether the mathematical imagery needs a text alternative or is decorative.
- [ ] Check text and control-label contrast, including when the linked font is unavailable.
- [ ] If the page includes moving or animated visual effects, check them with the operating system’s reduced-motion preference enabled. Ensure visitors can choose whether to start or replay audio.
