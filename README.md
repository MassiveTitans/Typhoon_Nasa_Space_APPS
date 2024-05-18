# Typhoon_AI




## NASA Space Apps Challenge 2023 in Tashkent
- Team: Typhoon
- - Members:
- - - Yaxshiliqov Javlon
- - - 
    
# Preject info

Predicting wildfire spread is critical  for land management and  disaster preparedness. We applied  our knowledge of wildfires, satellite 
imagery and machine learning to 
demonstrate a globally applicable fire 
spread prediction system using open data.

For this challenge, satellite imagery and machine learning to demonstrate a fire spread prediction system. Satellites offer wide area coverage in near real time, and can access even the most remote locations. Accurate prediction of fire spread could improve disaster response, for example to identify towns or properties in the greatest immediate risk. We used data from the MODIS and VIIRS satellite sensors, which provide long-term observational records in multiple spectral bands, as well as elevation and land cover data to make predictions with both traditional machine learning and deep learning models. The models predicted the next day's fire pattern with higher precision and recall than the baseline model of fire persistence. The use of the predictions in an application which could be used by fire management teams was also demonstrated. In future we hope that Satellite Vu’s high-resolution thermal imagery could be input to models such as these to provide even more spatially accurate fire spread predictions to help them pinpoint specific populations and areas at risk. We would also like to highlight that this work is done as a team challenge in a two-week sprint.


# Data Source
- The historical wildfire data are from the MOD14A1 V6 data set [1].
- Topography data are from the Shuttle Radar Topography Mission (SRTM) [2].
- Weather data are from the Gridded Surface Meteorological data set (GRIDMET) [3].
- Drought data are from the GRIDMET Drought data set [4].
- Vegetation data are from the NASA VIIRS Vegetation Indices (VNP13A1) data set [5].
- Population density data are from the Gridded Population of World Version 4 (GPWv4) data set [6].


# Training Deep Learning model

Amongst several CNN model architectures tested, we selected the ResUNet as it is showed the best performance during preliminary experiments. The ResUNet performance is compared to the baseline (fire persistence).

fire precision	fire recall	no-fire precision	no-fire recall
Baseline	0.27	0.33	0.98	0.98
ResUNet	0.30	0.44	0.98	0.97

The model achieves better precision and recall for the fire class than the baseline. The recall improves more significantly, which works in the favour of an application where the cost of error is higher. Note that the baseline metrics differ from the random forest values for 2 reasons: (1) in the random forest model the outermost pixels are not used and (2) the test dataset may have comprised slightly different images than those used on the random forest as a discrepancy was discovered very late in the day about the version of datasets being used by the two team members.


![5](https://github.com/MassiveTitans/Typhoon_Nasa_Space_APPS/assets/97624379/86ead9d8-731e-4683-929d-6fa8129fe02c)




https://github.com/MassiveTitans/Typhoon_Nasa_Space_APPS/assets/97624379/f89d1e3f-e96d-47c0-b1b9-5249b9094b0f


