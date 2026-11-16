# JANTEX LAB APP
Created by Kamran_Zahoor

## Publish on GitHub Pages
1. Create a GitHub repo, upload everything in this folder, keep the structure.
2. Settings > Pages > Deploy from branch > main / root.
3. Open https://USERNAME.github.io/REPO/ on Android in Chrome > menu > Add to Home screen.

## Offline OCR (optional but recommended)
Copy these into `libraries/` so OCR works with no internet:
- `tesseract.min.js` and `worker.min.js` from the npm package tesseract.js@5.1.1 (dist folder)
- the tesseract.js-core@5 files (`tesseract-core*.js` and `.wasm`)
- `eng.traineddata.gz` from tessdata_fast
Without them the app uses the CDN when online and the manual review table when offline.

## Data
Everything is stored in IndexedDB on the device. Updating the app never touches it. Export a JSON backup from the Backup tab regularly; devices do not sync.

## Honest limits
Handwriting OCR is unreliable. Always check the review table before saving.
