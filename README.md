# What Urban Factors Affect Success of a Restaurant 
This is the final assignment of Applied Data Science Course in NYU. 

## Group Members
- Zheyuan Zhang (zz2498@nyu.edu)
- Yutong Zhu (yz6080@nyu.edu)
- Guilherme Louzada (gl1082@nyu.edu)
- Di Xin (yli2@skidmore.edu)
- Aparna Bhutani (ab8473@nyu.edu)


## Reference Data Source  and ETL (Extract / Transform / Load) Process 

### Extract

For this project we used data from [Yelp Open Data set](https://www.yelp.com/dataset/). The original file from Yelp was divided in:
- **Business Attributes**: *yelp_business_attributes.csv*
- **Hours of Operation**: *yelp_business_hours.csv*
- **General Business Informaiton**: *yelp_business.csv*
- **Checkin Informaiton**: *yelp_checkin.csv*
- **Review Informaiton**: *yelp_review.csv*
- **Informational Tips left by customers**: *yelp_tips.csv*
- **User Informaiton**: *yelp_user.csv*

These files can be were stored in a Google Drive folder which can be accessed [here](https://drive.google.com/open?id=1WZ9zKjP0MswM6CO2ndhp0tJyjGQGtvCu):

### Transform

#### Part 1 - Reduce the data

Since the original files were too large (over 4gb) we decided to filter only the information related to Phoenix (AZ) to reduce the size of the file. These are the steps taken to do so:

1. Filter *yelp_business* where __'city'__ == 'Phoenix'
2. Generate a unique list of the *yelp_business* __'business_id'__ 
3. Filter *yelp_review* where __'busines_id'__ is in  the list generated on step 2
4. Export an output file with the reduced data as CSV 

#### Part 2 - Build Categories list

Yelp uses an aggregated form to categorize their business, aggregating all types of categories under one single field, separating the difgerente categories by semicolon (for example, an italian restaurant could have the following category: pasta;italian;sandwiche;bar). Since we would work on a categorization problem we needed single categories. In order to solve this issue we created an Excel File and manually assigned a single category by looking at the cases. We didn't automatize this part because we feared an automatized categorization could lead to misscategorization. The categories mapping file is in this GitHub repository (ListOfCategories.xlsx)

#### Part 3 - 

Further Steps could be seen in `Final_Report` file. All contributions to the project are recorded in the report as well.

 





