# Contributing Major & Trace Geochemistry Data

Major and trace geochemistry data can be added by manual entry or, for anything but the smallest datasets, via the Excel Wizard (recommended — manual entry is slow and error-prone at scale).

Get there via **Data** → **Analytical Data** → **Geochemistry**.

## Manual entry

1. Click **+ New** to create an inorganic geochemistry datapoint, choose the Data Package, then **Create**.
2. Fill in general datapoint info (analytical technique, mineral analysed, sample name), then save.
3. Go to the analytical data tab and enter the U-Pb-style analytical data.

The following are optional but recommended where available:

1. Intra-sample/aliquot details (grain/aliquot ID, spot ID, grain domain, total wt% of analysis)
2. Oxide concentrations and uncertainty per aliquot/grain/spot
3. Element concentrations, uncertainty, and measured mass per aliquot/grain/spot

## Excel Wizard

Download the blank **GCDatapoint** template from the drag-and-drop box at the bottom of the Geochemistry window. It contains:

| Sheet | Purpose |
|---|---|
| **GC Datapoints** | One row per sample (or per secondary reference material — use the *Sec. Reference Material* column for those, one row each). Records sample name, mineral analysed, and metadata (analytical method, lab, analyst) |
| **GC Concentrations** | One row per analysis/spot: concentrations, uncertainties, measured masses. Linked back to GC Datapoints via the **Key**/**Datapoint Key** pair |
| **Column Descriptions** | Reference only |
| **Lookup Tables** | Backing lists — don't edit |

!!! warning
    Red columns are required. Other columns can be reordered or deleted. Don't touch the first 4 rows.

!!! tip "Key / Datapoint Key"
    The **Key** (set in GC Datapoints) is a unique value you assign per sample or reference material. Every related row in GC Concentrations repeats that same value in its **Datapoint Key** column, linking spot/grain-level data back to the sample.

**Important:** only fill *Sec. Reference Material* for actual reference-material rows — link unknowns to reference material via matching **Analytical ID**, not this column.

### Detection limits

Below a known numerical detection limit: prefix the value with `<` (e.g. `<0.01`). Below an unspecified limit: enter just `<`.

### Uploading

1. Save the completed template, then drag it into the drop box on the Geochemistry window (or click to browse).
2. Choose the destination Data Package.
3. Step through the validation windows left to right — each flags **Errors** (block upload until fixed) and **Warnings** (should be reviewed).
4. Once every window is clear, click **Upload**.
5. Click the final confirmation button to finalise the import.

!!! warning
    Data isn't live until you click the final **Upload Batch** button.
