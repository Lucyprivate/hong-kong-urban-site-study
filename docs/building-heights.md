# Building heights with explicit evidence classes

[Back to the project](../README.md)

The 21 September height-enrichment stage began with **23,625 source parts without usable heights**. It added height representation to 4,511 parts while leaving 19,114 unresolved parts as footprints. These are stage-specific source-part counts, not a count of individual buildings in the latest model.

![A matched comparison of height additions](../images/building-heights-before-after.png)
*The same 600 × 600 m window, camera and ground geometry. Black additions identify 180 parts in this view: 175 historic LiDAR estimates and five official roofs combined with LiDAR ground estimates. This image is a data-generated line preview.*

## Evidence hierarchy

| Method | Accepted parts | Interpretation |
|---|---:|---|
| Current official height attributes | 1 | Official attributes supplied both base and top |
| Official roof + historic LiDAR ground | 213 | Roof evidence is official; the derived relative height still depends on an estimated ground surface |
| Historic LiDAR surface and terrain | 4,289 | Estimates from the 2019–2020 survey, not proof of current height |
| GBA predicted height + supporting LiDAR | 8 | Low-confidence statistical estimates under conservative matching rules |
| Unresolved | 19,114 | Original footprint representation retained |

The source workflow used nominal 5 m floating-point DSM/DTM mirror tiles, with a projected grid spacing of approximately 4.777 m, after the original 0.5 m bulk download could not be validated. It did not extract elevations from coloured map imagery.

For historic LiDAR estimates, the representative roof was the DSM 70th percentile inside an inset footprint and the base was the DTM median at aligned sample locations. Rules included at least four native samples, 90% valid coverage and conservative checks for roof coherence, ground variation and source dates. Open-sided structures received representative roof surfaces and perimeter lines without invented enclosing walls.

## Keep disagreement visible

Of the 4,511 accepted additions, **4,494 were displayed by default** and 17 severe terrain conflicts were retained for hidden review. Another 83 contextual mismatches above the reporting tolerance remained visible. These numbers describe this height-enrichment stage; later integration can alter the object and footprint inventory.

Cross-checks against known-height TS and OS source classes gave mean absolute differences of approximately 0.80 m for 246 and 66 qualifying parts respectively. This is a cross-date, cross-source comparison, **not an independent survey accuracy assessment**. Known heights were not fitted to these results or replaced by them.

Historical surfaces can predate redevelopment, small roofs can lack enough samples, and a coarse terrain surface can conflict with local structures. Such uncertainty is retained in the decision record rather than resolved through a default storey height.

See [Sources & credits](../SOURCES.md) for Lands Department building attributes, CEDD survey provenance, mirror services and the GBA study.
