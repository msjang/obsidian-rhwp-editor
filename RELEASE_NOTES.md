# Release Notes

## 0.2.3

### Fixed

- Fixed edit mode showing raw `rhwp-studio` menu HTML without CSS in Obsidian.
- Fixed edit mode failing to load files with `Cannot read properties of undefined (reading '__wbindgen_malloc')` after rhwp WASM initialization failed inside the iframe.
- Fixed missing SVG sprite icons in the edit mode toolbar and menus.

### Changed

- Edit mode now generates an Obsidian-specific `rhwp-studio-obsidian/` runtime entrypoint before opening the iframe.
- The generated entrypoint inlines CSS and the main JS bundle, rewrites font and renderer URLs for Obsidian resource loading, and passes rhwp WASM bytes directly instead of relying on iframe `app://` fetch.
