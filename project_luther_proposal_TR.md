# Project Luther Proposal - Fate of the STARmeter

### What makes an actor famous?

Analysis: Torin Rettig

### Proposal
An actor's fame, more than any other factor, determines the fate of their career. More than the producers or director, having a popular actor in your production can make the difference between a hit and a bomb so being popular makes a huge difference in what roles an actor can take. The IMDb STARmeter approximates an actor's fame by tracking interest in a particular actor on their site. The more traffic for a particular actor on the site, the higher the STARmeter, and as IMDb is the premier movie and TV industry database, STARmeter provides a good estimation for an actor's actual popularity.
But what are the factors that most strongly correlate with an actor's fame? Being in a big budget tentpole film? Having numerous articles written about them, the performance of their last film? Instagram followers? We will look at these factors and others to determine which have the biggest effect on an actor's STARmeter rating and use it to create a model to predict what their STARmeter rating would be, given the relevant factors in play. 


### Assumptions
* There is a vast array of potential factors to consider. To reduce the amount of features in the initial scrape and analysis we're going to assume that the last major production they were in will have the most influence, so we will look at several details of that last production as a significant number of the factors involved.
* We will also look at more conventional indicators of fame that are available, such as the number of articles written about the actor, Instagram followers and Twitter followers.
* Finally, as points of interest, we will look at factors that seem neutral, but that may have more affect than we would expect. These are factors such as age, height and gender. 

###  Methodology
* Gather actor STARmeter ratings
* Gather actor and  available through IMDb and other sites.
* Gather relevant details about the actor's latest film/TV production.

### Data
* Gather the top 1000+ actors' current STARmeter ratings
* Gather additional information about that actor and their recent productions to determine which have the greatest affect on their STARmeter rating.
* Build a linear regression model to determine factors that most influence STARmeter.
* Data Sources: IMDb, Twitter, Instagram

### Features
* Age (IMDb) - <Integer>
* Height (IMDb) - <Integer>
* Gender (IMDb?) - <Categorical>
* Time since last major release (IMDb) <Datetime>
* MOVIEmeter rating of last film (IMDb) <Integer>
* Production cost of last film (IMDb) <Integer>
* US gross of last film released (IMDb) <Integer>
* Worldwide gross of last film released (IMDb) <Integer>
* Articles written about actor (IMDb) <Integer>
* Time since last article written (IMDb) <Datetime>
* Number of images on IMDb (IMDb) <Integer>
* Instagram followers (IMDb + Instagram) <Integer>
* Twitter followers (IMDb + Twitter) <Integer>
* MOVIEmeter rating of actor's "Known For" production (IMDb) <Integer>
* Ratings Breakdown of last film (IMDB) <Float>

### Prediction
STARmeter rating for a given actor
