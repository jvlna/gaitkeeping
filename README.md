# Gaitkeeping
Gaited Horse Data Visualization Project

# Historical Horse Genetic Map

[Map Link](https://jvlna.github.io/gaitkeeping/)

Map created using Leaflet with data sourced from Wutke, Saskia, et al. “The Origin of Ambling Horses.” Current Biology, vol. 26, no. 15, 8 Aug. 2016, [https://doi.org/10.1016/j.cub.2016.07.001](https://doi.org/10.1016/j.cub.2016.07.001). 

Researchers sequenced the DMRT3 gene in 90 archaeological horse remain samples. A single substitution in this gene is linked to the ability to perform additional gaits beyond the standard walk, trot, canter, and gallop. One of the most notable examples is the tolt, performed by the Icelandic horse. This study has found that the DMRT3 variant was present in horses in England and Iceland around the same time, approximately 850-1050 AD. 

# Map Methodology

Data was pulled from the study's supplemental information *"Table S1: Successfully genotyped samples and corresponding information"* and converted to CSV using [Tabula](https://github.com/tabulapdf/tabula).

Data table was then cleaned up and processed for mapping using the following methods:
- If date was a range, the earliest listed year of the range was selected (*Column C*)
- Samples noted as possible duplicates by researchers were removed from table
- Coordinates (*Columns A and B*) assigned using Anthropic LLM and verified independently. Geographic accuracy confidence is listed in *Column L*, notes in *Column M*, and reference links in *Column N*. Coordinates were first assigned based on known published coordinates of the listed archaological site (high confidence). If not available, coordinates were assigned at the center of an estimated region for the archaological site (medium confidence). If no geographical information on the archaological site was available, coordinates were assigned at the center of the listed country (low confidence).
