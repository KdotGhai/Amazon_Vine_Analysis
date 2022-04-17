# Amazon_Vine_Analysis
Module 16

## Overview:
&nbsp;&nbsp;&nbsp;&nbsp;In this module we will be utilizing "Big Data" and NLP(Natural Language Processing) to give numerical value to Amazon reviews to determine the usefulness and inidcate if there is any bias. In doing so, we will determine if there is discrepancy within the reviews, meaning are there favorably biased reviews embedded amongst genuine/brutally honest reviews. We will carry out our anaylsis via Google Colab and Pyspark following the ETL process to pull desired results then upload our data to pgAdmin by creating a database with AWS(Amazon Web Servers) to funnel the data in its finalized form. 
## Resources:
Data Sources: [Amazon Data Review Sets](https://s3.amazonaws.com/amazon-reviews-pds/tsv/index.txt)
Software: Google Colab Notebook, PostgreSQL, pgAdmin 4, Amazon Web Service AWS
- NOTE: The code will fail to run if used in standard jupyter notebook, must utilize Google Colab

## Results:

### How many Vine reviews and non-Vine reviews were there?
<p align="center">
    <br>  <b> Total Non-Vine Reviews</b>  </br>
<img src="https://github.com/KdotGhai/Amazon_Vine_Analysis/blob/2b112cc99b451f8fd57b790a085778fbcccc1f5d/Images/Colab_Notebook_images/total_Vine_reviews.png" width="600" height="170"/>
  <br>  <b> Total Non-Vine Reviews</b>  </br>
<img src="https://github.com/KdotGhai/Amazon_Vine_Analysis/blob/2b112cc99b451f8fd57b790a085778fbcccc1f5d/Images/Colab_Notebook_images/total_nonVine_reviews.png" width="600" height="170"/>
</p>
  There were a total of 94 Vine reviews vs. 40,471 Non-Vine Reviews that we processed with the criteria that the reviewer had their review voted on at least 20 times of which 50% or more of the readers voted the review s most helpful

### How many Vine reviews were 5 stars? How many non-Vine reviews were 5 stars?

![Q2](Resources/Q2.PNG)

  5 star Vine reviews amounted to 48,  Non-Vine 5 star reviews: 15,663.

- What percentage of Vine reviews were 5 stars? What percentage of non-Vine reviews were 5 stars?

  This is a percentage of 5 star reviews Paid vs. Unpaid: 0.31%

Doing one more calculation,we learn that 48 out of 94 Vine reviews considered helpful, resulted in 51%, more than half of the reviews in the Video Games to be 5 star rating, while 15,663 out of 40,471 reviews resulted in about 39% of the reviews being rated 5 stars.

## Summary: 

Vote Ratings (helpful and total ratings) most helpful likely rule out many reviews that are either not worded very well or such that it reduced 1,785,997 to 65,379 useful reviews (just 3.7% of the total reviews are considered in this sample set). Since the Vine reviews accounted for just 31% of 5 stars and even less, 23% of all considered reviews. 

![Q3](Resources/Q3.PNG)

We cannot say for certain based just the 5 star and helpful review status of whether or not the Vine program creates bias in reviews. the percentage of 5 star reviews for Vine customers was higher than those of regular reviewers, but since the Vine customers accounted for so little helpful reviews vs regular reviewers, we cannot say for certain based on your calculations as is, if there is truly a right leaning bias towards 5 star reviews with Vine .

Such factors as whom the reviewer is... an influencer or celebrity may skew more customers to write positive reviews. We have not and probably should consider how Vine reviewers rate a product in other star ranges 1-4 to see if their review ratings skew to the right more than regular reviewers. Also one last thing to note, Are Vine Reviews done on products that may particular need a boost in reviews or as a form of a paid advertisement vs. a random product selected for review.

We should also chart the review stats for Customer_id's that review too often, as they may have their own bias in reviews (only creating negative reviews)

