# We-Rate-Dogs

Introduction
Real-world data rarely comes clean. Using Python and its libraries, you will gather data from a variety of sources and in a variety of formats, assess its quality and tidiness, then clean it. This is called data wrangling. You will document your wrangling efforts in a Jupyter Notebook, plus showcase them through analyses and visualizations using Python (and its libraries) and/or SQL.

The dataset that you will be wrangling (and analyzing and visualizing) is the tweet archive of Twitter user <a href= "https://twitter.com/dog_rates">@dog_rates</a>, also known as <a href= "https://en.wikipedia.org/wiki/WeRateDogs">WeRateDogs</a>. WeRateDogs is a Twitter account that rates people's dogs with a humorous comment about the dog. These ratings almost always have a denominator of 10. The numerators, though? Almost always greater than 10. 11/10, 12/10, 13/10, etc. Why? Because ,a href= "https://knowyourmeme.com/memes/theyre-good-dogs-brent" >"they're good dogs Brent"</a>. WeRateDogs has over 4 million followers and has received international media coverage.

WeRateDogs downloaded their Twitter archive to make the tweets into a concise usable. This archive contains basic tweet data (tweet ID, timestamp, text, etc.) for all 5000+ of their tweets as they stood on August 1, 2017. More on this soon.

# The Data
**Enhanced Twitter Archive**

The WeRateDogs Twitter archive contains basic tweet data for all 5000+ of their tweets, but not everything. One column the archive does contain though: each tweet's text, which I used to extract rating, dog name, and dog "stage" (i.e. doggo, floofer, pupper, and puppo) to make this Twitter archive "enhanced." Of the 5000+ tweets, I have filtered for tweets with ratings only (there are 2356).

**Additional Data via the Twitter API**

Back to the basic-ness of Twitter archives: retweet count and favorite count are two of the notable column omissions. Fortunately, this additional data can be gathered by anyone from Twitter's API. Well, "anyone" who has access to data for the 3000 most recent tweets, at least. But I, because I have the WeRateDogs Twitter archive and specifically the tweet IDs within it, can gather this data for all 5000+. And guess what? I'm going to query Twitter's API to gather this valuable data.

**Gathering Data for this Project**

I've gathered each of the three pieces of data in a Jupyter Notebook titled wrangle_act.ipynb

The WeRateDogs Twitter archive. twitter_archive_enhanced.csv

The tweet image predictions, i.e., what breed of dog (or other object, animal, etc.) is present in each tweet according to a neural network. This file (image_predictions.tsv) is hosted on Udacity's servers and should be downloaded programmatically using the Requests library and the following URL: https://d17h27t6h515a5.cloudfront.net/topher/2017/August/599fd2ad_image-predictions/image-predictions.tsv

Each tweet's retweet count and favorite ("like") count at minimum, and any additional data you find interesting. Using the tweet IDs in the WeRateDogs Twitter archive, query the Twitter API for each tweet's JSON data using Python's Tweepy library and store each tweet's entire set of JSON data in a file called tweet_json.txt file. Each tweet's JSON data should be written to its own line. Then read this .txt file line by line into a pandas DataFrame with (at minimum) tweet ID, retweet count, and favorite count. Note: do not include your Twitter API keys, secrets, and tokens in your project submission.


The instructions to deal stuff related to twitter is explained in this file. <a href="https://github.com/Siva123Prasad/We-Rate-Dogs/blob/master/Twitter.pdf">Twitter</a>

The analysis and insights reports of this project can be found here.
<a href="https://github.com/Siva123Prasad/We-Rate-Dogs/blob/master/act_report.pdf">Analysis Report</a>

The complete wrangling report can be found here.
<a href="https://github.com/Siva123Prasad/We-Rate-Dogs/blob/master/wrangle_report-converted.pdf">Wrangle Report</a>
