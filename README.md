# Hong Kong Urban Site Study

**Ewan · GIS → urban morphology → Rhino site modeling**  
Work in progress · Public snapshot: 14 October 2026

[中文说明](README.zh-CN.md) · [Model & preview](docs/model-and-preview.md) · [Performance](docs/model-performance.md) · [Urban tissue](docs/urban-tissue.md) · [Building heights](docs/building-heights.md) · [Terrain & transport](docs/terrain-and-transport.md) · [Validation](docs/validation.md)

This study connects historical maps, building heights, terrain and transport within a **10 × 10 km** site in northwestern Hong Kong. Geographic information system (GIS) data and Rhino models share a common spatial frame. The documents distinguish source evidence, interpretation and geometric estimates.

The final local set contains a **67,196-object master model and 100 tiles of 1 × 1 km**. The model uses black building attributes, gray terrain, white foundations and blue water. On 9 October 2026, a hash check matched the master and all 100 tiles to the final validation record.

![Dense urban fabric and river corridor](images/model-urban-river-20261014.png)
*14 October 2026. Native export from the local Rhino 8.6 graphical user interface (GUI), with Line drawing style and ViewCaptureToFile. Resolution: 3840 × 1968. No changes were saved to the source model. This is a local view, not the full site extent.*

## Project at a glance

| Scope | Public snapshot |
|---|---|
| Spatial frame | 100 km². EPSG:2326 source coordinates. Full-size meters. No vertical exaggeration |
| Final local models | One master with 67,196 objects. 100 one-kilometer tiles. 101 model files |
| Assembly | Rows A–J: north to south. Columns 01–10: west to east. Original world coordinates |
| Preview | Project Line Drawing and Blue Water Preview modes. Gray terrain and black building attributes |
| Urban tissue | Four paired 800 × 800 m windows. Historical maps from c.1999–2000 and a 2026 compilation |
| Height enrichment | 4,511 building/structure parts received added height representation at the 21 September stage |
| Earlier transport checks | 21 rail-module crossings, 45 rail/ground-road checks and 86 closed-deck checks at the earlier integration stage |
| Public contents | Selected images, methods, source credits and summaries of local checks |

Each count belongs to its stated stage and scope. The tiles contain 67,177 objects in total. Another 19 objects outside their indexing extent remain in the master. A source part is not necessarily a separate building. The October updates did not rerun the earlier transport checks. Geometry checks do not establish survey accuracy or engineering safety.

## Follow the work

1. **[Read urban change](docs/urban-tissue.md).** Compare formation, persistence and internal change. Missing historical coverage does not prove empty land.
2. **[Read height evidence](docs/building-heights.md).** Compare official attributes and historical LiDAR estimates. Unsupported footprints receive no arbitrary height.
3. **[Read terrain and transport](docs/terrain-and-transport.md).** Inspect coastal, road, bridge and railway relationships, including unresolved heights.
4. **[Inspect the model and tiles](docs/model-and-preview.md).** Read the assembly rules, preview settings and geometry checks.
5. **[Read measured performance](docs/model-performance.md).** Compare the final model with earlier versions and retain each test's limits.
6. **[Read validation](docs/validation.md).** Separate final-stage checks, historical records and the 9 October file-identity review.

![Elevated interchange and terrain](images/model-interchange-20261014.png)
*14 October 2026. Native Rhino 8.6 GUI export at 3840 × 1968, with Line drawing style and ViewCaptureToFile. No changes were saved to the source model. This presentation view is not a performance sample.*

![D05 tile in Line Drawing](images/tile-d05-line.png)
*Native Rhino functional check of D05. Its 1,274 buildings have black object attributes. Lighting can make individual faces gray. This tile view is not a performance sample.*

![Tile assembly index](images/tile-assembly-index.png)
*Generated index for the 100 one-kilometer tiles. This diagram is not a Rhino screenshot.*

[9 October native presentation views](docs/model-and-preview.md#native-presentation-captures) · [8 October controlled Shaded benchmark](docs/model-performance.md)

## Earlier study stages

![Tin Shui Wai rail and road context](images/tin-shui-wai-interchange.png)
*Earlier transport integration. Native Rhino capture. Elevated profiles and supports include model estimates.*

![Building-height comparison](images/building-heights-before-after.png)
*Earlier height enrichment. Data-generated comparison with the same camera and ground geometry. The window contains 180 added parts. This is not a Rhino screenshot.*

[Earlier overall axonometric view](images/site-global-axon.png) · [Earlier plan view](images/site-global-plan.png) · [Image index](images/README.md)

## Workflow and contribution

Ewan sets the project brief, supplies source materials and directs revisions. Scripts support data processing, model integration, geometry checks and exports. Source, estimate and review layers keep the evidence separate. Shared materials, official mapping and third-party datasets retain their credits in [Sources & credits](SOURCES.md). This portfolio does not claim sole authorship of those inputs or independent manual modeling.

The official openNURBS 7 reader kernel checked all 101 final model files. Native file-opening and display checks used Rhino 8. No Rhino 7 desktop test took place. The 9 October hash review did not rerun geometry or performance tests. The 14 October captures add presentation views only.

## Reading the evidence

This repository publishes a visual case study. Native models, ZIP packages, computer-aided design (CAD) files and GIS geometry remain local. Raw data, machine-specific scripts and full working logs also remain local. Public summaries omit local paths and personal identifiers. Ewan is the public byline.

Official plan geometry supports the transport layout. Vertical profiles, deck thicknesses and supports include estimates. The C06 boundary bridge and Tin Shui Wai station retain unresolved height relationships. Read the [specific limitations](docs/terrain-and-transport.md#known-limitations) before interpreting those views.

- [Model and preview methods](docs/model-and-preview.md)
- [Performance conditions and results](docs/model-performance.md)
- [Validation narrative](docs/validation.md)
- [Structured summary](evidence/summary.json)
- [Image provenance and hashes](evidence/image-manifest.json)
- [Sources, attribution and reuse](SOURCES.md)
