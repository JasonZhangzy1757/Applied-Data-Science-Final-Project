# Abstract 

<br />
<br />
Due to the Internet blossoming, reviews are everywhere. Hard to decide what to do for the weekend? go to Trip-Advisor. Which restaurants have the best rating in town? Go to Yelp and you will find the answer. All these online reviews are now the standard for urban people making decisions[1]. Maybe some of the rate does not match the actual experience, as it is biased and subjective[2]. They are still a good reference. Among all these review sites, many researchers have analyzed Yelp review data to impact consumers’ behavior and decision making. Although reviews and rates also have a significant impact on sales and business revenues[3], few research put their vision on restaurants side.  
<br />
<br /> 

New York is a city with a huge diversity of people from all over the world and a wide variety of restaurants. This motivated us to think of what exactly makes a restaurant successful. In our project we are trying to explore these factors which influence the restaurants’ success using yelp data and urban data. In our approach, we first do clustering to find the clusters with similar types of restaurants. We further explore these restaurants along with NLP for customer reviews to analyze the customer satisfaction and we eventually find the factors which drives the success of restaurants in New York.
<br />
<br /> 

In our research, similar to Fan and Khademi[3], we would like to create a fair analysis to predict factors that may impact restaurants’ success. Not only using the Yelp review data, we also implement urban data like average income, population and other shapefiles to make visualizations.
<br />
<br /> 
     

![image](https://github.com/JasonZhangzy1757/Applied-Data-Science-Capstone/blob/master/Early%20Framework%20Images/FrameWork.png)

# Methodologies

- ***Step 1:*** We are going to use population or income or postal zip shapefiles and using data extracted from **Yelp API** or **FourSquare API** to find the similiar restaurant in the similiar districts. (For example, a Chinese restaurant in Flushing and 8th Ave China Town could have a lot in common, we want bias as little as possible, so we shouldn't compare a Chinese restaurant to McDonald's or compare Chinese restaurant in totally different consumption level areas like Manhatten and 8th Ave in Brooklyn.) In this step **Clusters** will be implemented, and we will use python library **folium** to visualize the results. 
<br />
<br /> 

- ***Step 2:*** We are going to use the result from step 1 to build a **regression model**. the same type restaurants in the same district will be samples we use and a series of factors like price range, review counts, rating, and comments etc. will be our features. Because comments is string text form, we are going to use **Natural Language Processing** doing sentiment analysis to get a single number metrics to evaluate the attitude of customers.
<br />

![image](https://github.com/JasonZhangzy1757/Applied-Data-Science-Capstone/blob/master/Early%20Framework%20Images/framework%20picture.png)





# Reference

[1] Chen, P.-Y., Wu, S.-y., and Yoon, J. (2004). “The impact of online recommendations and consumer feedback on sales.” ICIS 2004 Proceedings, 58.

[2] Dellarocas, C. (2003). “The digitization of word of mouth: Promise and challenges of online feedback mechanisms.” Management science, 49 (10), 1407–1424.

[3] Fan, M., and Khademi, M. (2014). “Predicting a business star in yelp from its reviews text alone.” arXiv preprint arXiv:1401.0864.
