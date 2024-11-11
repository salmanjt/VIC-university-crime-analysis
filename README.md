# Exploring Criminal Offences and Crime Patterns in Proximity to University Campuses in Victoria, Australia

![Crime-Patterns-University-VIC](images/crime-patterns-university-vic.png)

> This project forms part of a larger research initiative that aims to develop an interactive narrative visualisation, showcasing the pivotal findings from our exploration of crime trends in areas surrounding university campuses. This project repository showcases my initial exploratory data analysis (EDA). The interactive narrative visualisation stemming from this analysis will be shared in a separate repository. Stay tuned for updates!

## Project Description

The safety and well-being of university students is of paramount
importance to educational institutions, law enforcement agencies and
society at large. While universities are generally considered secure
environments for intellectual and personal growth, they are not immune
to criminal activities. Incidents of theft, assault and other forms of
misconduct can have long-lasting psychological and emotional impacts on
victims, as well as the wider university community.

To better understand the scope and nature of the problem, this project
aims to answer the following research questions:

1.  **Crime Trends:** What are the prevalent crime trends in areas surrounding university
    campuses across Victoria, Australia?
2.  **Comparison of Crime Types:** Are there specific types of criminal offences that occur more
    frequently near university campuses compared to their neighbouring
    suburbs?
3.  **Crime Pattern Analysis:** What patterns in recorded criminal offences can be identified
    between suburbs in proximity to university campuses and the broader
    local government areas (LGAs)?

This research utilises data visualisation and geospatial analysis to reveal trends and identify hotspots, offering insights for law enforcement and university security policies to enhance student safety.

## Key Steps Involved

### Data Loading and Preparation

-   **Data Sources**: Crime statistics, geospatial boundaries for Victorian Local Government Areas (LGAs) and suburbs, and university campus locations.
-   **Data Cleansing**: Filtering, handling duplicates, renaming columns and aligning geospatial data for smooth integration.
-   **Data Structuring**: Converting university campus data and crime records into spatial data for mapping and trend analysis.

### Crime Data Analysis

-   **Trend Analysis**: Aggregating offence counts and analysing crime trends by category near university campuses.
-   **Geospatial Analysis**: Using geospatial joins to identify suburbs neighbouring university campuses and analyse offence types by area.
-   **Normalisation**: Calculating crime type concentration in university suburbs vs. neighbouring areas for meaningful comparisons.

### Visualisation and Insights

-   **Bar Charts and Tree Maps**: Visualising prevalent offence types, with specific focus on "Property & Deception" offences, particularly theft-related crimes.
-   **Heatmaps and Interactive Maps**: Examining distribution of property-related offences across targeted suburbs and comparing trends over time.
-   **Time-Series Analysis**: Analysing crime patterns across university suburbs and neighbouring suburbs over time to understand offence persistence and changes.

## Tools & Technologies

-   R (tidyverse)
-   Geospatial Analysis (sf, leaflet)
-   Data Visualisation (ggplot2, treemapify)

## Project Tree

```
📦 VIC-university-crime-analysis
├─ .gitignore
├─ LICENSE
├─ README.md
├─ VIC-university-crime-analysis.Rproj
├─ data
│  └─ input
│     ├─ Data_Tables_LGA_Criminal_Incidents_Year_Ending_March_2023.xlsx
│     ├─ Data_Tables_LGA_Recorded_Offences_Year_Ending_March_2023.xlsx
│     ├─ Data_Tables_Property_Items_Visualisation_Year_Ending_March_2023.xlsx
│     ├─ VIC_PropertyItems.csv
│     ├─ VIC_RecordedOffences_LocationType.csv
│     ├─ VIC_RecordedOffences_OffenceType.csv
│     ├─ VIC_Universities.csv
│     ├─ VIC_lga_boundary
│     │  ├─ vic_lga.dbf
│     │  ├─ vic_lga.prj
│     │  ├─ vic_lga.shp
│     │  ├─ vic_lga.shx
│     │  └─ vic_lga_locality.dbf
│     ├─ VIC_suburb_boundary
│     │  ├─ VIC_LOCALITY_POLYGON_shp.dbf
│     │  ├─ VIC_LOCALITY_POLYGON_shp.prj
│     │  ├─ VIC_LOCALITY_POLYGON_shp.shp
│     │  └─ VIC_LOCALITY_POLYGON_shp.shx
│     └─ aurin-aurin-national-education-dataset-universities-2018-na.csv
├─ images
│  ├─ fig1a.png
│  ├─ fig1b.png
│  ├─ fig2.png
│  ├─ ...
│  ├─ fig7.png
│  ├─ fig7_files
│  │  ├─ (HTML files )
│  └─ fig8.png
└─ notebooks
   ├─ 01-crime-analysis.Rmd
   └─ 01-crime-analysis.pdf
```

## Installation

1.  Clone the repository:

    ```bash
    git clone https://github.com/salmanjt/VIC-university-crime-analysis.git
    cd VIC-university-crime-analysis
    ```

2.  Install required R packages:

    ```r
    install.packages(c(
        "tidyverse", "leaflet", "sf", "scales", "ggthemes", "treemap", "treemapify", "fmsb", "viridis", "htmlwidgets"
    ))
    ```

## Data Sources

This project utilises the following open datasets for analysis:

-   **AURIN - National Education Facilities - Universities 2018**: Provides geospatial data for university locations in Australia.
-   **Crime Statistics Agency - LGA Recorded Offences**: Contains detailed recorded offences by type in Victorian LGAs and suburbs.
-   **Victoria LGA Boundaries and Suburb Boundaries**: Geospatial data delineating suburb and LGA boundaries in Victoria for mapping and area-specific analysis.

## Future Improvements

-   **Population-Weighted Analysis**: Adjust analysis to account for population density in crime rate calculation. This will provide a more accurate representation of crime patterns.
-   **Crime Severity Index**: Incorporate crime severity index to differentiate between minor and major offences for a more nuanced analysis. Might involve integrating additional datasets.
-   **Extended Temporal Analysis**: Expand time-series analysis to track crime trends over longer periods. This will help identify seasonal patterns and long-term changes in crime rates.

## License

This project is licensed under the MIT License - see the [LICENSE](https://github.com/salmanjt/VIC-university-crime-analysis/blob/main/LICENSE) file for details.
