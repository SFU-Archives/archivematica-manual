###### [Archivematica Manual](../README.md) `|` [Ingest Guidelines](overview.md)
###### [Start a Transfer](start-transfer.md) `|` Decision Points `| `[Update AIS](update-ais.md) `|` [Appraisal and Selection](appraisal-and-selection.md) `|` [Error Handling](error-handling.md)

# Decision Points
`Decision points` occur when certain microservices in the Archivematica `Dashboard` require the archivist to manually choose an option. This page describes the `decision points` in the [standard processing configuration](../processing-configurations/standard.md).
- For custom configurations that automate some or all microservices, see [Processing Configurations: Overview](../processing-configurations/overview.md).

**Decision points:**
- [Create SIP from Transfer](#create-sip-from-transfer)
- [Normalize](#normalize)
- [Approve normalization](#approve-normalization)
- [Add metadata if desired](#add-metadata-if-desired)
- [File format identification (submission documentation)](#file-format-identification-submission-documentation)
- [Store AIP](#store-aip)
- [Store AIP location](#store-aip-location)
- [Upload DIP](#upload-dip)
- [Store DIP](#store-dip)
- [Store DIP location](#store-dip-location)

## Create SIP from Transfer
Specify what to do with the `SIP` (transfer).

`Create single SIP and continue processing`
- Send the transfer to the `Ingest` tab to continue.
- Use if the transfer does not require any additional appraisal, selection, or arrangement.
- Use if it does require additional processing but you will not be doing this in the immediate future (process through Archivematica to create a [backlog AIP](../ingest-scenarios/processing-backlog-aips.md).

`Send to backlog`
- Send to Archivematica backlog.
- Use this option if you intend to process the transfer in the immediate future (appraise, select, arrange and describe).

`Reject transfer`
- Cancel the ingest process.
- Use if you realize you have a made a mistake and wish to start over.

## Normalize
Specify whether / how to normalize files in the transfer; determines whether Archivematica creates `preservation` and `access copies` in formats that may differ from the original file format.

`Normalize for preservation and access`
- This is the Archives' typical choice.
- If in doubt, choose this option.

`Normalize for preservation`
- Use if you manually created `access copies` prior to ingest (see [Manual Normalization](../pre-ingest-actions/manual-normalization.md)).
- You can also use this option for some formats that currently have no normalization rules for access (e.g. email ingested as `mbox`).

`Normalize for access`
- Can be used if the original files are already in `preservation format` but it is typically better to let Archivematica decide whether file formats do or do not already comply with `preservation formats`.

`Normalize service files for access`
- Use if you manually created `service files` prior to ingest (see [Manual Normalization](../pre-ingest-actions/manual-normalization.md)).
- Generally not used by Archives.

`Normalize manually`
- Use if you want manually normalize the files before continuing.
- Generally not used by Archives: if manual normalization is required, do this prior to ingest.

`Do not normalize`
- Can be used if the files are already know to exist in `preservation` and `access formats` (e.g. outsourced digitization work performed by a vendor).
- Typically it is better to let Archivematica determine this.

`Reject SIP`
- Use if you want to cancel the ingest process.
- E.g. you realize a mistake was made and you wish to fix, then start again.

## Approve normalization
Review the normalization report by clicking the `document icon` next to the drop-down menu.
- Depending on the size of the transfer, it may take some time to load.

Pink shading indicates that a file has not been normalized to an accepted preservation or access format.
- But in some cases (e.g with a number of images formats like `jpg`) this is because the Archives has departed from the default Archivematica rules.
- You can use the `Review` button to navigate to the a file to view / download for further inspection.
- If you have concerns about a particular result, consult with Artefactual support.
- For more information on how to handle failures, see [Error Handling](error-handling.md).

When you have review normalization results, choose an option: `Approve`, `Redo`, or `Reject`.
- It isn't entirely clear what affect `Redo` has (the Archives has not experimented with this option).

## Add metadata if desired
You can add descriptive or rights metadata to the `SIP` by clicking the `document icon` next to the drop-down menu.
- The Archives does not currently use this feature but there may be use cases in the future.
- Choose `Continue`.

## File format identification (submission documentation)
This step lets you runs file format identification and normalization on `submission documentation`.

Choose `Yes` if you included `submission documentation` in the `transfer package` (see [Submission Documentation](../pre-ingest-actions/submission-documentation.md)); otherwise, choose `No`.

## AIP and DIP creation / storage
You will typically be prompted for `AIP` and `DIP` microservices at the same time. `AIP` processing typically takes longer. **Always let Archivematica complete `AIP` processing before running the `DIP` microservices.**
- If you process the `DIP` first and an error subsequently occurs during `AIP` creation / storage, you will then have to manually delete the uploaded or stored DIP.

## Store AIP
This is your final chance to reject the AIP and cancel the current transfer.

`Store AIP`
- Use to continue.

`Reject AIP`
- Use to cancel, e.g. if you realize you made a mistake and wish to fix and re-start.

## Store AIP location
You can store the AIP with or without `encryption`.
- If there is any possibility that the `AIP` includes personal or confidential information, it should be `encrypted`.
- This includes materials that would have `Access status` = "Pending review" when processed.

Encryption is used to ensure that the Archives can send out `AIPs` containing sensitive data to third parties for geo-remote backup for recovery purposes. **Every encrypted `AIP` is also stored locally in an unencrypted copy in a `replication` directory.**

`Default location`
- Do not use.

`<pipeline_name> AIP store`
- Use for `AIPs` that do not need encryption, i.e. they are known to contain only `open` materials.

`Encrypted AIPs <pipelines`
- Use for `AIPs` that require encryption.

## Upload DIP
- If an error occurs during `AIP` creation / storage, you will likely have to re-run the entire transfer
This step allows you to upload the `DIP` to SFU AtoM (production site).
- **Materials must first be cleared for access and copyright restrictions before they can be uploaded.**

`Upload DIP to AtoM/Binder`
- Use for materials that have cleared access and copyright review.
- Do not use for digitized materials that are **already** described in AtoM (there is a separate process for this; see [CLI DIP Upload](../dip-management/cli-dip-upload.md).

When selecting this option you will be prompted to enter the AtoM `stub` of the **parent** description.
- The `stub` is typically the parent reference code with a lowercase `f-` (e.g. "f-49-1-0-0-1").
- If you know that you will be uploading to AtoM, you can save this step by enter the parent `stub` in the `Access system ID`; see [Start a Transfer](start-transfer.md#access-system-id).

`Upload DIP to Archives Space`, `Upload DIP to ContentDM`
- Do not use.
- SFU Archives does not use these systems.

`Do not upload DIP`
- Use for transfers being sent through as `backlog AIPs` (i.e. require future processing).
- Use for processed materials that have not yet been reviewed for access and copyright clearance or have been reviewed but did not clear or are not being sent to AtoM for any other reason.
- Use for digitized materials that were previously described in AtoM (to upload these, see [CLI DIP Upload](../dip-management/cli-dip-upload.md)).

## Store DIP
If you chose to normalize for access (i.e. created a DIP), always choose `Store DIP`.

## Store DIP location
Always choose `<pipeline_name> DIP store`; do not use `Default location`.

---
###### Last updated: Jan 28, 2022
