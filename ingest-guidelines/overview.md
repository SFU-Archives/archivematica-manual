###### [Archivematica Manual](../README.md) `>` Ingest Guidelines
###### [Start a Transfer](start-transfer.md) `|` [Decision Points](decision-points.md) `| `[Update AIS](update-ais.md) `|` [Appraisal and Selection](appraisal-and-selection.md) `|` [Error Handling](error-handling.md)

# Ingest Guidelines: Overview
###### Last updated: Mar 28, 2023
This section describes how to process a `transfer package` through the Archivematica `Dashboard`.
- This assumes you have already copied the `transfer package` to the Archivematica `transfer source location`; see [Upload to the Staging Server](../pre-ingest-actions/upload-to-the-staging-server.md).

There are three main principles:
- [Process all transfers to completion](#process-all-transfers-to-completion).
- [Store all DIPs](#store-all-dips)
- [Use processing configurations whenever possible](#use-processing-configurations-whenever-possible)

## Process all transfers to completion
All transfer packages should be fully processed through Archivematica as AIPs.
- **Exception:** transfers can be sent to Archivematica backlog if you plan in the near term to appraise / arrangement materials in Archivematica using the `Appraisal` tab.

Typically the Archives processes (appraises, selects, arrangement) transfers outside Archvimatica. Transfers not yet processed are still sent through Archivematica, but registered in the AIS as `backlog AIPs.`
This includes ones that have not yet been "processed", i.e. the content of the transfer still needs to be
- When an archivist is ready to arrange and describe a `backlog AIP`, they download it for processing (appraisal, selection, arrangement) outside Archivematica.
- On completion of processing, the archivist ingests the now-processed records as a new Archivematica transfer and deletes the old `backlog AIP.`
- See [Processing Backlog](../ingest-scenrios/processing-backlog.md) for more information about this scenario.

The main advantage of this **full ingest** approach (implemented in 2021) is that all transfers now get a consistent treatment and are stored in one place. This is useful where some materials may sit unprocessed in storage for many years before they can be arranged and described.

## Store all DIPs
If a DIP is created, it is always stored. This ensures that access copies of all materials are always readily available and can be easily downloaded for offline delivery to researchers. This is useful because many materials cannot be upload directly to AtoM due to access or copyright restrictions or pending an [access and copyright review](../dip-management/access-and-privacy-review.md) (and again, there may be a long timelag before this occurs).

Not all transfers require DIPs to be created; see [Ingest scenarios](../ingest-scenarios/overview.md) for different cases.

## Use processing configurations whenever possible
Ingest `decision points` occur when Archivematica microservices prompt the archivist to manually choose an option. The Archives has configured the `standard processing config` to minimize the number of `decision points`. `Custom processing configs` automate ingest by specifying in advance all decision point selections for a given transfer. Not all transfers can be handled in the same way, so the Archives has created multiple custom `processing configs` to cover most ingest scenarios.

You should only use the [standard default configuration](../processing-configurations/standard.md) if none of the custom configurations applies to your transfer. In some cases (e.g. digitization project), you may want to create a project-specific, one-off `processing config` to handle all ingests for just that project.

See [Processing Configurations](../processing-configurations/overview.md) for a list of the customized configurations available.

See [Decision Points](decision-points.md) for the prompts that occur with the [standard default configuration](../processing-configurations/standard.md).

## Contents of this section
- [Start a Transfer](start-transfer.md)
- [Decision Points](decision-points.md)
- [Update AIS](update-ais.md)
- [Appraisal and Selection](appraisal-and-selection.md)
- [Error Handling](error-handling.md)
