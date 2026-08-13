# The Map Window

The global geospatial database can be explored much like Google Maps: click and drag to pan, use the on-screen +/- buttons, the scroll wheel, or a trackpad pinch to zoom, and hold **Ctrl** while dragging to change the viewing angle.

Click a sample locality to retrieve that sample's metadata and geochemical data. To view and synthesise several samples at once, use the **Select Area** tool (below). Selecting one or more samples opens a data pop-up with a dropdown for switching between data dashboards — synthetic plots, detailed tables, and a list of associated references, all downloadable.

General Users can view, analyse, and synthesise sample metadata and geochemistry data from the Map window using the toolbar on the left-hand side:

[SCREENSHOT: Map window with left-hand toolbar labelled]

## Toolbar tools

**Data Packages** — view, hide, or add Data Packages to the map.

**Analytical Layers** — filter samples by data type (*Samples, Geochemistry, Geochronology, Thermochronology*). The toolbar options change depending on which layer is active.

**Basemaps** — switch between satellite, streets, dark/light themes, topography, bathymetry, and geology, plus Australia-specific overlays (magnetics, gravity, U/Th/K concentrations, soil depth, acid sulphate soils). Any base layer can be shown with or without contour lines.

**Select Area** — select multiple data points within a region, three ways:

- **Polygon select**: click multiple points, then click the first point again (or double-click) to close the shape.
- **Square select**: click a start point and drag to size, then click again to complete.
- **Multi-select**: as square select, but hold **Shift** and repeat to define several separate square areas at once.

**Go to location** — jump to a specific latitude/longitude.

**Find** — search by sample ID, rock or mineral type, or analysed mineral.

**Paleo Reconstructions** — view samples in a paleogeographic context. Activating this tool switches the Map window to a paleogeographic basemap with its own toolbar across the top. Available reconstruction models are chosen from a dropdown on the right of that toolbar; a scroll bar at the top toggles the reconstruction age. Some models support a paleotopography overlay; enabling it displays only samples with age information and filters out analytical data younger than the reconstruction age. An interactive present-day pop-up shows where the displayed samples actually sit today, for easy navigation regardless of reconstruction age. The Contour Data and Swath Profile tools, and all filters, continue to work while Paleo Reconstruction is active.

[SCREENSHOT: Paleo Reconstruction toolbar with model dropdown and age scroll bar]

**Contour Data** — produce a contour profile for a region, based on elevation or any available analytical data. Follow the prompts in the tool's pop-up window.

**Swath Profile** — investigate the relationship between a selected attribute and topography along a transect. After activating the tool, set the profile width, then click two points on the map to define the transect. Drag the larger of the two green circles to adjust the angle. Click **Draw** in the pop-up to generate the profile (re-click Draw after any change to refresh it); adjust width with the +/- controls; choose the attribute to colour by (e.g. *Age*, *Fission Track Length*) from the dropdown at the bottom left of the profile window; export the profile as an SVG at any time.

[SCREENSHOT: Swath Profile transect and resulting profile plot]

**Map View / Global View** — toggle between a flat map and a 3D globe.

## Filter pop-ups

Several toolbar buttons open a filter pop-up on the right side of the Map window. Most support colouring samples by a chosen attribute (via a palette/gradient control) as well as filtering:

| Filter | Available when | What it does |
|---|---|---|
| Location Type | Always | Filter/colour by sampling location (*Outcrop, Boulder, Section, Mine, Borehole*, etc.) via toggles |
| Rock Type | Always | Filter/colour by rock type (*Igneous, Sedimentary, Metamorphic, Ore, Meteorite*) via toggles |
| Elevation | Always | Filter by elevation (–8500 m to 10000 m) via sliders |
| Oxide | Geochemistry layer | Filter by oxide concentration via sliders; colour-code by a chosen oxide; option to show out-of-range samples as grey outlines |
| Element | Geochemistry layer | Filter by trace element concentration via sliders; colour-code by a chosen element; same grey-outline option |
| Analysis Scale | Geochemistry or Geochronology layer | Filter/colour by analytical scale (*Whole Rock, Multi-Grain Aliquot, Single Grain, Spot*) |
| Mineral | Geochemistry layer | Filter/colour by analysed mineral (*Apatite, Titanite, Zircon*, etc.) |
| Analysis Type | U-Pb Geochronology layer | Filter/colour by analytical method |
| Age | Thermochronology or Geochronology layer | Colour by measured age (central/pooled age for Fission Track, FT-corrected age for (U-Th)/He), on a geologic-time-scale colour bar; slider filters the age range |
| IQR | (U-Th)/He Thermochronology layer | Colour by interquartile range of single-grain ages — a dispersion indicator where low IQR implies less scatter |
| Technique | Fission Track Thermochronology layer | Filter/colour by measurement technique |
| Track Length | Fission Track Thermochronology layer | Colour by mean track length (MTL, µm); slider filters the range |
| Track Length σ | Fission Track Thermochronology layer | Colour by 1σ standard deviation of MTL; slider filters unimodal vs. broad/bimodal distributions |

[SCREENSHOT: example filter pop-up, e.g. Oxide filter with concentration sliders]
