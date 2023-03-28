###### [Archivematica Manual](../README.md) `|` [Ingest Guidelines](overview.md)
###### Start a Transfer `|` [Decision Points](decision-points.md) `|` [Update AIS](update-ais.md) `|` [Errors](errors.md)

# Start a Transfer
This page describes how to start an ingest project on the `Transfer` tab.
- For guidance on the `Backlog` and `Appraisal` tabs see the [Appraisal page](appraisal.md) in this section of the Manual.

The microservices on the `Transfer` tab will transform the `transfer package` into an Archivematica `SIP` (Submission Information Package) which in turn the microservices of the `Ingest` tab will transform into an `AIP` (Archival Information Package).

**Contents:**
- [Transfer type](#transfer-type)
- [Transfer name](#transfer-name)
- [Accession number](#accession-number)
- [Access system ID](#access-system-id)
- [Browse button](#browse-button)
- [Approve automatically checkbox](#approve-automatically-checkbox)
- [Select processing configuration](#select-processing-configuration)

## Transfer type
Select the `Transfer type` from the drop-down menu. See [Archivematica documentation here (v1.13)](https://www.archivematica.org/en/docs/archivematica-1.13/user-manual/transfer/transfer/#transfer-types) for more detail.

`Standard`
- Default and the one most commonly used by the Archives.
- Use for any transfer that is not one of the other more specific types.
- If in doubt, use `Standard`.

`Zipped directory`
- Use for a set of directories that has zipped into a single file.
- Generally not used by SFU Archives: prefer to upload unzipped transfer packages.

`Bag`
- A `bag` is a `transfer package` structured according to the [BagIt specification](https://datatracker.ietf.org/doc/html/rfc8493) and can be zipped or unzipped.
- The Archives' digital transfer workflow encourages the use of SFU MoveIt, a packager that creates `bags`.
- In this workflow, an archivist validates the transfer and re-bags it with accession and validation metadata.
- Always upload validated `bags` in **unzipped** form (`Transfer type` = "Unzipped bag").

`Disk image`
- The Archives has little experience working with disk images in Archivematica, but see [Disk Imaging](../pre-ingest-actions/disk-imaging.md) for more detail.

`Dspace` and `Dataverse`
- Not used; the Archives does not create these types of `transfer package`.

## Transfer name
The basic naming convention for transfers is:

```
AccessionNumber_CreatorName_ContentDescriptor
ACNYYYY-NNN_Name_Descriptor

E.g.
ACN2016-041_Education_CourseOutlines
```

Past practice has been inconsistent, and even now it is not critical to always follow the convention.
- It is mainly useful for transfers that will be processed through Archivematica as `backlog AIPs` that will sit in storage awaiting further appraisal, selection, and arrangement in the future (see [Processing Backlog](../ingest-scenarios/processing-backlog.md)).
- The main goal is to provide a name that allows quick comprehension of its provenance and content; but it will be registered in the AIS with fuller descriptive detail there if needed (see [Update AIS](update-the-ais.md)).
- Transfers that will be split up into multiple SIPs on the `Appraisal` tab will in any case no longer follow the convention.

## Accession number
Enter the `Accession no.` field with the AIS `Accession number` in the form `YYYY-NNN`.
- Do not use the "ACN" prefix as in the `Transfer name`.
- See [Pre-ingest actions > Accessioning](../pre-ingest-actions/accessioning.md) for more information.

## Access system ID
Enter the url slug of the parent AtoM description if applicable. This will typically be in the form of a `file reference code` = `f-x-x-x-x-x`.

**Enter only if you intend to directly upload the DIP to AtoM as part of your current ingest session.**
- Entering the slug ID will save you having to manually enter this later in the workflow on the `Ingest` tab.
- Leave blank if not applicable or if you are sending the transfer through as a `backlog AIP`.

## Browse button
Click to view / select available `transfer packages` currently on `staging server`.
- Click a folder to browse its contents.
- You cannot select individual files (shown with strike-through grey text), only folders.
- Click the `Add` button to select.
- You can add multiple selections.

## Approve automatically checkbox
Leave the `Approve automatically` box CHECKED.

## Select processing configuration
You can process the transfer with either the default [standard processing configuration](../processing-configurations/standard.md) or with a custom one.
- To use the standard configuration, just click the green `Start transfer` button.
- Click the drop-down arrow to view and select a custom processing configurations.
- Custom configurations are described on the [Processing configurations overview page](../processing-configurations/overview.md).

---
###### Last updated: Jan 26, 2022
