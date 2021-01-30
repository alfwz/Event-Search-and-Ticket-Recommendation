# Introduction
Event Search and Recommendation Engine is a full stack project powered by TicketMaster, whose purpose is to recommend events based on logged in user's current geo-location. Thanks to TicketMaster, who provides useful APIs, which were used in this project. This project has already been deployed to Amazon EC2, click demo link to visit(userid:1111 pwd:2222 for demo).

# Why doing this project
When I need to buy tickets, I often ask myself "what websites I will use to buy a ticket". After searching for some websites, I found that most ticket websites are just ticket listing websites, instead of a recommendation system. The reasons why I think ticket websites need a recommendation system are listed below.

1. Events most people in US like but you may not like.
2. Events you may like but can’t afford.
3. Events most people don’t know but you may like.
Based on above reasons, I decide to make a personalization based recommendation system for event search.

# Tech Stack
+HTML/CSS/JavaScript/JAVA
+MYSQL/MongoDB

# Recommendatino Algorithm(cotent-based)
In this project, I recommend events based on categories that the user has favorited. By knowing the category of the item the user favorited, I recommend some events belong to this category nearby this user. Concrete steps are as follow.
1. Fetch all the events (ids) this user has visited.
2. Given all these events, fetch the categories of these events.
3. Given these categories, find what are the events that belong to them.
4. Filter events that this user has visited.
5. Sort the recommendation list on ascending order of distance between recommended events's locations and user's location.

# Requirement 
+ Apache Tomat v9.0
+ Eclipse JEE
+ JAVA 8
+ MySQL

# Installation
Clone the GitHub repository and then import Event-Search-Recommendation-Engine.war into your eclipse.
To import WAR file into Eclipse JEE, click on File -> Import. Select Web -> WAR File.
+ WAR file: Provide the full pathname of the WAR file on your computer.
+ Web project: This will pre-fill based on the WAR file name. You can change it, which is handy if you’re experimenting.
+ Target runtime: You will need to select “Apache Tomcat 9.0”. The first time you import a WAR file (or create new “Dynamic Web Project”) you will need to declare the new runtime environment. Do this by clicking on “New” and filling in the form as follows:
  - Apache Tomat v9.0, then click “Next”
  - Provide the Tomcat installation directory by giving the full pathname of the directory containing your unzipped version of Tomcat 9.0.
  - Click “Finished”.
+ Click "Finished".
Run the imported project by “right-clicking” on the new project and selecting “Run As -> Run on Server.
