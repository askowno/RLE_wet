## **Workflows for undertaking the (inland) Wetland Red List of Ecosystems (RLE) assessment**

### **National Biodiversity Assessment - South Africa**

*South African National Biodiversity Institute (SANBI)*

June 2025

#### **Summary**

This repository contains a workflow that results in the NBA 2025 Red List of Ecosystems indicators for (inland) Wetland Ecosystems of South Africa.

The Quarto document [RLE_wet.qmd](RLE_wet.qmd) describes the import of the South African wetland database (version x ) prepared by SANBI. The data were imported using the sf package in R and summarised using the tidyverse. The dataset covers XX inland wetland ecosystem types in South Africa and includes per-feature Present Ecological Stats (PES) scores (A-F; good - very poor) developed using the WET-Health framework ([Macfarlane et. al., 2020](https://frcsa.org.za/wp-content/uploads/2020/10/TT-820_Final-web.pdf)).

The Red List of Ecosystems (also known as Ecosystem Threat Status in South Africa) assesses the risk of collapse of each ecosystem type based on a range of criteria on extent, condition and pressures faced by each ecosystem type.

The IUCN RLE (v2) framework was applied and following criterion were assessed:

-   Criterion A2b (current rate of decline in ecosystem extent); based on land cover change rates between 1990 and 2022 - projected forward to 2040.

-   Criterion A3 (historical reduction in ecosystem extent), based on land cover 2022

-   Criterion B1ai was applied using EOO calculations with ongoing decline defined as a decline rate of habitat loss rod of \>= 0.4% per year calculated form land cover change data

-   Criterion B1aii was applied using EOO calculations with ongoing decline defined as a decline in the extent of good/moderate condition estuarine extent (PES Classes A, B, C) from the previous PES assessment period.

-   Criterion D3 was applied to the Wetland Ecological State Class (PES) data such that severity of biotic disruption of \>= 90% was assumed for PES classes E-F; Severity \>=70% was assigned to PES classes D-F; Severity \>=50% was assigned to PES classes C-F. Each of the 22 estuary ecosystem types were assigned to one of the four risk categories: Critically Endangered, Endangered, Vulnerable and Least Concern. The highest risk category for these two criteria is selected as the threat / risk status for each river type.

For consistency with past assessments the South African Ecosystem Threat Status framework (developed by [Nel et al., 2010](DOI:%2010.1111/j.1472-4642.2006.00308.x) and modified by [van Deventer et al., 2019](http://hdl.handle.net/20.500.12143/5847)) was applied in a separate assessment. This approach uses the proportion of each ecosystem type that is in a good - fair condition (PES class A B and C) and a set of thresholds. If less than 20% of a type (measured by length of river segment) is in a A or B condition then the type is categorised as Critically Endangered; if between 20-35% of the type is in A or B condition then the type is categorised as Endangered; If less than 60% of the type is in A or or C condition then the type is categorised as Vulnerable; if none of these thresholds are crossed then the type is Least Concern. The results are referred to as ETS (Ecosystem Threat Status) to differentiate them from RLE results.

#### **Results:**

The assessment results per inland wetland ecosystem type for both the IUCN RLE and South African ETS are presented here [rle_wet_metrics_per_type.csv](outputs/rle_wet_metrics_per_type.csv)

Summary table - count of wetland ecosystem types per HGM zone per IUCN RLE category [rle24_wet_count.csv](outputs/rle24_wet_count.csv)

Summary table - count of wetland ecosystem types per HGM zone per South African ETS category [rle24sa_wet_count.csv](outputs/rle24sa_wet_count.csv)

| RLE 2024 - Wetlands | ETS 2024 - Wetlands |
|------------------------------------|------------------------------------|
| ![](outputs/rle24_wet_barplot_count.jpeg) | ![](outputs/rle24sa_wet_barplot_count.jpeg) |
