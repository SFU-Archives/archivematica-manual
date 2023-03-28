###### [Archivematica Manual](../README.md) `>` Processing Configurations

# Processing Configurations
Archivematica `processing configurations` regulate how many `decision points` are exposed to the archivist, requiring them to select among several options for processing.  Thallow you to automate the ingest process by . There is a separate page for each that documents settings and provides a brief description / rationale. The Archives has two processing pipelines, one for standard transfers and the other (with more dedicated RAM and disk space) for larger transfers and files (e.g. video).


Ingest `decision points` occur when Archivematica microservices prompt the archivist to manually choose an option in order to continuing processing a transfer. The Archives has structured the standard default `processing config` to minimize the number of `decision points` that must be answered. Custom `processing configs` automate ingest by specifying in advance **all** decision point selections for a given transfer. Not all transfers can be handled in the same way, so the Archives has created multiple custom `processing configs` to cover most ingest scenarios.
## Standard configuration
The default configuration is the same for both pipelines. See the [Decision points page](../ingest-guidelines/decisions-points.md) for discussion of options on microservices that require intervention.
- [Standard Processing Configuration](standard.md)
- [Decision Points](../ingest-guidelines/decisions-points.md).

## Standard pipeline


## Large transfer pipeline


---
###### Last updated: Jan 26, 2022
