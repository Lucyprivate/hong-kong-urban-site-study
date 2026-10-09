# Validation and the limits of the latest snapshot

[Back to the project](../README.md) · [Model and preview performance](model-performance.md)

**Public snapshot: 9 October 2026. Model stage: the final gray complete-site model of 8 October 2026.**

The current local main model and all 100 tiles were independently hashed for this publication update. All **101** match the per-file identities in the final recorded archive validation, with no missing or mismatching model. This checks the current files against the existing evidence; the publication update did not regenerate the model, rerun the geometry analysis or start Rhino.

    Local main model: Overall_Site_Model.3dm
    Bytes: 667,461,392
    SHA-256: 336881f5258d1a0177a3d133bfe72bf4068de897a4290eaac9d01597743c1b06
    Model is not distributed.

## Latest recorded checks

| Check | Scope and recorded result |
|---|---|
| Main scene / tile objects | 67,196 / 67,177; 19 objects remain only in the main scene |
| Assembly | 100 tiles of 1,000 × 1,000 m; original coordinates, metre scale and numbering retained |
| Native file format | All 101 models saved in Rhino 7 format, archive version 70 |
| Independent kernel reads | OpenNURBS 7.15.0 read all 101 models; 134,373 main/tile object occurrences checked |
| Supplementary reads | 8.32.2 checked double-precision coordinates and terrain-gray arrays |
| Native display tests | Rhino 8.6.24101.5001; no Rhino 7 desktop/UI test claimed |
| Geometry processing | 169 changed meshes; 68,006 accepted planar regions; 219,065 original tile seam segments checked |
| Full-surface distance bound | 2.576769926318507 × 10⁻⁷ m relative to the source geometry, below the 0.001 m processing limit |
| Color correction | Zero additional geometry error; original cameras, named views and validated optimized geometry retained |
| Saved surface caches | 64,166 surface objects / 75,995 meshes; saved and actual runtime signatures matched |
| Representative D05 tile | 1,281 surface objects matched saved/runtime signatures; a functional check, not part of the performance statistics |

The geometric bound uses full projected coverage and constrained planar retriangulation with holes, orientation and area preserved. It does not measure survey error or certify a structure. Regions without the required proof retained their geometry. The foundations retain their original open-mesh state; this is not a claim of newly closed solids.

Native cache signatures include UUID, CRC, face/vertex counts and double-precision mesh signatures. These checks concern reuse of persisted surface display meshes after actual opening and drawing. They do not establish a general speed claim by themselves; the [performance comparison](model-performance.md#same-period-native-comparison) reports the separate 12-run timing result and its limits.

The earlier three-new-run gray comparison retains **ACCEPTANCE_FAILED** because rotation was slower than a reused older comparison baseline. The later same-period 12-run comparison passed its stated timing criteria. Both remain in the evidence history; three runs per version are descriptive, and time-separated results do not isolate the cause of a regression.

## Current files and the historical package

The final historical package contained **106 files**: one main model, 100 tiles and five supporting files. Its 693,538,724-byte ZIP was recorded as passing complete member-length, SHA-256 and CRC checks. That historical ZIP is **not currently present at its former local location**, and this repository provides no model/archive download.

The current local directory contains **107 files**, including the added earlier railway-reference model. Its README has also been updated since that historical package. The final main model and 100 tiles still match their recorded identities; the current directory must not be described as an unchanged 106-file delivery. The current README supplies concise bilingual assembly and preview instructions. Cache preservation is described separately: ordinary Save retains caches; SaveSmall removes them.

## Keep validation stages distinct

The [24 September railway-validation narrative](rail-validation-2026-09-24.md) retains its original figures with its historical date and links clarified. The [24 September structured summary](../evidence/2026-09-24-summary.json) is preserved byte for byte. They describe the earlier 276,184,031-byte model, including its 21 railway-module and 45 rail–ground-road checks. **Those checks were not rerun as part of the October model or this publication update.** Their object/layer/material counts must not be presented as the latest scene counts.

The October color/performance work also does not turn earlier estimated transport elevations, conceptual station details or unresolved road/bridge interfaces into surveyed facts or complete engineering repairs. The source-versus-estimate limits in [Terrain & transport](terrain-and-transport.md#known-limitations) continue to apply.

## What the public evidence provides

Selected native PNGs show the recorded result. The [structured summary](../evidence/summary.json) publishes selected scalar totals, stage labels, model identities and hashes of named local reports. The [image manifest](../evidence/image-manifest.json) records image provenance. Absolute local paths, personal identifiers, raw geometry, working logs, machine-specific scripts, models and source datasets remain outside the public repository.

Readers cannot reproduce the complete local geometry checks from these selected files alone. Hashes identify evidence; they are not independent certification. Source credit, contribution and reuse scope remain governed by [Sources & credits](../SOURCES.md).
