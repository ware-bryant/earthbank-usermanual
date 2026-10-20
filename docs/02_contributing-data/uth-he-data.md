# Contributing (U-Th)/He Data

EarthBank handles both whole-grain and in-situ (U-Th)/He data from virtually any mineral. As with other data types, upload sample-by-sample (manual) or in bulk via the Excel Wizard — bulk is recommended for complex, multi-sample datasets.

Get there via **Data** → **Analytical Data** → **(U-Th)/He**, then use **+ New** to create data or the upload options at the bottom of the window.

## Manual entry

1. Click **+ New**, choose the Data Package, then **Create**.
2. Work through the tabs below.

### The Datapoint tab

Covers the sample as a whole (not a single grain): sample name, sample type, mineral analysed, number of aliquots, measured mean data. Save changes with the confirm button in the lower left before moving on. Start by marking the sample as **unknown** or **reference material** (e.g. Durango apatite, Fish Canyon zircon).

!!! tip "Batch ID"
    The **Batch ID** links unknown samples to the reference material measured alongside them — matching Batch IDs are treated as belonging together (equivalent to *Session ID* in the LA-ICP-MS data model).

Hover the info icon on any field for more detail. Once complete, continue to Analytical Metadata.

### Analytical Metadata tab

Choose whether the analysis was whole-grain or in-situ — this shows/hides the relevant fields. All fields are predefined dropdowns; if an option you need is missing, use **Help → Contact Us** in the title bar to flag it.

### Whole-Grain Analysis / In-Situ Analysis tab

Click **+ New** (within the relevant tab) to add a single-grain or multi-grain aliquot — a pop-up opens with fields including measured age, uncertainty, FT correction, and grain dimensions. Not all fields are required. Repeat **+ New** for each additional aliquot.

### More & Files tabs

**More** links the datapoint to other platform entities — a collaborating user, a publication, etc. **Files** accepts anything that doesn't fit a predefined field: raw data, grain images, drawings, figures.

Once done, return to the Datapoint tab and save — the new data appears in the (U-Th)/He list and on the Map window.

## Excel Wizard (bulk upload)

Best for datasets with multiple samples and multiple aliquots each. At the bottom of the (U-Th)/He window, choose the **Excel Wizard** or **.CSV uploader** option (Excel Wizard recommended) and download the blank `.XLSX` template.

| Sheet | Purpose |
|---|---|
| **He Datapoints** | One row per sample. For a reference standard, select it via the *Sec. Reference Material* dropdown; link to unknowns via matching **Batch ID** |
| **HeWholeGrain** / **HeInSitu** | Metadata and calculated mean values, plus per-aliquot results. Both can be used in the same file if you have both data types |
| Column Descriptions / Lookup Tables | Reference only |

!!! warning
    Don't touch the first 4 rows — the platform reads them on upload.

**Important:** *Sec. Reference Material* is only for measured secondary reference material rows, not the reference material used during instrument calibration. Link unknowns to reference results via **Batch ID**.

!!! tip "Key / Datapoint Key example"
    For sample `HeVic-12` with 5 whole-grain results, set **Key** = `HeVic-12_A` in He Datapoints, then repeat `HeVic-12_A` as the **Datapoint Key** for each of the 5 rows in HeWholeGrain.

### Uploading

1. Save the template, drag it into the drop box (or click to browse).
2. The platform flags issues (missing headers, unlinked Keys) if any — fix and retry.
3. Choose the destination Data Package, click **Next** (or **Cancel** to go back and edit the file directly).
4. Step through the wizard's 3 validation steps, then click **Upload Batch** to finalise.

!!! warning
    Data isn't live until **Upload Batch** is pressed.
