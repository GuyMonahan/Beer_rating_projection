# Beer_rating_projection
Taking the ingredients / flavors / descriptions to map what words best match up with the ratings that people attach to a beer.


# Business Proposal

Creating beers (or any beverage for that matter) should be informed by what people like to drink. I want to solve the problem of robustly assessing the overall desirability of beers against their flavors, such that a new, or existing, brewer can create drinks that might be more popular / highly rated. This would be especially useful for new brewers who want to create a menu of beers using different flavors for styles of beer, but want data that reflects what beers are highly rated so that they can come out of the gate with beers that have a better chance of being received well. I am a chemist and have worked with brewing small batches of beer in the past, and would love to eventually open a brewery of my own using data science to better empower my actions.

# Approach
I want to use natural language processing to comb through reviews web scraped off of www.BeerAdvocate.com about each of the beers along with their ratings. The idea is for each beer type to return important words when it comes to explaining flavor / taste / ingredients, and for that specific beer to also tie those words to its unique rating. Eventually taking all the words from the reviews and predicting ratings for that specific beer that have that component. 

<p align="center">
 <img width="600" height="600" src=images/rating_dist_donut.png>
 </p>

I will use various models to predict the rating of a beer with X type of ingredients / flavors (i.e. the projected rating of a beer with “raspberry” & “coffee” words should have a score of 4.75). 
Imagine a microbrewer who is looking to try new flavors and wants predictive ideas of the results in terms of ratings.
And create a recommendation engine that will return the best complimentary beers judging from the words and rating (as a reach goal)

<p align="center">
 <img width="900" height="300" src=images/word_cloud_all.png>
 </p>

I use random forest (as well as other models) to help get the score I want. This is a classification problem as we are looking for a the ingredients to fit the proper rating. The target variable are the beer ratings, getting our prediction as close to the actual. The goal is to assign weights to the words that would help better generate a good rating.

Moving forward I would like to make the module more flexible for all the different styles of beer and expand the platform of projects to further help prospective new brewers with ideas or data that helps them make business decisions. 


# Repo Map
'''to do'''


# Future Goals
Model - Trying more models, applying grid search, and tuning for the best fit

Recommendation Engine - Creating an engine that can recommend different beers based on ingredients and rating

Feature Development - Exploring other features and how they can be used to improve beers


# Presentation
https://docs.google.com/presentation/d/16cfUsYOI6Sp7UfBFastVWQZUyj3ACCpGpOzJpi6DWTM/edit?usp=sharing


# Sources
www.BeerAdvocate.com

https://github.com/ssmithie/beer_recommender

https://medium.com/@bedigunjit/simple-guide-to-text-classification-nlp-using-svm-and-naive-bayes-with-python-421db3a72d34


