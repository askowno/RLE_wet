## **Workflows for undertaking the (inland) Wetland Red List of Ecosystems (RLE) assessment**

### **National Biodiversity Assessment - South Africa**

*South African National Biodiversity Institute (SANBI)*

June 2025

#### **Summary**

This repository contains a workflow that results in the NBA 2025 Red List of Ecosystems indicators for (inland) Wetland Ecosystems of South Africa following the methods of [van Deventer et al., 2019](http://hdl.handle.net/20.500.12143/5847)

The Quarto document [RLE_wet.qmd](RLE_wet.qmd) describes the import of the South African wetland database (version x ) prepared by SANBI. The data were imported using the sf package in R and summarised using the tidyverse.

The Red List of Ecosystems (known as Ecosystem Threat Status in South Africa) assesses the risk of collapse of each ecosystem type based on a range of criteria on extent, condition and pressures faced by each ecosystem type. For consistency with past NBAs this assessment follows the methods developed by Nel et al., 2011 and modified by [van Deventer et al., 2019](http://hdl.handle.net/20.500.12143/5847). Each of the 100 wetland ecosystem types were assigned to one of the four risk categories: Critically Endangered, Endangered, Vulnerable and Least Concern.

The analysis approach of van Deventer et al., 2019 uses the proportion of each ecosystem type that is in a good - fair condition (Wet Health class A, B and C) and a set of thresholds. If less than 20% of a type (measured by extent) is in an A or B condition then the type is categorised as Critically Endangered; if between 20-35% of the type is in A or B condition then the type is categorised as Endangered; if less than 60% of the type is in A or B or C condition then the type is categorised as Vulnerable; if none of these thresholds are crossed then the type is Least Concern. This methods aligns with the South African Framework for Threatened ecosystems but not the IUCN RLE 1.1. Processes to transition to the IUCN framework are underway - but in the interest of comparing past results the 2019 methods have been implemented.

#### **Results:**

Overall per-ecosystem type RLE 2024 results using South African methods (van Deventer et al., 2019) and IUCN RLE methods [rle_wet_metrics_per_type.csv](outputs/rle_wet_metrics_per_type.csv)

Summary table - count of wetland ecosystem types per HGM zone per South African RLE category [rle24_sa_wet_count.csv](outputs/rle24_sa_wet_count.csv)

![Wetland RLE 2024 - using the South African Method](outputs/rle24sa_wet_barplot_count.jpeg)
