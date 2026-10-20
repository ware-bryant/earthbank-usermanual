# Contributing U-Pb(-Th) Geochronology Data

EarthBank accepts U-Pb(-Th) data from Thermal Ionisation Mass Spectrometry (TIMS), in-situ Secondary Ion Mass Spectrometry (SIMS/SHRIMP), and in-situ Laser Ablation ICP-MS (LA-ICP-MS, LA-MC-ICP-MS), each with its own bulk-upload template.

Get there via **Data** → **Analytical Data** → **U-Pb**.

There are two upload routes: manual entry (slow, error-prone — least recommended) or bulk upload via Excel templates, Excel Wizards, CSV importers, or third-party uploaders (e.g. SQUID 3) — the recommended route.

!!! note
    Data can only be uploaded to an existing sample belonging to an existing Data Package — see [Sample Metadata](sample-metadata.md) and [Data Packages](data-packages.md).

## Manual entry

1. Click **+ New**, choose the Data Package, then **Create** to start a new U-Pb datapoint.
2. Fill in general info (analytical technique, sample or secondary reference material, sample name), then save.
3. Go to the analytical data tab, and enter the U-Pb data.

Optional but recommended if available:

- Age grouping (e.g. crystallisation age, max deposition age) and calculation method (e.g. weighted mean ²⁰⁶Pb/²³⁸U, concordia age)
- Analytical metadata (instrument model, analytical conditions, calibration strategies)

## Excel Wizard

Several templates are available depending on acquisition method — download the one matching your data from the U-Pb window. Each has three main sheets:

| Sheet | Purpose |
|---|---|
| **UPb Datapoints** | One row per sample (or per secondary reference material, e.g. one row for Temora, one for Mud Tank). Records sample name, mineral analysed, and metadata |
| **UPbSpotDatap** | One row per analysis/spot: concentrations, ratios, dates. Linked to UPb Datapoints via **Key**/**Datapoint Key** |
| **UPbAgeGroup** | Optional — records interpreted *ages* (as opposed to raw dates), where statistical grouping has already been applied. Also linked via **Datapoint Key** |
| Column Descriptions / Lookup Tables | Reference only — don't edit Lookup Tables |

!!! warning
    Don't touch the first 4 rows — the platform reads them on upload.

**Important:** only fill *Sec. Reference Material* for actual reference-material rows — link unknowns to reference material via matching **Batch ID**.

!!! tip "Key / Datapoint Key example"
    For sample `AUS-12` with 30 zircon spots, set **Key** = `AUS-12_A` in UPb Datapoints. Use `AUS-12_A` as the **Datapoint Key** for all 30 rows in UPbSpotDatap, and again for any derived age groups in UPbAgeGroup.

### Uploading

1. Save the template, then drag it into the drop box at the bottom of the U-Pb window (or click to browse).
2. If issues are found, fix and retry; a green prompt means you're clear — click **Proceed**.
3. Choose the destination Data Package, click **Next**.
4. A summary lists each uploaded table (U-Pb datapoints, spot data, age groups). Open each in turn, review/fix any flagged errors or warnings, and confirm — repeat until every table shows a green check and "Successfully Imported".
5. Click the final **Upload Batch** button to finalise.

!!! warning
    Data isn't live until **Upload Batch** is pressed.
