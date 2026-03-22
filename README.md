# irs_eds_capstone

This is the repository for my capstone project on food insecurity and extreme heat.

# Project Summary

Using NYC SNAP participation and daily temperature data from 2009–2018, I examined whether there is a relationship between heat and SNAP enrollment, in order to explore the connection between climate impacts and food insecurity. I found no statistically significant relationship between heat and SNAP participation, even after accounting for lagged heat effects and seasonality. Instead, SNAP trends appear to be driven by longer\-term factors, suggesting monthly heat variation does not meaningfully impact food assistance enrollment in this context. While SNAP participation cannot necessarily be explained by variability in heat, there may be other variables that represent food insecurity and affordability that would be worth examining within a similar framework.

## Project Question

*Hotter summers --> Pressure on household budgets due to higher energy bills --> Impact on ability to afford food*

- How is food insecurity in NYC potentially impacted by changing weather like hotter summers?
- Do hotter summers drive up energy bills so much that people need to join food assistance programs like SNAP to be able to afford food?

## Project Rationale

- **What is the problem you're trying to address?** Climate change is increasing extreme heat and having other impacts that raise the cost of living in cities like New York. Higher utility bills, housing repairs, and other climate\-related expenses can strain household budgets and potentially increase reliance on food assistance programs.
- **Who would be interested in my capstone?** NYC Mayor and staff \(e.g. Mayor's Office of Climate and Environmental Justice & Mayor's Office of Food Policy\), NYC Department of Social Services, city council members, U.S. Congress members
- **Why does the answer to this question matter?** Nutritious food is critical for survival. Without sufficient access, families will not be able to sustain life in a city like New York. Living in New York is becoming less and less affordable as climate impacts worsen. This is a result of higher utility bills, increased need for building repairs, and displacement from flood zones. Climate change, particularly rising extreme heat, may affect food affordability and household budgets in New York City. Understanding whether heat exposure influences SNAP participation can help policymakers anticipate future food and energy assistance needs as the climate continues to change.

## Data Sources

##### SNAP Participation Data: From NYC Human Resources Administration (HRA) via NYC OpenData 

The data I'm using tracks the monthly trend statistics on SNAP supplemental nutrition assistance program recipients. The data comes from the NYC Human Resources Administration but is owned by NYC OpenData. According to the metadata, "data are from the Welfare Management System (WMS). Each record represents the total number of individuals receiving SNAP benefits at any time during the month listed." The dataset comes with two columns. One shows the month and the other shows the number of individuals recieving SNAP benefits in that month. Data comes from the years 2009-2019.

Data link: [SNAP Data](https://data.cityofnewyork.us/Social-Services/Total-SNAP-Recipients-Historical-/5c4s-jwtq/about_data)

##### Monthly Temperature Data: From National Weather Service

This dataset tracks the average monthly and annual temperatures in Central Park from 1869 to 2025. The dataset comes from the National Weather Service. It is presented in a PDF file, so I asked Claud to extract the data into a csv file to use for coding. While I initially thought I could merge this data with the monthly SNAP recipient data, I realized after doing some cleaning and EDA that the monthly average isn't the best metric to use, and I'd need some measure of monthly extremes. 

Data source link: [NWS Central Park Historical Data](https://www.weather.gov/okx/centralparkhistorical)

PDF: [Average Monthly & Annual Temperatures at Central Park](https://www.weather.gov/media/okx/Climate/CentralPark/monthlyannualtemp.pdf)

##### Daily Temperature Data: From SCACIS

This dataset comes from the SCACIS database. I downloaded data from 2009-2019 to correspond with the SNAP data I have. When I pulled in the data, I included both max and min daily temp, and daily precipitation, snowfall, and snow depth. I ended up extracting only the max temp column for my analysis, although the other columns will be helpful for follow-up analysis, like examining the relationship between extreme cold and food security. With the heat data, I constructed a monthly heat metric defined as the number of days per month above 82 degrees F, and focused only on the warm season: May through September. These data were collected in Central Park. 

Data link: [SCACIS Data](https://scacis.rcc-acis.org/)

## Process

- Clean SNAP dataset
- Clean daily temp dataset
- Define a variable to represent extreme heat
- Merge datasets
- Conduct exploratory data analysis
- Build visualizations (time series plots, scatterplots, distribution plot)
- Run simple regression: heat + SNAP recipients
- Run multiple regression: heat + lagged heat + SNAP recipients + seasonality control

## Repository Structure
```
irs_eds_capstone/
├── communication/         # Slides, reports, presentations
│   └── README.md          # Communication folder overview
├── data/                  # All datasets and related files
│   ├── analysis/          # Intermediate analysis files
│   ├── archive/           # Unnecessary or old data
│   ├── metadata/          # Data documentation
│   ├── outputs/           # Final tables, figures
│   ├── processed_data/    # Cleaned datasets
│   ├── raw_data/          # Original, untouched data
│   └── README.md          # Data folder overview
├── scripts/               # All code and scripts
│   ├── archive_scripts/   # Old scripts
│   └── README.md          # Scripts folder overview
└── README.md              # Project overview
```

## Other Notes

- The main Jupyter notebook that has data cleaning, EDA, and analysis is called: "SNAP_TEMP_cleanup_analysis_012826"
- This is located in the "Scripts" folder.

## Contact Information
- Ilana Schwartz
- ilanaRschwartz@gmail.com
- [LinkedIn](https://www.linkedin.com/in/ilana-schwartz-755295103/)
