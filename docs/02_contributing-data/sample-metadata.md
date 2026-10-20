# Contributing Sample Metadata

Sample metadata can be added one sample at a time, or in bulk via an Excel template. For anything beyond a handful of samples, use the Excel Wizard.

## Manual entry (individual samples)

1. In the title bar, open **Data**, select **Samples** from the left-hand menu, then click **+ New** (top right).
2. Enter the **Sample Name**, choose the **Data Package** it belongs to (create one first if needed — see [Data Packages](data-packages.md)), and continue.
3. Work through the tabs below, saving between each.

### Sample tab

| Field | Notes |
|---|---|
| Sample Name | — |
| Data Package | Must already exist |
| Stratigraphic Unit | Dropdown, or add a new one via the **+** icon |
| Sample Kind | Dropdown |
| Sampling Method | Dropdown |
| Rock/Mineral | Dropdown, backed by mindat.org |
| Sample Age [Ma] | Single value or range |
| Collection date | Single value or range |
| Notes on Sample / Notes on Archive | Free text |
| Archive | Current storage location — dropdown, or add new via **+** |
| Tags | User-defined, improve searchability |

### Location tab

| Field | Notes |
|---|---|
| Location Name | — |
| Location Kind | Dropdown |
| Note on Location | Free text |
| Use this location | Pick a point on the interactive map (street or satellite view) |
| Latitude / Longitude | WGS84 |
| Location Accuracy | Estimated |
| Elevation | *On Surface* or *Below Surface*; auto-filled from lat/long if left blank; reference elevation type set under **Advanced elevation** |

### IGSN tab

See [IGSN Minting](igsn-minting.md).

### Metadata links tab

| Field | Notes |
|---|---|
| Involved People | **+ Link Person**, then choose from the dropdown or add a new entry via **+**; role can be added |
| Referenced Literature | **+ Link Literature**, then choose from the dropdown or add via DOI or manually |
| Funding | **+ Link Funding**, then choose from the dropdown or add via **+**; notes optional |
| Properties | Free-form key/value pairs for anything not covered elsewhere, e.g. `colour=brown`, `weight(gram)=34` |

### Files tab

Upload images or related files individually or as a folder.

## Batch upload (Excel Wizard)

For uploading many samples at once:

1. Open **Data**, select **Samples**, scroll to the bottom of the page, and download the **Sample metadata Excel template** from the drag-and-drop box.
2. Fill it in (see below), then drag it back into that same box (or click to browse).

The template has three sheets:

| Sheet | Purpose |
|---|---|
| **Samples** | Enter data here. Required fields are highlighted pink, highly recommended yellow, optional green. The first two rows describe each field |
| **Column Descriptions** | Reference only — column names and definitions. Don't edit |
| **Lookup Tables** | Backing lists for the Samples sheet's dropdowns |

!!! warning
    Don't change the first 4 rows of the template — the platform reads them on upload.

### Upload steps

1. Drop the completed file into the upload box. The platform validates it and shows a prompt — errors must be fixed before continuing (exit via the close icon, fix the file, try again); a green prompt means you're clear to proceed.
2. Choose the destination Data Package.
3. You'll land on a batch-editing table flagging any remaining errors/warnings, sortable by either. Use **set new value in all empty cells** (after selecting one empty cell) to bulk-fill. You can export the table as CSV at any point.
4. Once there are no errors or warnings left, click **Upload**. A success prompt reports how many rows were imported.
5. Click through to finish — the final prompt shows the tag name applied to the imported batch.
