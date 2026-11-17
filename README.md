# Bull Kelp (Nereocystis luetkeana) Monitoring Data Visualization Dashboard

>  Here we will explore the best ways to present Northwest Strait Commission (NWSC) - Marine Resource Committee (MRC) kelp forest monitoring dataset which includes a variety of health metrics taken from June - September in the years 2015 - 2025. As a proof of concept we will focus on the Possession Point monitoring site and expand to other sites in the future. 

---

## Project Overview

- **Objective:** Scientific datasets can often present challenges when it comes to communicating their meaning, here we seek to find the best ways to present complicated and incomplete environmental datasets.
- **Domain:** Ecology

---

## Project Structure

```
├── data/                 # Raw and processed data
├── code/                 # Jupyter notebooks and Python scripts
├── reports/              # Generated reports and visualizations
├── requirements.txt      # Dependencies
└── README.md             # Project documentation
```

---

## Data

Individual cleaned data sets can be located in the "cleaned_eda" code notebook under "Kelp_DataVis.ipynb". 

- **Source:**
- NWS-MRC Kayak Kelp Monitoring Data - "SoundIQ Data Cleaning"
 	- Community Science Monitoring Efforts Performed by the Marine Resource Committees (MRCs), 	funded and managed by Northwest 		Straits Commission (NWSC) 2015 - 2024.
	- We have been given special permission to use a larger data set, however, the public version is available at: 						https://experience.arcgis.com/experience/5416ae7c51ae4244a1a42ba679c1479f/page/ 
  
- **Description:**
	- A census dataset created with the express aim to monitor the location, spatial migration, and area of kelp forests around the Puget Sound. In addition this data set contains Sea Surface Temperature Data and Kelp Expression Area in Acres at 31 sites across the Salish Sea. We expect to see relationships between location and Kelp Expression Area, where different locations may have smaller or greater kelp expansions depending on their conditions. One goal with this data set would be to visualize the change in area of kelp over time.

-  **License:**
	Data used in our specific project is not for public use or publication. 
  

- **Source:**
- Island County MRC Conductivity, Temperature & Dissolved Solids Monitoring - "CTD Cleaning"
	- Salinity & Temperature data taken at select kelp sites in 2015 - 2017 & all sites in 2025
	- Not publicly available.
  
- **Description:**
	- A shorter dataset taken during surveys from sea surface to benthos of temperature and salinity (via converted conductivity) at 4 data points around the perimeter of the kelp perimeter. A relationship we expect to find is an increase of salinity with temperature. An increase in temperature can lead to water evaporation, hence increasing salinity as the solution becomes less diluted. After merging with other data sets, our goal would be determining if salinity or temperature has an impact on kelp growth.
  
- **License:**
	Data used in our specific project is not for public use or publication.

- **Source:** 
- NWS-MRC Kayak Kelp Monitoring Latitude-Longitude Data - "Locations Cleaning"
	- Not publicly available.
  
- **Description:**
	- A small dataset containing latitude and longitude coordinates for multiple kelp bed sites.  We plan to use these coordinates to build site maps, helping us to visualize different spatial relationships between variables. The lat-lon coordinates will be especially helpful as we aim to visualize the change in kelp area across location. 
  
- **License:**
	Data used in our specific project is not for public use or publication. 
---

## Analysis

The notebooks should be run in this order:

1.	
2.	

---

## Results



## Authors
- Carter Ellis- [@EllisWebb](github.com/EllisWebb)

