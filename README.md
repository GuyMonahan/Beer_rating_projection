# Beer_rating_projection
Taking the ingredients / flavors / descriptions to map what words best match up with the ratings that people attach to a beer.


#Business Proposal

Creating beers (or any beverage for that matter) should be informed by what people like to drink. I want to solve the problem of robustly assessing the overall desirability of beers against their flavors, such that a new, or existing, brewer can create drinks that might be more popular / highly rated. This would be especially useful for new brewers who want to create a menu of beers using different flavors for styles of beer, but want data that reflects what beers are highly rated so that they can come out of the gate with beers that have a better chance of being received well. I am a chemist and have worked with brewing small batches of beer in the past, and would love to eventually open a brewery of my own using data science to better empower my actions.

#Approach
I figure to use natural language processing to comb through reviews web scraped off of www.BeerAdvocate.com about each of the beers along with their ratings. The idea is for each beer type to return important words when it comes to explaining flavor / taste / ingredients, and for that specific beer to also tie those words to its unique rating. Eventually taking all the words from the reviews and predicting ratings for that specific beer that have that component. 
I will use various models to predict the rating of a beer with X type of ingredients / flavors (i.e. the projected rating of a beer with “raspberry” & “coffee” words should have a score of 4.75). Imagine a microbrewer who is looking to try new flavors and wants predictive ideas of the results in terms of ratings.
And create a recommendation engine that will return the best complimentary beers judging from the words and rating (as a reach goal)

The data will be stored as a dataframe when dealing with the NLP.. I am going to be working with strings and floats. I will have to do a lot of tuning for my NLP to try and get as many of the novel words I need and as many of the superfluous words removed as possible. Depending on the style of beer I pick it can range between 3,000 and 18,000 different beers to look through. Creating a word cloud to quickly make apparent which flavors are favored is a starting point. I would like to also see the correlation between the frequency of a flavor vs its rating, the distribution of beer ratings, and other things that might pop up during EDA.

We can use linear regression to help get the score we want. This is a regression problem as we are looking for a numerical result. The target variable are the beer ratings, getting our prediction as close to the actual. The goal is to assign weights to the words that would help better generate a good rating.

Trying to find the MSRE between the projected rating and the actual ought to be the goal. The minimum viable product would be establishing and cleaning the NLP and doing the EDA from which to branch. Moving forward I would like to make the module more flexible for all the different styles of beer and expand the platform of projects to further help prospective new brewers with ideas or data that helps them make business decisions. 


#Repo Map



#Future Goals



#Presentation



#Sources


