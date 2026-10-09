# Model and preview performance

[Back to the project](../README.md) · [Validation](validation.md) · [Image index](../images/README.md)

**Model stage: 8 October 2026. Public snapshot: 9 October 2026.**

The latest complete-site model combines gray terrain, black building attributes and blue water with saved native display meshes. The work reduced terrain and road mesh complexity where complete surface-preservation checks passed, then corrected the preview colors without changing that validated geometry. In the final same-period comparison, the first Shaded preview was faster; opening the cached file itself was slower. The measured gain in opening plus first preview was **5.710%**.

![Final gray complete-site model](../images/model-gray-axon.png)

*Native Rhino capture from the final same-period benchmark, using isolated controlled Shaded settings. This does not depict a change to the user's default Shaded mode.*

## Scene and assembly

The 10 × 10 km scene retains full-size metre coordinates. Its 100 tiles are each 1,000 × 1,000 m: rows A–J run north to south and columns 01–10 run west to east. The main model contains **67,196 objects**; the tiles contain **67,177 object occurrences** in total. The remaining **19 boundary-outside objects** stay in the main model. The existing object assignment and original coordinates were retained; this was not a new split of crossing buildings.

[Open the existing tile assembly index](../images/tile-assembly-index.png).

The final main model and 100 tiles are saved in **Rhino 7 format (archive version 70)**. All 101 files were read through the independent OpenNURBS 7.15.0 kernel. Supplementary 8.32.2 reads checked double-precision coordinates and complete terrain-gray arrays. Actual native display and timing checks used **Rhino 8.6.24101.5001**; no Rhino 7 desktop test is claimed.

## Geometry and appearance

Mesh geometry, excluding surface display caches, changed from **12,520,376 to 10,756,752 faces**, a **14.086%** reduction. Terrain faces changed from **8,831,594 to 7,086,772**, a **19.757%** reduction; 588,918 mesh vertices were removed. The work accepted 68,006 planar regions across 169 changed meshes and retained regions that did not pass the complete proof.

The recorded full-surface bidirectional distance bound is **2.576769926318507 × 10⁻⁷ m**, below the 0.001 m processing limit. This bound comes from complete projected coverage, holes, orientation, area and constrained retriangulation checks. It is not a sampled-point result or a claim about source survey accuracy. Original double-precision vertex positions, 219,065 tile seam segments, boundaries and native topology states were retained. Buildings, railway details and rivers kept their geometry during the later terrain/road and color work. The 100 foundations retain their original open-mesh state.

The final color record contains 63,097 building objects with black attributes, 84 terrain meshes with object RGB(190,190,190), 100 white foundations and 1,069 original blue-water display overrides. Saved terrain vertex grays range from 146 to 198; the previous opaque gray values were shifted by −50 while retaining their order and differences. Color correction added **zero geometry error** relative to the validated optimized model.

The D05 native Line preview illustrates one tile. Its black outlines and lit faces should not be read as every building face rendering pure black. The original cameras and named views remain unchanged. Project preview modes provide the intended appearance without changing the user's default Shaded settings.

![Representative D05 tile in Line drawing style](../images/tile-d05-line.png)

*Actual native D05 functional check. Its diagnostic timing is excluded from the benchmark below.*

## Saved display meshes

The main file retains **75,995 native display meshes** for **64,166 surface objects**, totaling 3,548,417 faces and 4,491,948 vertices. Actual first Shaded and calibrated Line openings matched every recorded surface object's saved UUID, mesh CRC, face/vertex counts and double-precision signature. This verifies cache reuse in those checks; smaller face counts alone do not establish faster interaction.

Ordinary **Save** retains the saved display caches. **SaveSmall** removes them. Wheel sensitivity is an application preference, so neither the model nor its project preview files are claimed to embed a wheel-zoom setting.

## Same-period native comparison

The final comparison used four versions and three independent processes per version: **12 valid runs**, recorded on 8 October 2026 between 04:27:32 and 04:35:40 UTC. The view and image size were held at **1,280 × 720**, with the same camera. The reference was translated only to align its coordinate origin. Temporary isolated Shaded settings were identical; the user's default Shaded mode was not changed for the test.

Time is in seconds. Working set uses decimal GB (10⁹ bytes) after the first Shaded preview. Each value below is the median of three runs.

| Version | Open | First Shaded | Open + first Shaded | Rotation | Working set (GB) |
|---|---:|---:|---:|---:|---:|
| Earlier reference | 5.94439 | 3.67086 | 9.61525 | 0.2265866 | 2.4436 |
| River-optimized comparison | 8.15626 | 11.87751 | 19.97452 | 0.2879994 | 4.7817 |
| Cache-only comparison | 11.04647 | 8.34037 | 19.42046 | 0.2891744 | 4.6738 |
| Final gray model | 10.84489 | 7.82480 | 18.83398 | 0.2675692 | 4.5348 |

**The total column is the median of each run's combined elapsed time, not the sum of the separate Open and First Shaded medians.** First Shaded includes cache preparation, actual isolated viewport initialization, native drawing/message handling and the first captured preview. Rotation is the mean full elapsed time of three successive 5° world-Z rotations per run, followed by the median of those three run means; the display list was not frozen.

Relative to the river-optimized comparison, the final model reduced first Shaded time by **34.121%**, rotation time by **7.094%**, combined open/first-preview time by **5.710%**, and working set by **5.165%**. File opening alone increased by **2.68863 seconds**. Final rotation remained **18.09% slower than the earlier reference**.

The source files were hashed immediately before opening, producing warm operating-system file-cache conditions; no OS cache flush was performed. Three varied run orders provide limited balancing, not a complete four-position/predecessor design. Three runs per version support descriptive medians, not statistical significance or a speed guarantee on other machines or views. D05 functional-diagnostic timing is excluded from these figures.

## Retained earlier failure

An earlier gray-model check added only three new gray runs and reused comparison medians measured roughly seven hours earlier. Its first Shaded median changed from 11.3826032 to 7.9132342 seconds, but rotation changed from 0.2729305333 to 0.2844731333 seconds: **4.229% slower**. Its recorded status remains **ACCEPTANCE_FAILED**.

That comparison was not a simultaneous four-version retest. The later 12-run comparison is reported separately and does not delete, merge or relabel the earlier failure. The time gap limits causal interpretation: these records do not establish that color alone caused the earlier regression or that it was solely environmental variation.

See the [validation narrative](validation.md) and [structured summary](../evidence/summary.json) for the model identity, package changes, source-report hashes and publication limits. The models, project INI files, raw working scripts and source datasets remain local.
