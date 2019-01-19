# Project Luther Proposal - Fate of the STARmeter

Analysis: Torin Rettig

### What makes an actor popular?

### Proposal
An actor's fame, more than any other factor, determines the fate of their career. More than the producers or director, having a popular actor in your production can make the difference between a hit and a bomb so being popular makes a huge difference in what roles an actor can take. The IMDb STARmeter approximates an actor's fame by tracking interest in a particular actor on their site. The more traffic for a particular actor on the site, the higher the STARmeter, and as IMDb is the premier movie and TV industry database, STARmeter provides a good estimation for an actor's actual popularity.

But what are the factors that most strongly correlate with an actor's fame? Being in a big budget tentpole film? Having numerous articles written about them, the performance of their last film? Instagram followers? We will look at these factors and others to determine which have the biggest effect on an actor's STARmeter rating and use it to create a model to predict what their STARmeter rating would be, given the relevant factors in play.

### Assumptions
* There is a vast array of potential factors to consider. To reduce the amount of features in the initial scrape and analysis we're going to assume that the last major production they were in will have the most influence, so we will look at several details of that last production as a significant number of the factors involved.
* We will also look at more conventional indicators of fame that are available, such as the number of articles written about the actor, Instagram followers and Twitter followers.
* Finally, as points of interest, we will look at factors that seem neutral, but that may have more affect than we would expect. These are factors such as age, height and gender.

###  Methodology
* Gather collection of 1000+  actor STARmeter ratings
* Gather actor details  available through IMDb and other sites.
* Gather relevant details about the actor's latest film/TV production.
* Build a linear regression to determine the factors that most greatly affect STARmeter rating.

### Data
* Target - Actor's STARmeter rating.
* Features - Actor personal details and data relating to their overall popularity.
* Features - Movie/TV production details relating to the performance of the actor's latest film/TV production.
* Features - Number of followers for each actor on Twitter and Instagram.
* Data Sources: IMDb, Twitter, Instagram

### Features
1. Time since last major release (IMDb) - (Datetime)
2. MOVIEmeter rating of last film (IMDb) - (Integer)
3. US gross of last film released (IMDb) - (Integer)
4. Opening weekend gross of last film released (IMDB) - (Integer)
5. Production cost of last film (IMDb) - (Integer)
6. Worldwide gross of last film released (IMDb) - (Integer)
7. Instagram followers (IMDb + Instagram) - (Integer)
8. Twitter followers (IMDb + Twitter) - (Integer)
9. Ratings Breakdown of last film (IMDB) - (Float)
10. Articles written about actor (IMDb) - (Integer)
11. MOVIEmeter rating of actor's "Known For" production (IMDb) - (Integer)
12. Ratings Breakdown of last film (IMDB) - (Float)
13. Time since last article written (IMDb) - (Datetime)
14. Number of images on IMDb (IMDb) - (Integer)
15. Age (IMDb) - (Integer)
16. Height (IMDb) - (Integer)
17. Gender (IMDb) - (Categorical)

### Prediction
STARmeter rating for a given actor

### Stretch Goals

- Predict actor's time in the top 10/100
- Predict ROI based on STARmeter rating of principals 

### Additional Features

- Last Film MOVIEmeter Trend (IMDb) - (Integer)
- Last Film Gross Trend -Weekend- (IMDb) - (Integer)
- Last Film Gross Trend -Daily- (IMDb) - (Integer)
- Last Film Gross Trend -To Date- (IMDb) - (Integer)
- Last Film Opening Month (IMDb) - (Integer) 
- Last Film Opening Weekend Theater Count (IMDb) - (Integer)
- Award Nominations (IMDb) - (Integer)
- Awards Won (IMDb) - (Integer)