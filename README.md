# Amazon_Vine_Analysis
Module 16

## Overview:
&nbsp;&nbsp;&nbsp;&nbsp;In this module we will be utilizing "Big Data" and NLP(Natural Language Processing) to give numerical value to Amazon reviews to determine the usefulness and inidcate if there is any bias. In doing so, we will determine if there is discrepancy within the reviews, meaning are there favorably biased reviews embedded amongst genuine/brutally honest reviews. We will carry out our anaylsis via Google Colab and Pyspark following the ETL process to pull desired results then upload our data to pgAdmin by creating a database with AWS(Amazon Web Servers) to funnel the data in its finalized form. 
## Resources:
Data Sources: [Amazon Data Review Sets](https://s3.amazonaws.com/amazon-reviews-pds/tsv/index.txt)  
Software: Google Colab Notebook, PostgreSQL, pgAdmin 4, Amazon Web Service AWS  
- NOTE: The code will fail to run if used in standard jupyter notebook, must utilize Google Colab
## Deliverable 1: Amazon Data Uploaded and Dispalyed
<p align="center">
    <br>  <b> Customer Table</b>  </br>
<img src="https://github.com/KdotGhai/Amazon_Vine_Analysis/blob/5fd587aa99f893adacdc935101c52a750a634e91/Images/pgAdmin_table_images/customers_table.png" width="800" height="400"/>
  <br>  <b> Products Table</b>  </br>
<img src="https://github.com/KdotGhai/Amazon_Vine_Analysis/blob/5fd587aa99f893adacdc935101c52a750a634e91/Images/pgAdmin_table_images/products_table.png" width="800" height="300"/>
  <br>  <b> Reviews ID Table</b>  </br>
<img src="https://github.com/KdotGhai/Amazon_Vine_Analysis/blob/5fd587aa99f893adacdc935101c52a750a634e91/Images/pgAdmin_table_images/review_id_table.png" width="800" height="500"/>
  <br>  <b> Vine Table</b>  </br>
<img src="https://github.com/KdotGhai/Amazon_Vine_Analysis/blob/5fd587aa99f893adacdc935101c52a750a634e91/Images/pgAdmin_table_images/vine_table.png" width="800" height="500"/>
</p>

## Results:

### How many Vine reviews and non-Vine reviews were there?
<p align="center">
    <br>  <b> Total Non-Vine Reviews</b>  </br>
<img src="https://github.com/KdotGhai/Amazon_Vine_Analysis/blob/2b112cc99b451f8fd57b790a085778fbcccc1f5d/Images/Colab_Notebook_images/total_Vine_reviews.png" width="600" height="120"/>
  <br>  <b> Total Non-Vine Reviews</b>  </br>
<img src="https://github.com/KdotGhai/Amazon_Vine_Analysis/blob/2b112cc99b451f8fd57b790a085778fbcccc1f5d/Images/Colab_Notebook_images/total_nonVine_reviews.png" width="600" height="120"/>
</p>
  There were a total of 94 Vine reviews vs. 40,471 Non-Vine Reviews that we processed with the criteria that the reviewer had their review voted on at least 20 times of which 50% or more of the readers voted the review s most helpful

### How many Vine reviews were 5 stars? How many non-Vine reviews were 5 stars?
<p align="center">
  <br>  <b> 5-Star Reviews</b>  </br>
<img src="https://github.com/KdotGhai/Amazon_Vine_Analysis/blob/52efda0f928f767ab2ce817313766460f400096f/Images/Colab_Notebook_images/paid_vs_unpaid_5star_reviews.png" width="600" height="120"/>
</p>

  5 star Vine reviews amounted to 48,  Non-Vine 5 star reviews: 15,663. Although the percentage of paid reviewers doesnt even reach 1% this doesnt mean we can ignore the potential of bias existing in higher numbers for other datasets or other genres/categories of products.

### What percentage of Vine reviews were 5 stars? What percentage of non-Vine reviews were 5 stars?

  This is a percentage of 5 star reviews Paid vs. Unpaid: 0.31%

&nbsp;&nbsp;&nbsp;&nbsp;From the data we notice 48 out of 94 Vine reviews considered helpful, resulted in 51%, more than half of the reviews in the Video Games to be 5 star rating, while 15,663 out of 40,471 non-Vine reviews resulted in about 39% of the reviews being rated 5 stars, clear indications of disparity which inidcates there are more factors in play behind the scenes when it comes to the reviews overall.

## Summary: 

&nbsp;&nbsp;&nbsp;&nbsp;Vote Ratings (helpful and total ratings) most helpful likely rule out many reviews that are either not worded very well or such that it reduced 1,785,997 to 65,379 useful reviews (just 3.7% of the total reviews are considered in this sample set). Since the Vine reviews accounted for just 31% of 5 stars and even less, 23% of all considered reviews. 

<p align="center">
  <br>  <b> 5-Star Reviews</b>  </br>
<img src="https://github.com/KdotGhai/Amazon_Vine_Analysis/blob/5fd587aa99f893adacdc935101c52a750a634e91/Images/Colab_Notebook_images/Vine_Review_Overall.png" width="600" height="120"/>
</p>


&nbsp;&nbsp;&nbsp;&nbsp;We cant attain 100% accuracy from 5-star reviews and even isolating "helpful" reviews when it comes to Vine reviewers since we have proof of bias existing even at the smallest of scales where it would be considered negligible. The percentage of 5-star reviews for Vine customers was higher than those of regular reviewers however, the ratio of helpful [Vines reviews : regular reviewers] is a vast difference in favor of regular reviewers, we can only currently side with Vine reviews with what the data presents.

&nbsp;&nbsp;&nbsp;&nbsp;There are some impactful factors to takine into consideration that will always play a role, influencers or celebrities may skew more customers to write positive/negative reviews thus giving a unrealitic expectation of the product. A "red-flag" that exists is paid Vine reviewers, this is clear indication of bias for monetary gain in providing disingenuous expectations regardless its postive or negative. Furthermore, there is awlays the possibilty of either "Paid-Regular Reviewers" or bots the either sensationalize or slander/belittle products. Lastly, something that can't be tackled directly unless a reviewer goes out of their way to explain themselves is tone of the message, sarcasm, or euphemisms. We can never 100% capture the emotion and intent unless it written/stated as transparent as possible

&nbsp;&nbsp;&nbsp;&nbsp; We may need to tackle the issue of bots and paid reviews in order to ensure the accuracy/authenticity of the reviews that best reflect a product, being informative should never come at the expense of the truth. Also, a possible implementation of allowing reviewers to add adjectives as checkboxes or tags to attach to their starred reviews in an attempt to grasp reviewers emotions/thoughts on the product such as: "moneys worth!", "pricey yet effective/usful", "too costly", "useless", "faulty product", "Short lifespan", etc.

