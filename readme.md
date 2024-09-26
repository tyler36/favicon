# How to Favicon in 2022: Six files that fit most needs

- [How to Favicon in 2022: Six files that fit most needs](#how-to-favicon-in-2022-six-files-that-fit-most-needs)
  - [tldr](#tldr)
  - [The files](#the-files)

## tldr

- Based on [How to Favicon in 2022](https://evilmartians.com/chronicles/how-to-favicon-in-2021-six-files-that-fit-most-needs?ref=heydesigner#changelog)

```html
<link rel="icon" href="/favicon.ico" sizes="32x32"><!-- 32×32 -->
<link rel="icon" href="/icon.svg" type="image/svg+xml">
<link rel="apple-touch-icon" href="/apple-touch-icon.png"><!-- 180×180 -->
<link rel="manifest" href="/manifest.webmanifest">
```

```json
// manifest.webmanifest
{
  "icons": [
    { "src": "/icon-192.png", "type": "image/png", "sizes": "192x192" },
    { "src": "./icon-mask.png", "sizes": "512x512", "purpose": "maskable" },
    { "src": "/icon-512.png", "type": "image/png", "sizes": "512x512" }
  ]
}
```

## The files

- `favicon.ico` for legacy browsers
- A single SVG icon with a light/dark version for modern browsers
- 180×180 `apple-touch-icon.png` PNG image for Apple devices
- Web app manifest with 192×192 and 512×512 PNG icons for Android devices
- Web app should include maskable version with padding, safe zone is 409x409
