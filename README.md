# Film Dial

Standalone, offline-first film exposure calculator for iPhone.

## Functions

- Import EXIF ISO, shutter speed and actual lens aperture from an Apple Camera photo (manual photo selection required by iOS).
- Calculate equivalent film exposure with linked aperture and shutter dials.
- Supports film ISO, variable/fixed ND, reciprocity correction, and estimated Nikon SB-600 / Godox AD360 flash output.
- Independent EV calibration for the iPhone 1× and 3× cameras.

All calculations and photo metadata are processed locally in the browser; the app does not upload images.

## Publish on GitHub Pages

Open **Settings → Pages** and select **Deploy from a branch → main → / (root)**, then click **Save**.

Public URL: https://alexgrabchilev-cyber.github.io/film-dial/

## Install on iPhone

1. Open the published URL in **Safari** while online.
2. Share → Add to Home Screen → Open as Web App (if prompted).
3. Open Film Dial once with internet, then switch on Airplane Mode and verify that it launches.
4. To import the most recent photo, tap the photo button and select the latest image from the iOS photo picker. Safari cannot silently retrieve a photo from Photos.

## Updating

Commit modified code to `main` and GitHub Pages will redeploy. If you update offline application assets, increment `CACHE_NAME` inside `sw.js` so existing installations get the new version when opened online.

## Exposure accuracy caveats

Apple Camera processing (Smart HDR, automatic camera switching, etc.) may cause film results to differ from what the iPhone photo looks like. Inspect the imported EXIF aperture, disable Night Mode, and calibrate against a reference camera. Flash modifiers need empirical calibration.
