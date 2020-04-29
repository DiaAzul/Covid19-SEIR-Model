Covid-19 Modelling
==================

Infectious disease outbreaks (such as the 2020 Covid-19) can have a significant impact on the health and care system. This may result in the cancellation of planned activity to make way for unplanned infectious disease admissions, which has a determinental impact on population health outcomes. Demand forecasting tools to support planning discussions within the health and care system are scarce. This project will evolve a basic infectious disease compartmentalised SEIR model to provide insight into potential future demand for health and care services so that the risk involved in making future capacity decisions can be assessed and appropriate mitigation put in place where appropriate.

##InsightMaker model
The SEIR model is implemented using [InsightMaker](https://insightmaker.com/) an online System Dynamics modelling tool. This is free to use, though payment of a modest membership fee is encouraged. The model, as implemented, provides limited control of parameters using sliders to select values and a pop up dialogue to change the relevant population. Further customisation of the model is possible by creating an account in InsightMaker and cloning the model. This allows the model to be changed extensively, however, does require knowledge of InsightMaker.

The latest version of the model is: *Version 3.0*
The link to the latest version of the model is: [https://insightmaker.com/insight/191052/Infectious-Disease-Model-Version-3-0](https://insightmaker.com/insight/191052/Infectious-Disease-Model-Version-3-0)

The model makes extensive use of vectors within the System Dynamics workflow. Inputing these manually to InsightMaker is challenging for multi-dimensional age-sex arrays. To simplify this an excel workbook was created with assumptions for key variables within the model. This is available within the repository.
[Link](../blob)

##KNIME workflows
To support the modelling activity, analytics workflows were developed to download United Kingdom historical cummulative case numbers at Upper Tier Local Authority level from the Pulic Health England website, and then process them to calculate daily rates; smooth the data; estimate the reproduction number; calculate median and upper/ lower quartile levels across the UTLAs. A second workflow was created to process weekly reported deaths from the Office of National Statistics website, and then interpolate daily deaths which could be matched to the daily case data. These workflows are available here [KNIME Covid-19 workflows](https://hub.knime.com/diaazul/spaces/Public/latest/Covid-19/)


