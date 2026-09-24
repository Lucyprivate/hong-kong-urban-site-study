# Validation and the limits of a public snapshot

[Back to the project](../README.md)

The latest local delivery was saved and reopened in **Rhino 8.6.24101.5001**. Its recorded model size is **276,184,031 bytes**. During preparation of this public snapshot, the file was hashed again and matched the existing native-reopen and independent transport-validation records.

```text
SHA-256 of the local checked model (model not distributed):
61ce9db29a83f9338bd12e412eff830ff13f7a6652f2184b7264a014e1c76b96
```

## Recorded results

| Check | Recorded result |
|---|---:|
| Model-space objects | 76,302 |
| All objects, including the layout detail | 76,303 |
| Layers | 58 |
| Material-table records | 55 |
| Retained baseline objects checked | 72,079 |
| Ground replacement exceptions recorded | 1,192 |
| Legacy geometry replacements recorded | 30 |
| Closed new-deck checks | 86 |
| Invalid / out-of-frame / unexpected / missing objects | 0 / 0 / 0 / 0 |
| Rail-module crossing checks / failures | 21 / 0 |
| Rail–ground-road checks / failures | 45 / 0 |
| Native reopening | Success recorded |

Material-table records are not a count of distinct visible appearances. Crossing and deck checks cover the recorded subset, not every possible pair of scene objects. Retained-object checks exclude the explicitly recorded replacements.

## Why one comparison initially failed

Saving through Rhino changed some optional caches and bounding-box serialisations. A full cache-free JSON comparison matched **76,161 objects**, but still left **141 differences**. That intermediate comparison was not silently relabelled as a pass.

The subsequent recorded proof compared exact geometry values, using RhinoCommon `GeometryEquals` and the underlying surfaces, curves and topology where needed. It resolved the remaining 91 Breps and 50 meshes. The combined record reports all 76,302 master/native model geometries accounted for. The original intermediate result remains in the local evidence archive.

This separation matters: a file-encoding difference need not imply a shape change, but it requires an explicit follow-up check before the saved model can be called equivalent.

## What was verified for publication

- The current local checked-model byte count and SHA-256 agree with the frozen audit.
- The selected latest-stage image hashes agree with the native capture audit.
- Public summaries are selected scalar values from named local reports, accompanied by report hashes.
- Public files are restricted to explanatory text, summary JSON and selected PNGs; model and raw-data formats are excluded.
- Image and Markdown links are checked within the publication folder before upload.

This publication pass did **not** rerun the complete geometric analysis or reopen Rhino again. It checks the snapshot against the existing local records. Because models and source datasets are not distributed, a reader cannot independently reproduce the full geometry tests from this repository alone. Hashes identify the local evidence; they are not third-party certification.

See [summary.json](../evidence/summary.json) for structured values and source-report hashes, and [image-manifest.json](../evidence/image-manifest.json) for image provenance. The project remains a work in progress with the height and conceptual-detail limits described in [Terrain & transport](terrain-and-transport.md#known-limitations).
