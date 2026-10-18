# Validation and the limits of the latest snapshot

[Back to the project](../README.md) · [Model and preview performance](model-performance.md)

**Public snapshot: 14 October 2026. Model stage: 8 October 2026, final gray model.**

On **9 October 2026**, the initial publication review independently hashed the local master and all 100 tiles. All **101** matched the final archive's file identities. No model was missing or different. That review did not generate a model, rerun geometry or performance tests, or start Rhino. Later screenshot reviews have separate scopes.

```text
Local main model: Overall_Site_Model.3dm
Bytes: 667,461,392
SHA-256: 336881f5258d1a0177a3d133bfe72bf4068de897a4290eaac9d01597743c1b06
Model is not distributed.
```

## Native screenshot review: 9 October 2026

The later 9 October review opened that master in the local Rhino graphical user interface (GUI). Existing Line drawing style displayed a full-site view and an urban-river detail. Native ViewCaptureToFile exports used **2,400 × 1,230 pixels**.

- [Complete-site capture](../images/model-native-overview.png)
- [Urban-river detail](../images/model-native-detail.png)

These PNGs are direct native exports without later image edits. No changes were saved to the source model. The [image manifest](../evidence/image-manifest.json) records identities and capture sources.

This visual review added no performance samples and did not rerun geometry validation. The **8 October geometry/cache evidence and 12-run benchmark** keep their original report hashes.

## Native presentation views: 14 October 2026

The new views use the final model in the local Rhino 8.6 GUI. Line drawing style and native ViewCaptureToFile exports use **3840 × 1968 pixels**.

- [Dense urban fabric and river](../images/model-urban-river-20261014.png)
- [Interchange and terrain](../images/model-interchange-20261014.png)

No changes were saved to the source model. These views add no performance sample or geometry test. They do not imply a new hash review of all 101 models on 14 October.

## Latest recorded checks

| Check | Recorded scope and result |
|---|---|
| Master / tile objects | 67,196 / 67,177. Another 19 remain only in the master |
| Assembly | 100 tiles of 1,000 × 1,000 m. Original coordinates, meter scale and numbering |
| File format | 101 models in Rhino 7 format. Archive version 70 |
| Independent reads | openNURBS 7.15.0 read 101 models. 134,373 object occurrences checked |
| Supplementary reads | 8.32.2 examined double-precision coordinates and terrain-gray arrays |
| Native display | Rhino 8.6.24101.5001. No Rhino 7 desktop/UI test |
| Geometry processing | 169 meshes. 68,006 accepted planar regions. 219,065 original seam segments checked |
| Full-surface distance bound | 2.576769926318507 × 10⁻⁷ m from source geometry. Below the 0.001 m limit |
| Color correction | Zero added geometry error. Original cameras, named views and optimized geometry |
| Saved caches | 64,166 surface objects / 75,995 meshes. Saved and runtime signatures matched |
| D05 tile | 1,281 surface signatures matched. Functional check, outside performance statistics |

The geometry proof examines full projected coverage and constrained planar retriangulation. It preserves holes, orientation and area. It does not measure survey error or certify structures. Regions without proof keep their geometry. Foundations keep their original open-mesh state. They are not newly closed solids.

Cache signatures include universally unique identifiers (UUID), cyclic redundancy checks (CRC), face/vertex counts and double-precision mesh data. The checks establish saved display-mesh reuse after actual opening and drawing. They do not establish a general speed claim. The separate [12-run comparison](model-performance.md#same-period-native-comparison) states its timing results and limits.

The earlier three-new-run gray comparison keeps **ACCEPTANCE_FAILED**. Its rotation was slower than a reused earlier baseline. The later same-period 12-run comparison passed its stated timing criteria. The records keep the two results separate. Three runs per version are descriptive. Time-separated results do not identify the cause of a regression.

## Current files and the historical package

The historical final package contained **106 files**: one master, 100 tiles and five support files. Its 693,538,724-byte ZIP passed full member-length, SHA-256 and CRC checks. That ZIP is absent from its former local location. The repository offers no model or archive download.

The directory recorded in the 9 October review contains **107 files**. These include an added earlier railway-reference model. Its README also changed after the historical delivery. The final master and 100 tiles still match their recorded identities. The directory is not an unchanged 106-file package.

The current README gives bilingual assembly and preview instructions. Ordinary Save keeps display caches. SaveSmall removes them.

## Keep validation stages distinct

The [24 September narrative](rail-validation-2026-09-24.md) keeps its historical figures and date. The [24 September summary](../evidence/2026-09-24-summary.json) remains byte-identical. They describe the earlier 276,184,031-byte model, with 21 rail-module and 45 rail–ground-road checks. The October work and publication updates did not rerun those checks. Historical object, layer and material counts are not current scene counts.

October color and performance work does not establish surveyed transport heights or repair every unresolved bridge and road relationship. Conceptual station details and estimated elevations retain their limits in [Terrain & transport](terrain-and-transport.md#known-limitations).

## What the public evidence provides

Native PNGs show the recorded result. The [structured summary](../evidence/summary.json) gives selected totals, stage labels, model identities and hashes of named reports. The [image manifest](../evidence/image-manifest.json) records image sources.

Local paths, personal identifiers, raw geometry, logs, machine-specific scripts, models and source data remain outside the repository. These public files cannot reproduce the full local geometry checks. Hashes identify evidence, not independent certification. [Sources & credits](../SOURCES.md) states attribution and reuse limits.
