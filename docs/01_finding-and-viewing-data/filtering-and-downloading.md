# Filtering & Downloading

## Filtering

Samples can be filtered at the Data Package scale or the individual sample scale, both from the Data window.

**Data Package scale** — select **Data Packages** in the left-hand menu. Default filters (*Data Package Name, Kind of Data, Institution, Team Member*) sit at the top of the window; click the filter icon (top right) for additional options (*Distribution, Workflow State, My Team's*). Selected filters appear as fields in the header and can be removed with the × next to each.

**Sample scale** — select **Samples** (filter by metadata) or **Analytical Data** (filter by analytical data) in the left-hand menu. Default filters are *Sample Name, Data Package, Material, Tag*; the filter icon adds *Image, IGSN, Creator, Editor, Sample Method, Archive, Literature, Funding,* and *Person*.

[SCREENSHOT: Samples window with filter panel expanded]

### Filter reference

| Filter | Meaning |
|---|---|
| Package Name | Search for a specific Data Package |
| Kind of Data | Analytical data type (major/trace geochemistry, fission track, U-Pb geochronology, etc.) |
| Institution | Data Contributor's institution |
| Team Member | Collaborator granted access to a Data Package |
| Distribution | Public or Private |
| Workflow State | *In Progress*, *Finished*, or *Frozen* |
| My Team's | Toggle to show only Data Packages you created or are a Team Member of |
| Sample Name | Search for a specific sample name |
| Material | Broad-to-specific classification, e.g. Igneous rock → Granite → zircon |
| Tag | User-entered or auto-added at upload |
| With Images | Toggle samples that include images |
| IGSN | Search by International Generic Sample Number |
| Creator / Editor | Find samples by the researcher who created or edited them |
| Sample Method | e.g. Hand Sample vs. Core |
| Archive | Filter by holding institution |
| Literature | Find samples linked to a specific publication |
| Funding | Find samples collected under a specific funding scheme |
| Person | Search by contributor |

## Downloading

EarthBank supports three download scopes: a whole Data Package, a single sample, or a selection of samples.

**Whole Data Package (ZIP):** in **Data Packages**, click the download icon at the bottom left of the package. A pop-up shows whether a ZIP already exists, its generation date, and whether it's current, with a button to download immediately. The same pop-up's overflow menu lets you generate a fresh ZIP or view ZIP history. If no ZIP has ever been generated, you'll be prompted to create one — you'll get an email when it's ready. The ZIP contains all sample metadata, analytical data, and relevant shapefiles.

[SCREENSHOT: Data Package download pop-up]

**Single sample or selection:** in **Samples** or **Analytical Data**, tick the checkbox next to the sample(s) you want, then use the download button at the top of the window. You can also download the selected samples' shapefile or IGSN QR codes from the same toolbar.

## Data visibility on the map

To control which Data Packages show on the map, go to **Data Packages** in the Data window and toggle the visibility icon at the bottom left of the package. The title bar's map icon blinks as a reminder to switch back to the Map window to see the change.
