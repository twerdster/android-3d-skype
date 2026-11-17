# Updated browser example

Added 17 November 2026 as a new, project-specific interaction. It is separate from the recovered software and is not the students' implementation.

## What runs

Sample a generated depth surface, set the depth quantization step, rotate its point cloud, move a manual marker anchor and export the generated frame.

The generated surface is sampled on a 160 × 120 grid. Each depth sample is counted as a 16-bit value; reported payload excludes transport headers, color and calibration. Projection uses a fixed illustrative pinhole camera. No latency or sensor accuracy is measured.

## Run

Open https://twerdster.github.io/android-3d-skype/ or serve the repository's `docs/` directory with any static HTTP server. For example, from the repository root:

```sh
python3 -m http.server 8000 --directory docs
```

Open `http://localhost:8000`. The demo uses standard Canvas 2D and local browser controls. No additional demo packages, SDKs or credentials are required. Downloads are generated JSON files. No camera permission is requested.

## Implementation

`docs/index.html` contains the controls and factual scope labels; `docs/demo.js` implements the interaction; `docs/demo.css` contains the responsive layout. All generated images/data are illustrative. It uses no Kinect stream, does not track markers with a camera and does not run the historical app.

## Recorded checks

[VALIDATION.json](VALIDATION.json) records 12 passed browser assertions on the new interaction, JSON export where present, local-only requests, error-free JavaScript and a 390-pixel responsive layout. These are interaction assertions on generated/local examples, not accuracy or compatibility benchmarks. Original native application/hardware coverage is unchanged; see [historical recovery notes](../docs/RECOVERY.md).

## Attribution and terms

Original project: Raafat Francis, Hashem Naara. Supervision: Aaron Wetzler. The new browser example was prepared with Codex assistance in November 2026; Claude reviewed the README wording and factual scope. The new files have a [scoped MIT license](../docs/DEMO-LICENSE.txt); it does not relicense historical code, images, slides, reports or third-party dependencies.
