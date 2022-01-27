###### [Archivematica Manual](../README.md)

# Ingest Guidelines: Overview
This section describes how to process a `transfer package` through the Archivematica `Dashboard`.
- This assumes you have already copied the `transfer package` to the Archivematica `transfer source location`; see [Upload to the Staging Server](../pre-ingest-actions/upload-to-the-staging-server.md).

There are two key components of the Archives' practice:
1. All `transfer packages` are sent through Archivematica to completion, even ones that have not yet been fully "processed", i.e. the content of the transer remains to appraised, selected, and arranged and described.
2. Whenever a DIP is created, it is always stored.

Transfers that are not yet processed in respect of their contents are considered and registered in the AIS as `backlog AIPs`.
- When an archivist is ready to arrange and describe a `backlog AIP`, they download and reingest it for processing.
- On completion the archivist deletes the original `backlog AIP` while retaining its METS file.
- See [Processing Backlog](../ingest-scenrios/processing-backlog.md) for more information about this scenario.

The main advantage of this **full ingest** approach (implemented in 2021) is that all materials put through Archivematica get a consistent treatment (including full normalization). This is useful where materials may sit in backlog for many years before they can be processed.

Universal DIP storage (implemented ca. 2016) ensures that access copies of all materials are always readily available and can be easily downloaded for offline delivery to researchers. This is useful because many materials cannot be upload directly to AtoM pending an [access and copyright review](../dip-management/access-and-privacy-review.md) (and again, there may be a long timelag before this occurs).

**Contents:**
- [Start a Transfer](start-transfer.md)
- [Decision Points](decision-points.md)
- [Update AIS](update-ais.md)
- [Appraisal and Selection](appraisal-and-selection.md)

---
###### Last updated: Jan 21, 2022
