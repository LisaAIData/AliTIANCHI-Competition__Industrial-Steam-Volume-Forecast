# AliTIANCHI-Competition__Industrial-Steam-Volume-Forecast
This competition is held by Alibaba TIANCHI. 
Competition link: https://tianchi.aliyun.com/competition/entrance/231693/introduction?spm=5176.12281925.0.0.37857137Sn0KXB&lang=en-us

Contest background
The basic principle of thermal power generation is: when fuel is burned, water is heated to generate steam, and the steam pressure drives the steam turbine to rotate, and then the steam turbine drives the generator to rotate to generate electricity. In this series of energy conversion, 
the core that affects the power generation efficiency is the combustion efficiency of the boiler, 
that is, the fuel is burned to heat the water to generate high temperature and high pressure steam. 
There are many factors affecting the combustion efficiency of the boiler, including the adjustable parameters of the boiler, 
such as the combustion feed rate, primary and secondary air, induced air, return air, and water supply water; 
and the working conditions of the boiler, such as the boiler bed temperature, bed pressure, Furnace temperature, pressure, superheater temperature, etc.

Problem description
The data collected by the desensitized boiler sensor (the collection frequency is at the minute level) can predict the amount of steam generated according to the working conditions of the boiler.


I tried to use standardization and box-cox for features, but doing so leads to the higher MSE in the end. This is because the data has already highly close
to normalization and doesn't have magnitude difference. Although these coding still exist in this file because I want to keep what I've wrote, please skip them when you read them.


In general, my final feature workflow is to use raw dataset with:
- Remove outliers using Ridge regression
- Remove low correlation features (<0.5)
- XGBoost, LightGBM, RandomForest regressor with Grid Search to find best parameters.








