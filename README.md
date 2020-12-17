# Battle_of_Neighbourhoods
# Oxford City Food Choices: Business Proposal

# Introduction
The purpose for this project is to explore the various food or restaurant venues in Oxford, UK. It aims to help identify various venues based on their price and ratings and allow people living in or visiting Oxford to make an informed decision of where to go eat.
There are many people, especially students, living in Oxford or in the surrounding areas of Oxfordshire. Oxford is a world famous university city which it draws hundreds of visitors each year. It would be beneficial to have a selection of venues whereby people can explore the various food or restaurant choices and determine if they would like to try these places out by primarily looking at the price tier that will fit their budget, venue ratings and likes by other customers. As many students living in the area and are mostly on a tight budget, it is would be good to know where to go for a good inexpensive meal or splurge out on a highly rated more expensive venue. 

# Problem to be solved:
The purpose of this project is to help visitors to Oxford to identify and explore food venues close to the Oxford city centre based on their location, price, ratings and likes so they can make an informed decision on where to visit.

# Data Description
Location data:
Oxford city is in the county of Oxfordshire, UK, the postcode areas pertaining to Oxford will be scraped from https://en.wikipedia.org/wiki/OX_postcode_area using requests and BeautifulSoup libraries and the information converted to a pandas dataframe. The postcode areas will be used to get the location coordinates (latitude and longitude) of Oxford centre and the postcode areas using the Geopy Geocoder library. Folium library will be used to bind the location data of Oxford and the postcode areas onto an interactive map.

# Foursquare API: 
This project would use the Foursquare API as its prime data gathering source as it has a database of millions of places, especially their Places API that provides the ability to perform location search, location sharing and details about various venues. Requests are made to the API to search and explore venue recommendation data nearby the targeted location coordinates (Oxford centre). The information to be retrieved would be the venue name, venue ID, venue latitude and longitude and venue categories. The venue ID will be used to explore more in depth into the venue details and retrieve the venue ratings, price tier and the number of likes. These details will be used to explore which places are good to visit based on their price tier and ratings and the number of likes previous customers have given to the venue.
To use the Foursquare API to request data, client credentials (client id and client secret) are required; this is acquired from the Foursquare developers website once you sign up. Using the credentials and the foursquare requests URL, requests for nearby venue information can be mined. Request limitations for the number of places per neighbourhood parameter would be set to 100, the radius parameter would be set to 2200m and the request version date will be the current date.

# Clustering Method:
After the data collection and cleaning, the data will be analysed and various analysis techniques will be used to visualise the data and extract insightful information. Following this, K-Means clustering algorithm method will be used to cluster the venue information based on the location, price tier, ratings and number of likes. This will then be represented on a map.