- Ahrial Young - [@ayoung42](https://github.com/ayoung42)
  
- Sydney Golden- [@sgolden3](github.com/sgolden3)

- Jamil Ditter - [@jamilditter](github.com/jamilditter)
---

## License

Licenses outside of data copyright are not applicable. 

---

## Acknowledgements
Thanks to NWSC Employees Jeff Whitty, Leah Skare, and Suzanne Shull for collating and QA/QCing the data, not to mention the day to day work they do to manage the Kelp Monitoring Data. 

Thanks to all MRC volunteers for hundreds of hours on the water collecting data. 



# Description of Graphics

1. Ridgeline of Acreage Change Over Time
	
	Perhaps the most integral part, and certainly the aim, of this monitoring project is to implicitly track the health of kelp throughout the Salish Sea via the change in the maximum area seen each summer at each one of these kelp sites. However, environmental parameters such as temperature, nutrients, and water quality can cause variation on smaller time scales, even from month to month. The ridgeline plot is aimed to showcase how the increase of kelp area over the growing season (June - September) fluctuates during that time period.

2. Depth Change Over Time
	
	Depth is a data point taken 4 times during most surveys, two along the shoreline side of the kelp perimeter, and another two along the sound edge of the kelp perimeter. Changes in depth over time can be indicative of environmental parameters influence of kelp health such as rising temperatures causing a retreat from shallow regions, or sediment changes causing retreats from deeper regions. For this reason, we deemed it important to track these changes in a simple line graph which will depict "average sound edge depth" and "average shore edge depth" throughout the projects history. 

3. Interactive Map of Island County's 5 Monitoring Sites
	
	In order to orient ourselves in space it would be helpful to have a map of the locations of the 5 monitoring sites. We already have all of the latitude and longitudes so it is a matter of finding a projection, and plotting our points of interest on the map. Kelp beds will be in green to meet convention. Filters can be added for additional information, such as salinity, conductivity and temperature at each location for the most recent year. Could potentially include popups that show charts of this information from previous years.

5. 2025 Pycnocline Heat Map (Salinity & Temperature Changes in the Water Column)

	Salinity and temperature are two important ways to identify the density gradient where the pycnocline sits within a body of water. To try and identify at what depth this pycnocline sits, we want to look at the changes in both salinity and temperature from the surface for Possession Point. This site collects data at four distinct points, and we will want to show these points in a side-by-side comparison. We will make two sets of bar charts, one for changes in salinity and one for changes in temperature. The x-axis will be the months in which the surveys were collected, while the y-axis will be the depth at which the temperature or salinity changes. 

6. Percent Area Change

    % CH = ((Area - Area Previous Year) / Area of Previous Year ) * 100

	We can go two different ways to visualize the change in area of the beds from year to year. We experimented with plotting them on a map during EDA (the AY EDA document). If we did this, every year should probably be associated with a different color and be transparent so it does not occlude the years behind it. While this might be a compelling graphic for a casual audience, it leaves a lot to be desired for accuracy of reporting changes in area, which is already a difficult task for a human brain. So the alternate graphic would be a bar chart of normalized data that shows the change in area from year to year. Could be a diverging bar chart to really drive home the increase/ decrease from year to year. Position is the most relevant encoding for this type of chart but, if we were to use color, we would use green for growth (inc) and red for decreases, or even potentially leave decreases as grey so that it is less salient. The scale for this type of chart would be percentage change.

7. Perimeter / Area Ratio (PA) vs Area

	PA = Perimeter (mi) / Area (acre)

Understanding the relationship between the Perimeter/Area Ratio and Area values can support analysis of how kelp expands in the ocean. Both variables are quantitative values, meaning they would be the most effectively encoded by position. An effective plot would be a scatterplot with Area in acres on the x axis, the PA ratio on the Y axis, and categorical color encodings for each location can effectively display how the PA ratio changes by area in different locations. The plot may need to be scaled to accomodate a larger range of values. 

9. Coefficient of Variation (CV) Score

	CV = Standard Deviation of Area / Mean of Area

The Coefficient of Variation Score assesses the variation in area in each bed, with a greater CV implying a greater variance in data. As we're assessing relationships between variables, it's important to recognize which beds may be more or less consistent since it may impact reliability of other asssesments. CV can be expressed in a score box, which may include text encodings for the quantitative CV score values layered on top of a box with a sequential single-hue color scheme for each bed to distinguish concentration of the quantitative value by color. 

Additional Potential Plots:

9. Spline of Temperature Extremes

10. Trend Score

11. Share of Total Acres Monitored Treemap


