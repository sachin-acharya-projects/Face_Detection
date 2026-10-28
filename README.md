# Face Detection

A browser-based face detection demo built with HTML and JavaScript using [face-api.js](https://github.com/justadudewhohacks/face-api.js). It accesses the camera, detects faces, and overlays face landmarks and predicted facial expressions.

## Preview

[Open the HTMLPreview demo](https://htmlpreview.github.io/?https://github.com/sachin-acharya-projects/Face_Detection/blob/docs/improve-readme-preview-links/index.html)

> The demo needs camera permission and the model files in `models/`. If the preview service cannot resolve the project's root-relative `/models` paths, run it locally as described below.

## Features

- Live camera input through the browser.
- Face detection with the Tiny Face Detector model.
- 68-point facial landmark overlays.
- Facial-expression predictions.
- Detection overlays drawn on a canvas.

## Tech stack

- HTML and CSS
- Vanilla JavaScript
- [face-api.js](https://github.com/justadudewhohacks/face-api.js)
- Browser MediaDevices / camera APIs

## Run locally

Camera access generally requires HTTPS or localhost. Because the code requests model files from `/models`, serve the repository root rather than opening `index.html` directly.

```bash
git clone https://github.com/sachin-acharya-projects/Face_Detection.git
cd Face_Detection
python -m http.server 8000
```

Open [http://localhost:8000](http://localhost:8000), allow camera access, and wait for the models to load.

## Project structure

- `index.html` — page and camera video element.
- `script.js` — model loading, camera setup, detection loop, and overlays.
- `face-api.min.js` — bundled face-api.js library.
- `models/` — pre-trained model manifests and weight shards.

## Troubleshooting

- **Camera does not start:** use localhost or HTTPS, grant camera permission, and ensure another app is not holding the camera.
- **Models fail to load:** serve the repository root and confirm that `models/` is available at the requested URL.
- **No detections:** ensure your face is visible and well lit, and wait until all model files finish loading.

## Privacy

Camera frames are processed in the browser by this demo. Review the source and third-party library before using it with sensitive footage.

## License

No project-specific license is currently documented. Check the repository and dependency licenses before redistributing the code or model assets.
