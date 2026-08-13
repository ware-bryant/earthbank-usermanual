# Contributing Thermal History Data

EarthBank stores thermal history model data — predicted results and time-temperature (tT) reconstruction points — from any modelling software, for both single-sample models and multi-sample models (e.g. vertical transects, boreholes). Thermal history data can be linked to existing samples, Fission Track data, (U-Th)/He data, geochemistry data, and U-Pb data, so measured and model-predicted results can be compared directly.

Get there via **Data** → **Analytical Data** → **Thermal History**. As elsewhere, you can build a model manually or (strongly recommended) bulk-upload via Excel.

## Model-by-model (manual) entry

1. Click **+ New**, choose the Data Package, then **Create**.
2. Work through the tabs: **General**, **tT Sample**, **tT Input**, **tT Model Constraint**, **tT Path** (unique to this data model), plus the platform-wide **More** and **Files** tabs.

### General tab

Define the model set-up: software used, approach, iterations, starting temperature gradient.

### tT Sample tab

Click **+ New** to link the model to a sample. Give it a **Name** — a unique identifier, ideally related to the sample name (e.g. sample `T1-05` → name `T1-05-model`). This name is used to reference the model in later tabs.

### tT Input tab

Click **+ New** to add a **THistInput** datapoint. Set **Thermal History** to the name from the previous tab. Fill in the constraint fields as applicable, and enter the model-predicted results (age, track length, or reflectance) at the bottom — if measured Fission Track or (U-Th)/He data for the sample is already on the platform, this lets it be compared directly against the model. Repeat **+ New** for additional inputs if the model uses multiple data types as constraints.

### tT Model Constraint tab

Click **+ New** to define a time-temperature constraint box (mean and range of both time and temperature), with a **Constraint Type** dropdown. Repeat for multiple constraints — e.g. a present-day constraint is set as time = 0, range = 0, with Constraint Type = *Present-day*.

### tT Path tab

Click **+ New** to add a **THistNickpoint** — a point in time-temperature space along the model path. Since most modelling software doesn't export path data directly, points usually need digitising from a figure first (the team recommends [WebPlotDigitizer](https://automeris.io/WebPlotDigitizer/)). For more than a couple of points, use the CSV batch option instead: expand **Batch Edit** to download/upload a CSV, where **datapointName** must exactly match the name set in the tT Sample tab.

!!! tip
    Adding path points one at a time is slow — use the bulk Excel uploader below for anything beyond a trivial model.

### More & Files tabs

Same pattern as elsewhere.

Once complete, return to the General tab and save.

## Bulk upload (Excel Wizard)

Two templates are available at the bottom of the Thermal History window:

- **`THDatapoint_SingleSample.template.xlsx`** — single-sample models only
- **`THDatapoint_MultiSample.template.xlsx`** — single- or multi-sample models (has extra fields; use only when you actually need multi-sample support)

Either template can carry multiple models in one file — no need for a separate upload per model iteration.

!!! tip "Key / Datapoint Key"
    The **Key** is set in the **tT Model Setup** sheet, uniquely identifying a sample and/or model iteration (e.g. `FT-102-model`). Every related row in the other sheets repeats that value as **Datapoint Key**. For multi-sample models, use a generic key for the model as a whole (e.g. `model_transect_A`), repeated across all the samples that belong to it.

### Single-sample template

Four sheets:

| Sheet | Purpose |
|---|---|
| **tT Model Setup** | Model metadata, starting parameters, and the **Key** |
| **tT InputOutput** | Data used to constrain the model, and the model's predicted age/track length/reflectance output; links to existing sample data already on the platform |
| **tT Model Constraint** | Time-temperature constraint box(es) — mean and range of time and temperature; present-day constraint uses time = 0, range = 0, Constraint Type = *Present-day* |
| **tT Path** | The digitised time-temperature path points (see WebPlotDigitizer note above) |

### Multi-sample template

Same four sheets, plus:

| Sheet | Purpose |
|---|---|
| **tT Sample** | Links multiple samples to one model — one row per sample, **Datapoint Key** matching the model's **Key** |

The remaining sheets work as in the single-sample template, except **tT Path** additionally records which sample each path belongs to, and **tT InputOutput** may have multiple constraint rows per sample — keep Datapoint Keys (and Sample Names, where multiple constraints share a sample) matched carefully.

!!! warning
    Don't touch the first 4 rows of either template — the platform reads them on upload.

### Uploading

1. Save the completed template, drag it into the drop box at the bottom of the Thermal History window (or click to browse).
2. Fix any flagged issues (missing headers, unlinked Keys), then click **Proceed**.
3. Choose the destination Data Package, click **Next** (or **Cancel** to edit the file directly).
4. Step through the wizard's 3 validation steps, then click **Upload Batch** to finalise.

[SCREENSHOT: Thermal history bulk upload validation steps]

!!! warning
    Data isn't live until **Upload Batch** is pressed.
