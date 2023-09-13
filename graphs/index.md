```mermaid
graph TD

REGISTER((Register Dataset \n By Creating \n GitHub Issue)) 
  -- send metadata --> BIOECO[(BioEco Portal & ODIS)]

BIOECO --> MAP[[US MBON Map of Activities]]

%% REGISTER --> REGIONAL{Select \n regional MBONs.}
REGISTER --> ERDDAP_FMT{Host dataset \n on MBON \n RA ERDDAP}
  --> ERDDAP[(ERDDAP)]

ERDDAP -- upload raw data --> NCEI[(NCEI)]

REGISTER --> THEMATIC{Select \n Data Types} 

THEMATIC --> TAXA((taxonomic \n occurrences)) 
  --> DWC_ALIGN{manually \n align to DwC} 
  --> DWC[(OBIS+GBIF)]
THEMATIC --> DNA((DNA)) 
  --> DWC_ALIGN
THEMATIC -- acoustics --> ACOUSTICS_DB[(?)]
  -- ? --> DWC_ALIGN
THEMATIC -- imaging --> IMAGE_DB[(?)]
  -- ? --> DWC_ALIGN
THEMATIC -- Animal tracking --> ATN[(ATN)]
  -- ? --> DWC_ALIGN
THEMATIC -- optics --> SEABASS 

THEMATIC --> GRIDDED((Gridded \n Spatiotemporal))
GRIDDED --> COG{create COGs} --> COG_DB[(?)]
  --> INDICATORS

DWC --> INDICATORS
ERDDAP --> INDICATORS

%% === working groups
INDICATORS[[Indicator Dev \n Workgroup]]

CKAN[(CKAN)] -- ? --> PORTAL
ERDDAP -- ? --> PORTAL[[MBON data portal]]

%% this "clickable" class works magically? 
classDef clickable color:#25f,text-decoration: underline

%% custom classes
classDef popupsubgraph color:#2ff,text-decoration: underline

%% sub-graphs from within this repo
click DWC_ALIGN "https://ioos.github.io/mbon-docs/mbon-data-flow.html#darwin-core-alignment"
DWC_ALIGN:::popupsubgraph

%% external links
click MAP "https://github.com/marinebon/map-of-activities"
click REGISTER "https://github.com/marinebon/dataset-registry/issues"
```
