# Archived railway validation: 24 September 2026

[Current validation](validation.md) · [Back to the project](../README.md)

This page records the 24 September 2026 railway stage. The October model work did not rerun its checks.

The local delivery record reports a save and file-opening check in **Rhino 8.6.24101.5001**. The model size was **276,184,031 bytes**. The original publication review hashed the file again. Its hash matched the existing native and independent transport records.

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

Material records do not count distinct visible appearances. Crossing and deck checks examine the recorded subset, not every possible pair of objects. Retained-object checks exclude the recorded replacements.

## Why one comparison initially failed

Rhino changed some optional caches and bounding-box serializations during the save. A full JSON comparison without caches matched **76,161 objects**, but left **141 differences**. That intermediate result remains a failure in the evidence record.

The later proof compared exact geometry values with RhinoCommon `GeometryEquals`. It also examined underlying surfaces, curves and topology where necessary. This resolved the remaining 91 Breps and 50 meshes. The combined record accounts for all 76,302 geometries in the master and native files. The local archive keeps the intermediate result.

A file-encoding difference does not necessarily mean a shape change. An explicit extra check must resolve the difference before a record can call the geometries equivalent.

## What was verified for publication

- The checked model's byte count and SHA-256 matched the frozen audit.
- Selected images matched native capture hashes.
- Public summaries contain selected scalar values and hashes of named local reports.
- The public files contain text, summary JSON and selected PNGs. Models and raw data remain local.
- The publication review examined image and Markdown links before upload.

That original publication review did not rerun the geometry analysis or open Rhino again. It compared the snapshot with existing records. The public repository cannot reproduce the full geometry tests without the local models and source data. Hashes identify evidence. They are not third-party certification.

The [24 September summary](../evidence/2026-09-24-summary.json) retains structured values and source-report hashes. The [image manifest](../evidence/image-manifest.json) records provenance. The height and conceptual-detail limits in [Terrain & transport](terrain-and-transport.md#known-limitations) still apply.
