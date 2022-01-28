###### [Archivematica Manual](../README.md) `|` [Ingest Guidelines](overview.md)
###### [Start a Transfer](start-transfer.md) `|` Decision Points `| `[Update AIS](update-ais.md) `|` [Appraisal and Selection](appraisal-and-selection.md)

# Decision Points
Some Archivematica microservices allow multiple options requiring choice.
- Options can be pre-selected in an automated [custom processing configuration](../processing-configurations/overview.md).
- `Decisions points` occur when microservices settings are **not** pre-configured and therefore require the archivist to manually choose an option.

This page describes the `decision points` in the [standard processing configuration](../processing-configurations/standard.md).
- For custom configurations, see the entries on [Processing Configurations: Overview](../processing-configurations/overview.md).

There is only one `decision point` required on the `Transfer` tab. Pre-defined settings include:
- Generate tree directory structure of the transfer.
- Identify file formats.
- Run BulkExtractor to identify potentially sensitive data (e.g. credit card numbers).

On the `Ingest` tab there are several `decision points`, mainly relating to the choice of whether and where to create / save `AIPs` and `DIPs`. Pre-defined settings include:
- Generate thumbnails.
- OCR image files.
- Use `7z without compression` as the AIP compression setting.

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
- Send transfer to the `Ingest` tab to continue.
- Use if the transfer does not require any additional appraisal, selection, or arrangement.
- Use if it does require addtional processing but you will not be doing this in the immediate future (process through Archivematica to create a `backlog AIP`).

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

Normalization failures will also generate an Archivematica email report.
- You should save these reports and upload to the AIS in the AIP's `Event` log.
- These emails often cannot be printed / pdf'ed easily (file names may not fit the screen).
- It is better to copy the table data from the email into a `csv` and save / upload it in this format.

When you have review normalization results, choose an option: `Approve`, `Redo`, or `Reject`.
- It isn't entirely clear what affect `Redo` has (the Archives has not experimented with this option).

## Add metadata if desired
You can add descriptive or rights metadata to the `SIP` by clicking the `document icon` next to the drop-down menu.
- The Archives does not currently use this feature but there may be use cases in the future.
- Choose `Continue`.

## File format identification (submission documentation)
This step lets you runs file format identification and normalization on `submission documentation`.

`Yes`
- Use if you included `submission documentation` in the `transfer package` (see [Submission Documentation](../pre-ingest-actions/submission-documentation.md)).

`No`
- Use if not applicable (i.e. there is no `submission documentation`).

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
- Upload DIP to AtoM/Binder
- Upload DIP to Archives Space
- Upload DIP to ContentDM
- Do not upload DIP

## Store DIP
- Store DIP
- Do not store

## Store DIP location
- Default location
- <pipeline_name> DIP store

---
###### Last updated: Jan 27, 2022
