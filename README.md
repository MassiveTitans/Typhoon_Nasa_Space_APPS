# Typhoon_Nasa_Space_APPS

![photo_2023-10-08_09-26-53](https://github.com/MassiveTitans/Typhoon_Nasa_Space_APPS/assets/97624379/99e3dc90-6caa-4d03-812e-b3f16f6f0b92)


## NASA Space Apps Challenge 2023 in Tashkent
- Team: Typhoon
- - Members:
- - - Yaxshiliqov Javlon
- - - Jabborov Diyorbek
    
# Preject info

Predicting wildfire spread is critical  for land management and  disaster preparedness. We applied  our knowledge of wildfires, satellite 
imagery and machine learning to 
demonstrate a globally applicable fire 
spread prediction system using open data.


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

https://github.com/MassiveTitans/Typhoon_Nasa_Space_APPS/assets/97624379/f89d1e3f-e96d-47c0-b1b9-5249b9094b0f


