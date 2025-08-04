# Aviation Accident Dashboard Based on NTSB Data

This project presents a Power BI dashboard that visualizes aviation accident data from the National Transportation Safety Board (NTSB) in the United States.

## Purpose of This Project

The dashboard is designed for pilots, aviation professionals, and safety analysts to explore key factors that contribute to aviation accidents. Through comprehensive visualizations of historical data, users can identify safety issues, detect risk patterns, and gain actionable insights that may help prevent future incidents. The interactivity of Power BI allows deep exploration of various dimensions—such as aircraft maintenance and pilot experience—ultimately supporting a safer aviation environment.

## Source Data

The NTSB aviation accident database includes records of civil aviation accidents and selected incidents from 1962 to the present, covering the U.S., its territories, and international waters. Foreign investigations with NTSB participation are also included.

For this project, only U.S. accident data from 2008 onward is used.

- Source: [NTSB Aviation Accident Database](https://www.ntsb.gov/safety/data/Pages/Data_Stats.aspx)
- avall.zip is used for this project [NTSB dataset download page](https://data.ntsb.gov/avdata)

## Table of Contents

- **1. Trend and Distribution**
  - 1.1 Trend of Accidents and Incidents  
  - 1.2 Trend of Injury and Fatality  
  - 1.3 Accident Map  
  - 1.4 Recent 5 Major Accidents  

- **2. Aircraft**
  - 2.1 Aircraft Type Breakdown  
  - 2.2 Breakdown by Weight Class  
  - 2.3 Accident Aircraft by Make and Model  
  - 2.4 Aircraft Flight Hours Distribution  
  - 2.5 Aircraft Age Distribution  
  - 2.6 Aircraft Flight Hours Since Last Inspection Distribution  

- **3. Pilot**
  - 3.1 Pilot Age Distribution  
  - 3.2 Accident Breakdown by Pilot Experience Level of Accident Aircraft Model  
  - 3.3 Breakdown of Accident by Pilot Medical Certificate and Profession  
  - 3.4 Accident Breakdown by Pilot's Instrument Flying Experience  
  - 3.5 Accident Breakdown by Pilot Flight Hours of Accident Aircraft Model within Last 30 Days  

- **4. Cause and Phase**
  - 4.1 Distribution of Damage Level  
  - 4.2 Breakdown of Accident by Causes  
  - 4.3 Breakdown of Accident by Phase of Flight  


## Data Model

The dashboard is built on multiple relational tables structured for efficient analysis:

- **Events**: Accident date, location, and environmental conditions  
- **Aircraft**: Aircraft type, registration, and specs  
- **Flight Crew**: Details about involved pilots and crew  
- **Injury**: Injury and fatality counts  
- **Findings**: Determined causes and flight phases  
- **Flight Time**: Pilot flight experience in hours  

## Key Features

- Interactive filtering by date range, aircraft type, and geographic region
- Cross-filtering capabilities between related visualizations
- Drill-through visuals for detailed analysis of specific data segments (see 4.2 and 4.3)
- Custom DAX measures for calculating meaningful aviation safety metrics
- R script integration for distribution plots
- Geographic mapping for spatial pattern identification

## Notes

- **1.1**: 'Incidents' refer to less serious events that had the potential to escalate into accidents.  
- **1.4**: Only major accidents involving more than 50 injuries are included.  
- **2.4 – 2.6**: These visuals require R; they may not render properly without R installed.  
- **2.4**: Aircraft flight hours track engine operation time, similar to a car's odometer—critical for assessing aircraft condition.  
- **2.5**: Aircraft age is calculated from the manufacturing date.  
- **2.6**: Frequent inspections are key to safety. Aircraft are inspected more rigorously than most vehicles to avoid mid-flight mechanical failures.  
- **3.1 – 4.3**: Visuals use the number of aircraft involved (not accidents), to account for multi-aircraft crashes.  
- **3.2**: Pilot experience is evaluated based on time in the specific aircraft model involved in the accident.  
- **3.3**: A “professional pilot” refers to someone whose occupation is flying, not private or recreational.  
- **3.4**: Instrument flying allows pilots to operate aircraft without external visual references—crucial in low-visibility conditions.  
- **4.2**: “Cause factors” are primary causes per NTSB investigations. “Contributing factors” are secondary conditions or events. Both are essential for a complete picture.
  


## Technical Requirements

- Power BI Desktop (latest version recommended)  
- R (optional, for R-based visualizations)

> **Note:** This dashboard uses a custom visual — [README Visual](https://appsource.microsoft.com/sr-latn-rs/product/power-bi-visuals/michaellindsay1750536687927.readme?tab=overview) — to display introductory information on the first page.  
> To ensure it displays correctly:
> - Download it from the Microsoft AppSource link above or directly from [GitHub - PBI-README](https://github.com/MDeanLindsay/PBI-README).
> - In Power BI, go to `Visualizations > More Visuals > Import from marketplace`, search for **README**, and add it to your report.
> - Identical information to gitlab readme page. In case difficulties with this visual, just refer to gitlab readme page. 

## Installation and Usage

1. Download the `aviation_visualization.pbix` file from the repository  
2. Download the `avall.zip` or download latest avall.mbd from NTSB website. see Source Data section above. **Extract to local folder.** 
3. Open aviation_visualization.pbix in Power BI Desktop  
4. **Update data source connection, connect to avall.mbd in this repo.**
5. If using R visuals, ensure R is installed and configured in Power BI. ggplot2 is used for visual creation and need to be setup in R environment. 

## Future Enhancements

- Integration of weather data for correlation analysis  
- Addition of FAA airspace violation reports  
- Predictive analytics for risk forecasting  
- Mobile-optimized dashboards for on-the-go access  

## Contributors

- **Yi GU** – Project Lead  

## License

This project uses publicly available NTSB data. It is intended solely for educational and safety-awareness purposes.

## Contact

For questions or feedback, contact:  
- **Email**: u4933040@anu.edu.au  
