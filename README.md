# Location Inference of Tweets: A Performance Comparison of Name-Entity Recognizer and Probabilistic Models

## Abstract
Location information is often collected and used in marketing without informing netizens. Further research is thus essential to understand and evaluate the accuracy and capability of location inference methods. We compare the performance of a Name-Entity Recognizer(NER) and a probabilistic generative model on Twitter location inference with related works. Results show that both text-based methods do not scale well when applied to the contiguous United States.

## Dataset
We used the GeoText Twitter Dataset provided by Eisenstein et al. (2010). The GeoText dataset contains 380,000 tweets from 9,500 users in the contiguous United States, which were collected in the first week of March 2010. (http://www.cs.cmu.edu/~ark/GeoText/)

## Method 1: NER Location Extraction
Our first method is adapted from Brunsting et al. (2016)’s GeoTextTagger using the Stanford CoreNLP software (Finkel et al., 2005) and Nominatim OpenStreetMap.

## Method 2: Probabilistic Generative Model
Ryoo & Moon (2014) described a probabilistic generative model to evaluate location indicativeness of words, and used words with high locality to predict users’ locations.

## Results
### NER Location Extraction
Out of the 9475 Twitter users in GeoText, we were able to retrieve at least one pair of coordinates for 7042 of them. We examined the distance error between the predicted and actual coordinates. If we only consider the top ranked coordinates, our results are similar to those of Brunsting et al. (2016) who had 2.2% for the 10km range and 5.4% for the 100km range. If we consider the top two or three choices, our results are better than Brunsting et al. (2016).

![Results based on the Weighted Distance Scores] (Screenshot_table1.jpg)
