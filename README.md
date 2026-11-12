# Video Shake Editor

Single-file browser app that adds realistic camera shake to videos. Everything runs locally in the browser, no uploads.

## Use

- Open `index.html` directly (download the raw file), or
- Serve via GitHub Pages: Settings > Pages > Deploy from branch > `main`.

## Features

- Procedural shake engine: presets, seed, intensity, drift, sway, tremor, roll, gait bounce, zoom breathing.
- Reference shake transfer: extracts the full camera motion of a handheld clip; slow intended movement becomes editable camera-move keyframes, the residual shake adds on top.
- Camera-move timeline: keyframe pan X/Y and roll, smoothstep easing, drag to retime.
- Auto safety zoom so no black borders appear.
- HEVC/H.265 to H.264 converter (ffmpeg.wasm, in-browser).
- Frame-accurate MP4 (H.264 + AAC) export via WebCodecs; every frame rendered at its exact timestamp. Real-time recording fallback for browsers without WebCodecs.
- Settings save/load as JSON, including seed, keyframes and the reference trajectory.

Recommendation: match the export frame rate to the source clip for smoothest motion.