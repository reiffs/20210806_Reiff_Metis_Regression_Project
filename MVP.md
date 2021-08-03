### **MVP overview**
* **Goal:** This analysis seeks to identify areas of low Wi-Fi hotspot density relative to heavy commuter traffic. In order to assess density/traffic, it is first necessary to identify standalone commuter volumes and hotspot locations.
* **Process:** Data exploration to reach this conclusion entailed aggregation of daily commuter data at the turnstile level, MTA station level, and finally zip code level; Wi-Fi hotspots were aggregated at the zip code level.   
* **Preliminary visualization:** The first six figures below depict the highest and lowest traffic zip codes for MTA commuters aggregated for the latest three months (Apr, May, Jun, Jul '21) and late summer/fall for '18 and '19 (Jul, Aug, Sept). The following two figures illustrate the highest and lowest density zip codes for public Wi-Fi hotspots; Downtown Brooklyn, Chelsea, and the Upper West Side have the highest hotspot density, while the bottom 20 zip codes have less than 5 hotspots per zip code. 
* **Preliminary conclusions:** At first blush, this suggests there could be opportunity to deploy Wi-Fi hotspots in zip codes similar to **10001** and **10007** as they have some of the highest commuter traffic without a commensurate rank in Wi-Fi hotspot density. 

###### **Preliminary linear regression model results**
![preliminary_linear_reg](https://github.com/reiffs/20210806_Reiff_Metis_Regression_Project/blob/main/graphics/prelim_lr.png)

###### **Model features**
![model_features](https://github.com/reiffs/20210806_Reiff_Metis_Regression_Project/blob/main/graphics/features.svg)
