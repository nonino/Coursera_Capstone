### Universites anaylsis in Marsielle, France. Using data from FOURSQUARE public API.

## I. Introduction

Marseille is the second-largest metropolitan area in France after Paris. Marseille is a major French center for trade and industry, with excellent transportation infrastructure (roads, seaport, and airport). Marseille Provence Airport is the fourth largest in France. It is also France's second-largest research center with 3,000 research scientists within Aix Marseille University. Hence, it is not surprising if this city attracts the interest of students doing their Master's degree and Restaurants or Cafe owners.

A lot of students come each year from different countries to study or complete their master's degree in one of the best marseille universities, each university is positioned in a different place in marseille which means that not all the students have access to the same venues or Cafes nearby.

Our goal in this analysis is to find the best-positioned university for the students to be able to access different venues in a short time (between the course breaks) and minimizing the cost of buying food or other stuff.

## II. Data
 -we will need a list of the best universities in marseille and their coordinates. unfortunately, I didn't manage to find this data in a formatted form so I got the university names from [1](https://www.languagecourse.net/universities-marseille),and their coordinates from google maps.we will use the data to plot the universities and find the nearby venues to them.
 
 - geocoder for op

-Foursquare has a public API that can provide us the data. Foursquare has some account tiers for developers. Each tier has a different set of available features [2](https://developer.foursquare.com/docs). In this project, we are using a personal tier. In this tier, we can get the data of venues near the specific location with a specific category. The data should contain longitude, latitude, and the category of the venue. Processing and analysis will be done on this data to help us answer the business problem.
