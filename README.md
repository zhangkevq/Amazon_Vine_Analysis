# Amazon_Vine_Analysis
Big Data using PySpark, Amazon Web Service (AWS), Google Colaboratory, and pgAdmin

## Overview of the Analysis
Various natural language processing skills were explored to prepare a customer review analysis for a client interested in digital video games.      

## Topics Explored
1. Define big data and describe the challenges associated with it.
2. Define Hadoop and name the main elements of its ecosystem.
3. Explain how MapReduce processes data.
4. Define Spark and explain how it processes data.
5. Describe how NLP collects and analyzes text data.
6. Explain how to use AWS Simple Storage Service (S3) and relational databases for basic cloud storage.
7. Complete an analysis of an Amazon customer review.

## Example
Example of AWS data pulled into pgAdmin using Google Colab and PySpark script:  
     
![review_id](https://github.com/zhangkevq/Amazon_Vine_Analysis/blob/main/images/review_id_table_pg4.png)

## Results

### How many Vine reviews and non-Vine reviews were there?
The dataset appears a little on the small side for Big Data with 145,431 reviews.
Only reviews with 20 or more votes where considered for the rest of the analysis leaving 3,342 reviews. 
Helpful votes were defined as being 50% or greater than the total votes narrowing the list to 1,685 reviews.

Unfortunately, due to the applied criteria, it significantly diminished the sample size.  In the remainder 1,685 reviews, there were no reviews that were paid for by the Vine program.     

![no_reviews](https://github.com/zhangkevq/Amazon_Vine_Analysis/blob/main/images/vine_count.png)     

All 1,656 remaining reviews are unpaid Vine with 0 paid Vine.  

### How many Vine reviews were 5 stars? How many non-Vine reviews were 5 stars?     
As for 5-star unpaid Vine reviews, there were 631 reviews.  Attempting to divide by zero, the code would result in a zero division error.  Therefore, there are also 0 paid Vine with 5-star reviews.     

### What percentage of Vine reviews were 5 stars? What percentage of non-Vine reviews were 5 stars?   
![5-star-percentage](https://github.com/zhangkevq/Amazon_Vine_Analysis/blob/main/images/unpaid_vine_program.png)   
The percentage of unpaid, 5-star Vine reviews resulted in 37.4%, while the percentage of paid, 5-star Vine reviews would be 0%.   

## Summary

Because the sample size was constricted to a degree that it was impossible to compare paid and unpaid Vine reviews, the analysis is biased towards unpaid Vine reviews.  Another indicator is comparing 37% of unpaid, 5-star Vine reviews to 0% paid, 5-star Vine reviews also shows that the unpaid Vine are biased as well.

The starting criteria of 20 likes or the 50% helpful criteria may have been too high, which made the data set too small.  Adjustments to these criteria is a first step to reconsidering using this data set.
