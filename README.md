# data-management-checklists
:warning: this project is under construction and not yet usable. :warning:

The checklists here are the entrypoint for MBON-supported datasets.
Anyone can submit a dataset in any state of development.
The checklists here will walk you through recommended methods for managing data from planning through publication.
Methods differ by region, data type, and research domain - this is a tremendous amount of complexity to consider, if ever you reach a dead end, please open an issue.


# I. ALL DATA
1. submit the MBON-facilitated data resource form (TODO: create)
    1. dataset ID, description, & contact info
    1. state of the data resource [planning, collecting, standarizing, ...]
1. further instructions will be provided based on the information given

# II. domain-specific protocols

## a. Biological Occurrence Data
1. standardize data to Darwin Core (see sub-checklist + diagram [here](https://github.com/ioos/bio_mobilization_workshop/pull/28))
    1. contact BioData Working Group for help
       * [via gh-issues](https://github.com/ioos/bio_data_guide/issues)
       * join one of the open meetings
1. upload your data to an IPT for (OBIS&|GBIF)
    1. contact your (OBIS&|GBIF) node manager for help
1. get the link to your dataset in OBIS/GBIF
1. fill out biodata dataset update form (TODO)
    * link to the dataset in OBIS/GBIF
    * update other info if needed

## b. SpatioTemporal Gridded Data
1. add your data to an ERDDAP server
1. submit the gridded data form (TODO: create)
1. fill out ERDDAP dataset update form (TODO)
    * link to the ERDDAP dataset
    * update other info if needed
    * spatial resolution

# III. report relevant metadata
1. spatial coverage
    * input WKT or shapefiles 
    * required to be added to MBON activities map (NYI)
    * coverage can be inferred from:
        * ERDDAP link
        * OBIS/GBIF link
1. temporal coverage
    * temporal span
    * temporal granularity
    * required to be added MBON activities gantt chart (NYI)
1. ATN link
2. NCEI link
