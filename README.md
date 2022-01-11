# Spatio-Temporal Correlation on Crime Prediction in NYC
Urban Computing 2021 Research Project @ Leiden University

The research project is inspired by Xiangyu Zhao and Jiliang Tang. 2017. 
*Modeling Temporal-Spatial Correlations for Crime Prediction*. In Proceedings of the 2017 ACM on Conference on Information and Knowledge Management (CIKM '17). Association for Computing Machinery, New York, NY, USA, 497–506. DOI:https://doi.org/10.1145/3132847.3133024

The data collected for this projected have mainly been collected from NYC open data https://opendata.cityofnewyork.us/ . For some of the larger datasets, filtering on the dates 07/01/2012 to 06/30/2013 have been applied before downloading the data. Several columns in the dataset have also been removed due to not important for this task based on the data description that can be found at the website where all data was collected. Each entry in the dataset was also assigned to a zipcode, based on the shapefile for NYC zipcode.

The following jupyter notbooks and the data they process will be explained below:
- "preprocessing311data" processes a csv file from https://data.cityofnewyork.us/Social-Services/311-Service-Requests-from-2010-to-Present/erm2-nwe9 already filtered to the years 2012 and 2013 to narrow down the dataset (its a very extensive dataaset otherwise). The x-/y-coordinates of the SPCS data have been deleted since the data also contains the longitude/latitude information of the same kind.
- "preprocessingNYPDcomplaints" processes a csv file from https://data.cityofnewyork.us/Public-Safety/NYPD-Complaint-Data-Historic/qgea-i56i also filtered to only the eximed date. Filtering regarding the date have been applied here.
-"preprocessingSAFdata" processes two csv-files for 2012 and 2013 collected from https://data.cityofnewyork.us/Public-Safety/The-Stop-Question-and-Frisk-Data/ftxv-d5ix. This data only consisted of spatial data in the format of SPCS coordinates, so after filtering on the correct data a conversion from the x,y coordinates to longitude/latitude was made.
-"gettingPOI" is the notebook for fetching points of interest from FourSquare API. It uses the json file "foursquare_venue_categories.json" translating the venue-id to names and interesting information. The closest surrounding venues for each grid will be collected in this file and stored to a new csv.
-"preprocessingTaxiData" - fill it in!

