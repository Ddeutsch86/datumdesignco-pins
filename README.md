# datumdesignco-pins
DatumDesignCo Pinterest pin images

## How pin images get here

- Pin images are pushed as base64 text files at `b64jpg/<name>.b64`.
- The workflow `.github/workflows/decode-jpg.yml` runs on each push to `b64jpg/`. It decodes every file to `<name>.jpg` at the repo root.
- The workflow never overwrites a file that already exists. If `<name>.jpg` is already there, it skips that file.
- Files in this repo are add-only. Pin images and their `.b64` sources are never deleted or modified, so every hosted image link keeps working.
