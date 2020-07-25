# Twitter Wrangle Analysis

## Using Twitter API to Wrangle and Analyze WeRateDogs Data
The Twitter user [@dog_rates](https://twitter.com/dog_rates?lang=en), also known as WeRateDogs, is an account that rates dogs with humorous commentary. While the denominator for these ratings is 10, the scores are almost always greater with ratings like 11/10, 12/10, 13/10 etc. WeRateDogs has over 4 million followers and has received international media coverage.

This project focuses on wrangling data from the WeRateDogs Twitter account using Python and its libraries. A thorough assessment of format, quality, and tidiness was performed prior to cleaning. Wrangling efforts and visualizations are provided in the notebook titled 'weratedogs_wrangle_act.ipynb.'

## Datasets
**Enhanced Twitter Archive**

>The [WeRateDogs](https://twitter.com/dog_rates?lang=en) Twitter archive contains basic tweet data for all 5000+ tweets. The archive contains each tweet's text, which was used to extract information like ratings, dog name, and "stage" (i.e. doggo, floofer, pupper, and puppo) to make this Twitter archive enhanced. Only tweets with ratings have been filtered for this file leaving 2,356 tweets total for this analysis. 

**Twitter API**

>[Tweepy](https://www.tweepy.org/) was used to query [Twitter's API](https://developer.twitter.com/en/docs/basics/developer-portal/overview) and gather information like tweet ID, retweet and favorite counts. Access to this data is limited to the 3000 most recent tweets but the enhanced Twitter archive allows the user to pull information for all 5000+ tweet IDs. 

**Image Predictions File**

>Every image in the WeRateDogs archive was ran through a neural network that can classify dog breeds. This file was provided by Udacity and contains image predictions for each tweet ID, an image URL, and numbers that correspond to the most confident prediction (ranging from 1 to 4 since tweets can have up to four images). The image predictions file can be found and downloaded [here](https://d17h27t6h515a5.cloudfront.net/topher/2017/August/599fd2ad_image-predictions/image-predictions.tsv).

## Software
The following packages were used in this analysis:
* Python and libraries:
  * json
  * math
  * Matplotlib
  * NumPy
  * os
  * pandas
  * re
  * requests
  * time
  * Seaborn
* Jupyter Notebooks

## Summary of Findings
* The most popular source for users is Twitter for iPhone followed by Twitter Web Client and TweetDeck.
* The greatest number of tweets created was in December 2015 with 366 new tweets. Since then the number of tweets has decreased and stayed relatively constant with occassional peaks seen in February-March and May-June of 2016 with an increase of 9 and 24 tweets respectively.
* The most frequently assigned numerator is 12 with 447 dogs given a 12/10 rating.
* The algorithm predicted 1617 dog breeds and failed in 370 cases.
* The 10 most frequent dog breeds are: Golden Retriever, Labrador Retriever, Pembroke, Chihuahua, Pug, Toy Poodle, Chow, Pomeranian, Samoyed, and Malamute
* The prediction confidence varies between the 10 most frequent dog breeds. The algorithm is more confident in predictions for breeds like the Samoyed, Pomeranian, and Pug. Less confident predictions near 50% can be seen with Chihuahuas, Toy Poodles, and Malamutes.
* The 10 most frequent dog names are: Oliver, Cooper, Charlie, Lucy, Penny, Tucker, Sadie, Winston, Lola, and Daisy
* Tweets that include a dog name are more likely to be favorited and less likely to be retweeted.
* Tweets with dog ratings above 10 are more likely to be favorited and retweeted.
* The distribution for favorite counts is skewed right when compared to retweet count suggesting that users favorite tweets more often than retweeting.
* Pupper is the most reported dog stage(222) followed by doggo(70), puppo(26) and floofer(7).
* Puppos received the highest ratings. Although puppers appeared the most frequently, they have the lowest average ratings.
* Puppos are the most favorited dog stage. Puppers are the least number of favorites.
* Floofers and puppos have the most retweets. Puppos are the least retweeted.

## Credits
* https://d17h27t6h515a5.cloudfront.net/topher/2017/August/599fd2ad_image-predictions/image-predictions.tsv
* https://developer.twitter.com/en/docs/basics/developer-portal/overview
* https://stackoverflow.com/questions/28384588/twitter-api-get-tweets-with-specific-id
* https://stackoverflow.com/questions/12309269/how-do-i-write-json-data-to-a-file
* https://stackoverflow.com/questions/19482970/get-list-from-pandas-dataframe-column-headers
* https://stackoverflow.com/questions/45184549/python-pandas-new-columns-value-if-the-item-is-in-the-list
* https://stackoverflow.com/questions/51782443/np-where-do-nothing-if-condition-fails
* https://stackoverflow.com/questions/35919907/replace-some-specific-values-in-pandas-column-based-on-conditions-in-other-colum
* https://stackoverflow.com/questions/42574379/python-sorting-dates-after-counting-them-in-pandas
* https://stackoverflow.com/questions/36220829/fine-control-over-the-font-size-in-seaborn-plots-for-academic-papers
* https://www.tweepy.org/
* https://twitter.com/dog_rates?lang=en
* https://www.udacity.com/course/data-analyst-nanodegree--nd002
