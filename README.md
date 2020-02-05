# Neo4j-Project
Airbnb is a trending online marketplace for arranging lodging, homestays or tourism experiences. Neo4j is a new trending graph database engine. In this project, we use Neo4j to create a graph database and analyze the data collect from Airbnb public data sources.  

The dataset was achieved from Kaggle.com and has been pre-processed and cleaned for using to create the graph database with Neo4j. 
 https://www.kaggle.com/tylerx/melbourne-airbnb-open-data#cleansed_listings_dec18.csv

This dataset is collected from Melbourne Airbnb Open Data, as part of the InsiderAirbnb initiative, this dataset describes the listing activity of homestays in Melbourne, VIC, Australia. The dataset used for analyzing Airbnb is included three csv files that are listing.csv, host.csv, and review.csv. 
•	Host report(host.csv): This report data includes the information about the hosts who are registered in Airbnb.
•	Review report(review.csv): This report data shows the reviews written by the guests after staying in a certain accommodation.
•	Listing report(listing.csv): This listing report stores information about the existing accommodation around Melbourne listed in Airbnb.

In host.csv, the data includes the following attributes:
Host_verifications: the verification information of the host
Host_url: the url of the host
Host_location: the address of the host
Host_is_superhost: the indicator of whether the host is a super host or not
Host_response_time: the response time of the host
Host_since: the beginning date of the host
Host_id: the unique id number of the host
Host_name: the name of the host

In the listing.csv, the data includes the following attributes:
Summary: the summary of the host
Amenities: the amenities that the host have
picture_url: the url of the host pictures
Listing_id: the unique id number of the listing
Listing_url: the url of the listing
Host_id: the unique id number of the host
Extra_people: the price of adding an extra people
Zipcode: the zipcode of the host
Calculated_host_listings_count: the calculated count of the host listing
Price: the price of the host
Street: the street address of the host
Neighborhood: the neighborhood area of the host
Name: The room name of the host
Room_type: the type of the room
Longtitude: the longtitude of the room

In the Review.csv, the data includes the following attributes:
Date: the data of the reviewing
Review_id: the unique id of the review
Review_scores_rating: the score rating of the review
Comments: the comments of the host
Listing_id: the id number of the listing linked to the review
Reviewer_name: the name of the review
Reviewer_id: the unique id number of the reviewer

we create the node of Review in the graph database using Cypher to import the csv data file into the database. There are 8208 nodes. 8208 labels and 57456 properties stored in the review. The first relationships were created between the host and listing nodes. There are 100 relationships between each node we created for host and listing. The next relationships were created between review and listing nodes, there are 8208 relationships between nodes of review and listing. 

To analyze the data on different purposes, we list all accommodation names and locations taht do not provide Wi-Fi, how many times a reviewer left reviews, List the pairs of accommodations that have more than three amenities in common, etc. 
