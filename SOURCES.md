# Sources, credits and reuse

## Project context and contribution

Ewan supplies the project brief and source materials, and directs revisions. Scripts support analysis, geometry integration, checks and documentation. Shared materials and third-party data retain their original rights. This portfolio does not claim sole authorship of those inputs or independent manual modeling. Public files omit other contributors' personal identifiers and identifying source filenames.

Rhino images are local project outputs. The height comparison is a data-generated line preview. The urban tissue overview is an atlas page. The [image index](images/README.md) identifies each stage.

The initial **9 October 2026** update added the 8 October gray-terrain benchmark, D05 tile and assembly index. The benchmark uses isolated, controlled Shaded settings. D05 uses Line drawing style. The index is a composed guide, not a native capture. The update compared file hashes with the final delivery record. It did not rerun geometry or performance tests or change display preferences.

A later **9 October** review opened the master in the local **Rhino 8.6 GUI**. It selected a full-site view and urban-river detail in existing Line drawing style. Native **ViewCaptureToFile** exports used **2400 × 1230**. A post-capture hash check matched the source model. No changes were saved to it.

The **14 October 2026** presentation views use the same final master and local Rhino 8.6 GUI. Native ViewCaptureToFile exports with Line drawing style use **3840 × 1968**. No changes were saved to the source model. These views add no benchmark samples or geometry tests. The [image manifest](evidence/image-manifest.json) records capture sources and image identities.

## Source register

Dataset update dates, extraction dates and observation dates have different meanings.

| Source | Project use | Limit |
|---|---|---|
| Lands Department HP1C sheets, supplied mosaic | c.1999–2000 map interpretation. 207 editions | Missing coverage does not prove empty land |
| Supplied Lands Department iB1000 extraction, 14 August 2026 | Building/structure and urban-tissue context | Extraction date is not a shared survey date |
| [iB5000 metadata][ib5000] and [dictionary][ib5000-dict] | Rail, road and coastline interpretation. iB50000 fills a coastline gap | Plan location and layer order do not establish full vertical profiles |
| [Official building attributes][buildings] | Building attributes and identity checks | Roof elevation and relative height need suitable base evidence |
| [CEDD 2019–2020 LiDAR][lidar] | Historical surface and ground evidence | Historical survey does not establish current building height |
| Esri China (Hong Kong) / HKGeodata [DSM][dsm] and [DTM][dtm] mirrors | Nominal 5 m floating-point tiles for height estimates | The original 0.5 m bulk download remained unvalidated and unused |
| [GBA height study][gba], Earth System Science Data 17 (2025) | Eight predicted-height additions with conservative matching | Statistical 2018/2019-era estimates. Heights: CC BY-NC 4.0. Footprints: ODbL |
| Supplied official RoadCentreline, 2025-09-01 edition | Independent road alignment context | Record updates are not construction dates |
| Supplied terrain and secondary context layers | Shared relief and contextual comparisons | Some dates and vertical metadata are unknown. Secondary layers do not independently establish change |
| [West Rail report][west-rail], May 2020, and [Hung Shui Kiu EIA][hsk] | Transport context | These references do not establish a full surveyed 3D reconstruction |
| [OpenStreetMap contributors][osm], retrieved 24 September 2026 | Extra bridge and context references | Completeness and update dates vary |

CEDD means Civil Engineering and Development Department. LiDAR means light detection and ranging. DSM and DTM mean digital surface model and digital terrain model. GBA means Greater Bay Area. EIA means environmental impact assessment. ODbL means Open Database License.

Government data credit: Lands Department and Civil Engineering and Development Department, Hong Kong SAR Government. Other data and documents retain their providers' credits. No government or provider endorsement is implied.

[ib5000]: https://portal.csdi.gov.hk/csdi-webpage/metadata/landsd_rcd_1637224243141_96556/html
[ib5000-dict]: https://open.hkmapservice.gov.hk/OpenData/opendata_static/resources/resources_iB5000_FGDB.zip
[buildings]: https://portal.csdi.gov.hk/csdi-webpage/dataset/landsd_rcd_1637211194312_35158
[lidar]: https://portal.csdi.gov.hk/csdi-webpage/dataset/cedd_rcd_1629267205233_87895
[dsm]: https://www.arcgis.com/home/item.html?id=aec73d5d4dbe4c599c93b5d3070b6e10
[dtm]: https://www.arcgis.com/home/item.html?id=88ba826def794c19bab247011726f7c5
[gba]: https://doi.org/10.5194/essd-17-6647-2025
[west-rail]: https://www.epd.gov.hk/eia/files/applications/en/pp_694/vep_4152/progress/action_9052/emar202005.pdf
[hsk]: https://www.epd.gov.hk/eia/files/applications/en/pp_291/eia_1886/progress/action_1883/EIA/Text/HTML/02%20Project%20Description%20and%20Consideration%20of%20Alternatives.htm
[osm]: https://www.openstreetmap.org/copyright

## Scope of public release

The repository publishes a visual case study and selected validation summaries. Rhino models, CAD files, GIS layers, map mosaics, elevation tiles, archives and detailed source geometry remain local.

No blanket open-source or open-data license applies to these mixed sources. Third-party rights and original terms still apply. This publication grants no right to redistribute underlying datasets. Get source data and current terms from the linked providers. A citation of this case study must credit **Ewan** and keep the relevant data attribution and uncertainty notes.
