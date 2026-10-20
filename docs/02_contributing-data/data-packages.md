# Data Packages

To upload data, first upgrade your account from General User to Data Contributor — see [Registration & Accounts](../00_getting-started/registration-and-accounts.md).

## Why Data Packages exist

All data in EarthBank is uploaded in a structured, relational way so it can be queried, synthesised, and visualised on the fly. Sample metadata, Fission Track data, and every other data type are each uploaded through their own template and drag-and-drop box, but they all attach back to samples grouped under a **Data Package** — the organising unit for a dataset. Keeping data structured this way also makes it possible to link new analytical data to samples already on the platform.

## Creating a Data Package

1. In the title bar, open **Data**, then select **Data Packages** from the left-hand menu.
2. Click **+ New** (top right corner).
3. Enter a name and click **Save** — you'll land on the Data Package's property setup page.

From here you can set package information, add team members, attach files/images, and mint a DOI ([DOI Minting](doi-minting.md)).

## Package information

On the **Package Info** tab, set:

- **Name** and **Description** — the description appears on the map when hovering over the Data Package's info icon
- **Distribution** — Public or Private (see below)
- **Workflow State** — In Progress, Finished, or Frozen (see below)
- **License**

## Data privacy control

Distribution controls who can see a Data Package's data:

- **Public** — visible to the whole EarthBank community
- **Private** — visible only to designated Team Members (see below), for a limited embargo period

EarthBank is designed as an open repository, so Private data defaults to a **two-year** embargo from upload date. Data already in the public domain (e.g. published in a journal) must be uploaded as Public.

Before the two-year embargo ends, you'll be notified that the data will automatically switch to Public. At that point you can request a **one-year extension**, granted automatically, and a further extension after that (four years total). After four years, any data still Private is made Public automatically.

You can also switch a package to Public manually at any time: open **Data Packages**, click the package's overflow menu, open the **Package Info** tab, select **Public** from the Distribution dropdown, and save.

## DOI workflow state

Also on the Package Info tab, the Data Contributor (and anyone added as a Supervisor) can set the **Workflow State**:

| State | Meaning |
|---|---|
| In Progress | Editors can still edit datapoints in the package |
| Finished | Datapoints can no longer be edited |
| Frozen | The package can no longer be changed at all. **Cannot be undone.** Only use once a package is DOI-minted and published |

!!! warning
    Do not set a Data Package to **Frozen** before publication.

## Team members

On the **Team** tab, add collaborators as Team Members so they can view and edit the Data Package — useful for shared research projects.

## Attaching files

On the **Files** tab, either create a folder and upload a batch of images/files, or upload directly via the upload icon. Files can be downloaded or deleted at any time from the same tab.
