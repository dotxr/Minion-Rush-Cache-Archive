# Minion Rush (Cache Archive)

Every Minion Rush asset still pullable from Gameloft's servers as of September 2026, from the 2013 launch through the Unity farewell update.

| Folder | Era | Client ID | Versions |
|---|---|---|---|
| `native-1677/` | Original engine (Gaia) | `1677:53162` | iOS 1.0.0k – 5.7.0k, Android 5.1 – 5.7, Amazon 1.2 – 5.7 |
| `native-3493/` | Original engine (Gaia) | iOS `3493:71465`, Amazon `3493:75247` | iOS/Android 7.8.0e – 10.5.0e, Amazon 7.0.0a – 10.5.1a |
| `unity/` | Unity remake (MRU) | `mru:7094:85785` | 12.0.1 – 13.4.0 |

## Layout

- `assets/`: iris assets, flat, original names. Native assets are LZMA-alone as served.
- `tocs/`: `mnhtn_toc_*` and `mnhtn_index_*`.
- `versions.json`: platform → version → `{ toc, assets, missing }`.
- `eve/`: recorded discovery configs.
- `hash_files/` (native): Gameloft's size and SHA-1 chunk lists. The assets were checked against them.
- `sem/`, `manifest.json`, `snapshots/` (unity): event images, build → asset map, and live state from 2026-09-26 (leaderboards, config, events).

## Gaps

- `missing` in `versions.json` lists assets that were already deleted upstream.
- `native-1677` only has the latest TOC for each platform. The iOS 6.x TOCs are gone.
- Files over 99 MB are tracked with Git LFS.
