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

- **Source:**
- NWS-MRC Kayak Kelp Monitoring Data
 	- Community Science Monitoring Efforts Performed by the Marine Resource Committees (MRCs), 	funded and managed by Northwest 		Straits Commission (NWSC) 2015 - 2024.
	- We have been given special permission to use a larger data set, however, the public version is available at: 						https://experience.arcgis.com/experience/5416ae7c51ae4244a1a42ba679c1479f/page/ 
  
- **Description:**
	- A census dataset created with the express aim to monitor the location, spatial migration, and area of kelp forests around 		the Puget Sound. In addition this data set contains Sea Surface Temperature Data and Kelp Expression Area in Acres at 31 sites 		across the Salish Sea.

-  **License:**
	Data used in our specific project is not for public use or publication. 
  

- **Source:**
- Island County MRC Conductivity, Temperature & Dissolved Solids Monitoring.
	- Salinity & Temperature data taken at select kelp sites in 2015 - 2017 & all sites in 2025
	- Not publicly available.
  
- **Description:**
	- A shorter dataset taken during surveys from sea surface to benthos of temperature and salinity (via converted conductivity) at 4 data points around the perimeter of the kelp perimeter.
  
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

4. 2025 Pycnocline Heat Map (Salinity & Temperature Changes in the Water Column)

5. Perimeter / Area Ratio (PA) vs Area

	PA = Perimeter (mi) / Area (acre)

6. Spline of Temperature Extremes

7. Coefficient of Variation (CV) Score

	CV = Standard Deviation of Area / Mean of Area	

8. Trend Score

9. Share of Total Acres Monitored Treemap

10. Percent Area Change ????

    % CH = ((Area - Area Previous Year) / Area of Previous Year ) * 100

	


