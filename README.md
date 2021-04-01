# Beer_rating_projection

<p align="center">
 <img width="900" height="300" src=images/brewing.png>
 </p>

# Business Proposal

Creating beers (or any beverage for that matter) should be informed by what people like to drink. I want to solve the problem of robustly assessing the overall desirability of beers against their flavors, such that a new, or existing, brewer can create drinks that might be more popular / highly rated. This would be especially useful for new brewers who want to create a menu of beers using different flavors for styles of beer, but want data that reflects what beers are highly rated so that they can come out of the gate with beers that have a better chance of being received well. I am a chemist and have worked with brewing small batches of beer in the past, and would love to eventually open a brewery of my own using data science to better empower my actions.

<p align="center">
 <img width="480" height="350" src=images/distrib_beer_ratings.png>
 </p>

# Approach
I want to use natural language processing to comb through reviews web scraped off of www.BeerAdvocate.com about each of the beers along with their ratings. The idea is for each beer type to return important words when it comes to explaining flavor / taste / ingredients, and for that specific beer to also tie those words to its unique rating. Eventually taking all the words from the reviews and predicting ratings for that specific beer that have that component. 

<p align="center">
 <img width="900" height="300" src=images/word_cloud_all.png>
 </p>

I will use various models to predict the rating of a beer with X type of ingredients / flavors (i.e. the projected rating of a beer with “raspberry” & “coffee” words should have a score of 4.75). 
Imagine a microbrewer who is looking to try new flavors and wants predictive ideas of the results in terms of ratings.
And create a recommendation engine that will return the best complimentary beers judging from the words and rating (as a reach goal)

 
<p align="center">
 <img width="600" height="600" src=images/rating_dist_donut.png>
 </p>

I use random forest, linear regression, and other models to create models that will project these ratings. At first I saw this as a classification problem (see the pie visual), looking for a the ingredients to fit the proper rating. But while doing this project I found it made more sense to create a linear model that best represents the outcome of the words, rather than trying to cram some words into ratings they didn't belong because of the context of that particular beers review versus similar beers. The target variable are the beer ratings. The goal is to assign weights to the words that would help better generate a good rating through tf-idf. After culling the most common and least common words, it would leave the most pertient words. Passing them through the models I could track the difference in the training and test sets to make sure my model was not too underfit / overfit.

<p align="center">
 <img width="750" height="600" src=images/freq_beer_ratings.png>
 </p>

The results for the linear models ended up being all roughly between 0.4 and 0.5, where the lower the RMSE the better. The values represented here are the ranges that the results can skew within this model from the best result. While a 0.4 is not ideal when aligned with a rating scheme of 1-5, it makes the better point of being able to explain a lot of the beer in a range that makes sense when compared to the rating groupings we saw with the classification part.  

Moving forward I would like to make the module more flexible for all the different styles of beer and expand the platform of projects to further help prospective new brewers with ideas or data that helps them make business decisions. That would include potentially a recommendation system and using more statistical metrics to update the ratings like abv, original gravity, or ibu. Eventually creating a suite of tools for brewers to use data to glean insight into how to produce and market their beers.

<p align="center">
 <img width="900" height="600" src=images/cheers.png>
 </p>

# Repo Map
cleaned_notebooks [final material]
-Beer_NLP_w_models
-Beer_Web_Scraping

csv_data [The CSV files that house the data]
-beer_df
-beer_w_reviews
-reviews

images [png files for my readme]
-brewing
-cheers
-distrib_beer_ratings
-freq_beer_ratings
-rating_dist_donut
-word_cloud_all

scrap_notebooks [notebooks where I explored the data before organizing it]
-Beer_EDA
-Brewery_API_setup
-brew_api_key

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


