# ReFED-Code-Challenge

The notebook and repo that has been created is used to transform the provided datasets into the desired tables with the needed cleansing and calculations

When approaching this problem, it was important to understand the structure of the data and how it needed to be manipulated in order to conduct the analysis and develop the analytical pipeline.

Breaking down part 1 with the first 4 steps for loading the data, simple transformations and data cleansing.
#When approaching the data cleansing, the basics were covered to check for nulls, duplicates, data types, and outliers in the data. This all showed no issues with this sample dataset. In a real production scenario when there would highly likely be issues in the data, my recommendation for the data cleansing would be to drop nulls, duplicates and outliers as we do not want this bad quality data to affect conclusions that people can make from them on the Insights Engine. If this dropping is too drastic, then a discussion around the quality of the data and ranking from 1 to 5 similar to the Insights Engine today should be considered while mean is used to replace any numerical nulls so as not to cause spread in the data. Another thing to consider during data cleansing is the SLA's and other expectations from the vendors of this data whether its a government, organizational body like Dairy Producers of America, NGO's, academia, or other sources. Improper data could be a discussion with them rather than a technical challenge if the data differs from the expected data that was used for the sharing agreement with ReFED.

Once a clean dataset was established, it was straight-forward to calculate the tons never harvested in Python using the provided formulas as well as calculating that breakdown for those tons never harvested by cause using the provided causes file. A simple data check was done on the provided causes file to ensure that the %'s added to 100% as a sanity check. Following this step, the production dataset is ready for analysis as recommended in Part 2.

These steps were repeated for the farm update in part 3 in order to append the new cleaned dataset to the previous production and create a v2 production dataset for updated analytics.

The architecture for these parts was reading the raw data files from a public github repository using a jupyter notebook generated in Google Colab. The production files are saved in the local directory of the users laptop.

The steps required to replicate the analysis are to download the .ipnyb file and run the file in Google Colab. WHen run in google colab the v1_clean, v1_prod, and v2_prod files will download to the cloud drive itself as part of Colab for further analysis or storage as needed. 
