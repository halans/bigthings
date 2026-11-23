# Big Things for iPhone — marketing site

A static, dependency-free site for the iOS app: `index.html` (home), `privacy.html`
(the privacy policy the App Store asks for) and `styles.css`. No build step: open
`index.html` in a browser, or host the folder anywhere that serves static files
(GitHub Pages, Cloudflare Pages, Netlify, or a folder on bigthings.downunder.blue).

It's self-contained so it can move to its own repo unchanged.

## Look

Colours, fonts and the outlined "sticker" style come from the app's `Theme.swift`
(which mirrors the web app), including the dark palette, chosen automatically by
`prefers-color-scheme`.

## Before publishing

- **App Store link.** The "Coming soon to the App Store" buttons in `index.html` point
  to `#download` and the web map. Once the app is live, replace them with the App Store
  URL and Apple's official "Download on the App Store" badge (see Apple's marketing
  guidelines), and update the Download section's text.
- **Support.** support@halans.dev is linked from both footers and the privacy page. For the
  App Store's Support URL, use this site's home page (or add a support page).
- **Numbers.** The stats and category counts (481 mapped, 300 with photos, 1,075 claimed
  nationally) are from the dataset of 2026-11-21. Update them when the dataset grows.
- **Privacy policy.** It describes the app as built on 2026-11-23: no analytics, location
  only on request and on device, favourites on device. Re-check it if the app ever adds
  networking, accounts or analytics.
- **Photo.** `images/screens/detail.jpg` shows the Big Banana photo (Halans Photography,
  CC BY-SA 4.0) with two people in it.

## Screenshots

`images/screens/*.jpg` are from the iPhone 17 simulator (iOS 27.3, light appearance),
resized to 644×1400. To refresh one:

```
xcrun simctl io booted screenshot screen.png
sips -Z 1400 -s format jpeg -s formatOptions 82 screen.png --out images/screens/<name>.jpg
```

## Fonts

`fonts/` holds the same files the app bundles: Caprasimo and Inter, both under the
SIL Open Font License 1.1 (https://openfontlicense.org), which allows using and
redistributing them with a site like this.
