### Universites anaylsis in Marsielle, France. Using data from FOURSQUARE public API.

## I. Introduction

Marseille is the second-largest metropolitan area in France after Paris. Marseille is a major French center for trade and industry, with excellent transportation infrastructure (roads, seaport, and airport). Marseille Provence Airport is the fourth largest in France. It is also France's second-largest research center with 3,000 research scientists within Aix Marseille University. Hence, it is not surprising if this city attracts the interest of students doing their Master's degree and Restaurants or Cafe owners.

A lot of students come each year from different countries to study or complete their master's degree in one of the best marseille universities, each university is positioned in a different place in marseille which means that not all the students have access to the same venues or Cafes nearby.

Our goal in this analysis is to find the best-positioned university for the students to be able to access different venues in a short time (between the course breaks) and minimizing the cost of buying food or other stuff.

## II. Data
 -we will need a list of the best universities in marseille and their coordinates. unfortunately, I didn't manage to find this data in a formatted form so I got the university names from [1](https://www.languagecourse.net/universities-marseille),and their coordinates from google maps.we will use the data to plot the universities and find the nearby venues to them.
![alt text](https://raw.githubusercontent.com/nonino/Coursera_Capstone/master/10min.png "Logo Title Text 1")

 
-geocoder for obtaining the coordinates of marseille to plot the map using folium library.

-Foursquare has a public API that can provide us the data. Foursquare has some account tiers for developers. Each tier has a different set of available features [2](https://developer.foursquare.com/docs). In this project, we are using a personal tier. In this tier, we can get the data of venues near the specific location with a specific category. The data should contain longitude, latitude, and the category of the venue. Processing and analysis will be done on this data to help us answer the business problem.


## III. Methodology
There are steps that we need to do to answer the business problem. Here they are:

1.Creating the Dataframe

creating the data frame with the university names.

2. Get longitude and latitude of each university

The coordinate of each university center is needed when using public Foursquare API in the next step.

3. Get a list of  venues near each university

We use the coordinate of the university to find the nearest venues. We limit our exploration by only getting 100 number of venues in radius 1000 meters from the coordinate.so that's only 10 minutes walk from the university. The data should contain longitude, latitude, and the category of the venue.

4. Exploratory Data Analysis (EDA)

Descriptive statistics is useful to describe and summarize the venue data. Creating data visualization of top venue categories and top venues will help us to answer the question.
![alt text](https://raw.githubusercontent.com/nonino/Coursera_Capstone/master/befor.png "Logo Title Text 1")

![alt text](https://raw.githubusercontent.com/nonino/Coursera_Capstone/master/data2.png "Logo Title Text 1")


5. Cluster all universities

5.1.Data Preparation

Data of available categories in each university will be considered as a feature in our model. So, we are playing with a categorical variable. It is convenient to convert this variable to a numerical variable because most machine learning models cannot work well with categorical data as a feature.

5.2.Clustering

We will use k-Mean, which is a popular clustering algorithm for market segmentation, to see the similarity between each university. We divide all universities into 3 clusters.

5.3.Cluster Visualization
It is good for us to see the map of the 3 clusters so we can know visually the geographical distribution of all clusters.
![alt text](https://raw.githubusercontent.com/nonino/Coursera_Capstone/master/cluster.png "Logo Title Text 1")

5.4.Cluster Analysis

## IV. Result and Discussion

Well now after clustering and plotting the universities it becomes obvious that the universities in cluster 0 (the red ones) are the best in term of their position in marseille for the student, because they have a lot of venues nearby in less than a 10 minutes walk , which means better use of their time and most importantly fewer costs because everything is in their reach and more venues mean more competition and lower prices.


## V. Conclusion

Every university in the world has it's advantages and Of course, its disadvantages. The importance of them is to teach the students to be the best doctors, engineers and so on, but they never take in mind the surrounding of the university and its effects on the student time to reach it or the costs of the lunch cafe, etc.. nearby. In this analysis, we focused on this problem, and we found the best of them in terms of their positioning which are Aix-Marseille University, University of the Mediterranean, and the University of Provence.