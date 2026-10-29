# Clawd on Desk — source

The home of the supplied **Clawd on Desk 1.3.0** desktop source: a fuzzy Solana Clawd companion. The browser version lives on Musebook at [musebook.trade/clawd-desk](https://musebook.trade/clawd-desk/) — drag Clawd to a comfortable spot, try a pose, or hide the companion and bring them back later.

This repository exists to distribute the source archive. The archive used to ship inside the musebook.trade website build (58 MB in `web-react/public/`); it now lives here as a GitHub release asset so the site deploy stays lean and no single file exceeds the 25 MB per-file limit of the Pages deploy path.

## Downloads

- All releases: https://github.com/themusebook/clawd-on-desk/releases
- **Source archive (1.3.0):** https://github.com/themusebook/clawd-on-desk/releases/download/source-1.3.0/clawd-on-desk-source.tar.gz
  - Size: 58,415,254 bytes
  - SHA-256: `968571ed67e2e1b382c221546df2b7be35b2c7214ef3d923e013cfccc50638ef`

The archive is the frozen allowlisted source: dependencies, caches, private local files, and build outputs are excluded. See [SOURCE.md](SOURCE.md) for the hosting and provenance notes; every included source file and its SHA-256 is recorded in the inventory referenced there (source inventory SHA-256: `4c421a2664199fc6fef46a73a7762058d1a50fae2765bf063f1dc2a2c226c8da`).

## Add Clawd to your own page

Place this before your closing body tag:

```html
<script src="https://musebook.trade/clawd-desk/companion.js" data-clawd-assets="https://musebook.trade/clawd-desk/assets/" defer></script>
```

The floating companion remembers its position and visibility in the visitor's browser. The supplied static mascot is used when the visitor requests reduced motion.

## Website events

A website can request a pose or visibility change:

```js
document.dispatchEvent(new CustomEvent('clawd:companion', { detail: { state: 'happy' } }));
document.dispatchEvent(new CustomEvent('clawd:companion', { detail: { action: 'hide' } }));
document.dispatchEvent(new CustomEvent('clawd:companion', { detail: { action: 'show' } }));
```

These browser interactions do not mirror local coding sessions or connect to the desktop LAN bridge.

## Source and credits

Clawd Solana theme and supplied mascot: 8bit. Original desktop project: Clawd on Desk 1.3.0, by rullerzhou-afk and its contributors.

## License

The desktop source is licensed under **AGPL-3.0-only**; artwork retains its separate rights. The full license texts (desktop code license, artwork license, and original third-party notices) ship with the website bundle at https://musebook.trade/clawd-desk/ and inside the source archive.
