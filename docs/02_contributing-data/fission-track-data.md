# Contributing Fission Track Data

EarthBank curates fission track (FT) age and length data at both the sample and single-grain level, accepting Population Method, EDM, LA-ICP-MS, and ζ-calibration methodologies. As with other data types: manual entry sample-by-sample, or bulk upload via Excel (recommended for multi-sample datasets with many single-grain results).

Get there via **Data** → **Analytical Data** → **Fission Track**.

## Manual entry

1. Click **+ New**, choose the Data Package, then **Create**.
2. Work through the tabs: **Fission Track Datapoint**, **Fission Track Data**, **Single Grain FT Data**, **Length Data** (unique to this data model), plus the platform-wide **More** and **Files** tabs.

### Fission Track Datapoint tab

Mark the sample as **unknown** or **reference material**. The **Batch ID** links unknowns to the reference material measured with them (same convention as (U-Th)/He — see [Contributing (U-Th)/He Data](uth-he-data.md#the-datapoint-tab)). Fields are mostly predefined dropdowns.

### Fission Track Data tab

Multi-grain summary data: number of grains measured, pooled/central age, mean U content, dosimeter used, mean kinetic results. If a dropdown (e.g. Dosimeter) is missing an option you need, use **Help → Contact Us**.

### Single Grain FT Data tab

Add single-grain count data and/or single-grain age data via the relevant radio button and **+ New**, or upload a CSV (separate templates exist for count data and age data — expand **Batch Edit** to download/upload). In each CSV, **DataPointName** must exactly match the sample name set in the Fission Track Datapoint tab.

### Length Data tab

Add track length data via one of two radio-button-selected formats, or by CSV (separate templates for **Individual Track Lengths** and **Binned Lengths** — expand **Batch Edit**). Seven additional summary fields at the top right (mean track length / MTL, total tracks measured, etc.) can be filled even without individual lengths — useful for legacy data reporting only mean results.

### More & Files tabs

Same pattern as elsewhere: **More** links collaborators/publications; **Files** takes raw data, grain images, drawings, or figures.

Once complete, return to the Fission Track Datapoint tab and save.

[SCREENSHOT: Fission Track Datapoint tabs]

## Excel Wizard (bulk upload)

Download the blank `.XLSX` template from the bottom of the Fission Track window.

| Sheet | Purpose |
|---|---|
| **FT Datapoints** | One row per sample; reference-material rows via *Secondary Reference Material* dropdown, linked to unknowns by matching **Batch ID** |
| **FTCountData** | Mean counting data: pooled/central age, grains measured, mean Dpar |
| **FTSingleGrain** | Single-grain counting data: ages, U content |
| **FTLengthData** / **FTBinnedLengthData** | Track length measurements — pick the sheet matching your data format |

!!! warning
    Don't touch the first 4 rows — the platform reads them on upload.

!!! tip "Key / Datapoint Key example"
    For sample `FtNsw-03` with 20 single-grain ages, set **Key** = `FtNsw-03_B` in FT Datapoints, then repeat `FtNsw-03_B` as **Datapoint Key** in FTCountData, FTSingleGrain, and FTLengthData/FTBinnedLengthData.

### Uploading

1. Save the template, drag it into the drop box (or click to browse).
2. Fix any flagged issues (missing headers, unlinked Keys), then click **Proceed**.
3. Choose the destination Data Package, click **Next** (or **Cancel** to edit the file directly).
4. Step through the wizard's 3 validation steps, then click **Upload Batch** to finalise.

!!! warning
    Data isn't live until **Upload Batch** is pressed.
