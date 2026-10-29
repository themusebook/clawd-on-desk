# Clawd on Desk — hosting and provenance notes

This file is the provenance record for the Clawd on Desk source archive. It is mirrored from the copy that ships with the website bundle at https://musebook.trade/clawd-desk/SOURCE.md; the download reference below points at this repository's release asset.

The browser companion uses the original Clawd Solana theme supplied by 8bit, from Clawd on Desk 1.3.0. The 19 animated WebPs, static mascot, theme configuration, and copied documentation preserve their original bytes.

The website companion controller is provided separately from the Electron desktop application. The browser companion reacts to website interactions and does not connect to desktop hooks, local coding sessions, or the LAN pairing bridge.

Source code in the desktop download is licensed under AGPL-3.0-only. Artwork is excluded from that source-code license and retains its separate rights. See licenses/LICENSE.txt, licenses/ASSETS-LICENSE.txt, and licenses/NOTICE.md (shipped with the website bundle and inside the archive).

Download the frozen allowlisted source from the release asset: https://github.com/themusebook/clawd-on-desk/releases/download/source-1.3.0/clawd-on-desk-source.tar.gz (SHA-256: 968571ed67e2e1b382c221546df2b7be35b2c7214ef3d923e013cfccc50638ef), with dependencies, caches, private local files, and build outputs excluded. source-inventory.json records every included source file and its SHA-256; manifest.json records the original companion asset hashes and the archive hash.

Source inventory SHA-256: 4c421a2664199fc6fef46a73a7762058d1a50fae2765bf063f1dc2a2c226c8da

Refresh from a supplied checkout (script lives in the musebook-private repo) with:

    node scripts/sync-clawd-desk.mjs --source /path/to/clawd-on-desk

Verify the shipped bundle without that checkout with:

    node scripts/sync-clawd-desk.mjs --check
