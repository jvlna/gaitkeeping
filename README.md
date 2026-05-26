# Gaitkeeping
Gaited Horse Data Visualization Project

# Historical Horse Genetic Map

Map created using Leaflet with data sourced from Wutke, Saskia, et al. “The Origin of Ambling Horses.” Current Biology, vol. 26, no. 15, 8 Aug. 2016, [https://doi.org/10.1016/j.cub.2016.07.001](https://doi.org/10.1016/j.cub.2016.07.001). 

Researchers genotyped 90 archaological horse remain samples 

# Map Methodology

Data pulled from the study supplemental information *Table S1: Successfully genotyped samples and corresponding information* and converted to CSV using [Tabula](https://github.com/tabulapdf/tabula).

Data table was then cleaned up and processed for mapping using the following methods:
- If date was a range, the earliest listed year of the range was selected (*Column C*)
- Samples noted as possible duplicates by researches were removed from table
- Coordinates (*Columns A and B*) assigned using Anthropic LLM and verified independently. Accuracy confidence is listed in *Column L*, notes in *Column M*, and reference links in *Column N*. Coordinates were first assigned based on known published coordinates of the listed archaological site (high confidence). If not available, coordinates were assigned at the center of an estimated region for the archaological site (medium confidence). If no geographical information on the archaological site was available, coordinates were assigned at the center of the listed country (low confidence).
