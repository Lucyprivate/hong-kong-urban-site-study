# Sources, credits and reuse

## Project context and contribution

Public portfolio by **Ewan**, developed from Group 4 coursework materials supplied for the ongoing urban site study. Codex assisted with analysis, scripts, geometry integration, validation and documentation. Shared coursework and third-party source material are not claimed as Ewan's sole original work. Other students' personal names, student numbers and source filenames containing personal identifiers are omitted from this public snapshot.

Rhino images are local project outputs. The height before/after plate is a data-generated line preview; the urban tissue overview is an atlas page. Each image's stage is listed in [the image index](images/README.md).

## Source register

These references document the sources recorded in the project. Dataset update dates, extraction dates and observation dates are different concepts.

| Source | Role in this project | Important limit |
|---|---|---|
| Lands Department HP1C historical sheets, supplied Group 4 mosaic | c.1999–2000 map interpretation; 207 sheet editions | Historical coverage is incomplete; blanks do not prove empty land |
| Supplied Lands Department iB1000 extraction, 14 August 2026 | Current building/structure and urban-tissue context | Compilation/extraction date is not a common survey date |
| [Lands Department iB5000 metadata](https://portal.csdi.gov.hk/csdi-webpage/metadata/landsd_rcd_1637224243141_96556/html) and [data dictionary](https://open.hkmapservice.gov.hk/OpenData/opendata_static/resources/resources_iB5000_FGDB.zip) | Official rail, road, coastline and related feature interpretation; iB50000 used for a coastline gap | Plan location and layer order do not supply complete vertical profiles |
| [Lands Department building dataset](https://portal.csdi.gov.hk/csdi-webpage/dataset/landsd_rcd_1637211194312_35158) | Official building attributes and identity checks | Roof elevation and relative height require appropriate base information |
| [CEDD 2019–2020 LiDAR dataset](https://portal.csdi.gov.hk/csdi-webpage/dataset/cedd_rcd_1629267205233_87895) | Historical surface/ground evidence | Historic survey cannot establish a building's current height |
| Esri China (Hong Kong) / HKGeodata [DSM mirror](https://www.arcgis.com/home/item.html?id=aec73d5d4dbe4c599c93b5d3070b6e10) and [DTM mirror](https://www.arcgis.com/home/item.html?id=88ba826def794c19bab247011726f7c5) | Nominal 5 m floating-point tiles used for height estimates | The original 0.5 m bulk download was not successfully validated; it was not used |
| [GBA building-height study, Earth System Science Data 17 (2025)](https://doi.org/10.5194/essd-17-6647-2025) | Eight conservatively matched predicted-height additions | Statistical 2018/2019-era height estimates; height data recorded as CC BY-NC 4.0 and footprint data as ODbL |
| Supplied official RoadCentreline 2025-09-01 edition | Independent road alignment context | Record updates are not construction dates |
| Supplied terrain and secondary Group 4 / peer coursework layers | Shared relief and contextual comparison | Some dates and vertical metadata remain unknown; secondary layers do not independently establish change |
| [EPD West Rail monitoring report, May 2020](https://www.epd.gov.hk/eia/files/applications/en/pp_694/vep_4152/progress/action_9052/emar202005.pdf) and [Hung Shui Kiu EIA project description](https://www.epd.gov.hk/eia/files/applications/en/pp_291/eia_1886/progress/action_1883/EIA/Text/HTML/02%20Project%20Description%20and%20Consideration%20of%20Alternatives.htm) | Transport context and cross-reference | Contextual evidence does not provide a complete surveyed 3D reconstruction |
| [OpenStreetMap contributors](https://www.openstreetmap.org/copyright), project retrieval 24 September 2026 | Supplementary bridge/context cross-reference | Community mapping has variable completeness and update dates |

Government mapping/data credit: Lands Department and Civil Engineering and Development Department, Hong Kong SAR Government. Other data and referenced documents remain attributable to their respective providers. No government or provider endorsement is implied.

## Scope of public release

This repository distributes a curated visual case study and derived validation summaries. It does not distribute the Rhino models, CAD files, source GIS layers, historical map mosaics, elevation tiles, working archives or detailed source geometry embedded in audit logs.

No blanket open-source or open-data licence is applied to these mixed-source materials. Third-party rights and their original terms continue to apply; this portfolio publication does not grant permission to redistribute the underlying datasets. Use the linked providers to obtain source data and its current terms. Referencing this work as a portfolio case study should credit **Ewan** and retain the relevant dataset attribution and uncertainty notes.
