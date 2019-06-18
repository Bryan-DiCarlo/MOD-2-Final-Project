# MOD 2 Final Project Submission
* Student name: Bryan DiCarlo
* Student pace: Full Time Online 4/15/19 Cohort
* Scheduled project review date/time: Tuesday June 18 @ 12:30pm
* Instructor name: Rafael Carrasco
* Blog post URL: https://bryan-dicarlo.github.io/hypothesis_testing_and_the_northwind

# Introduction
* For this project, we will be working with the Northwind database--a free, open-source dataset created by Microsoft containing data from a fictional trading company.
* Data will be gathered from the database using SQL queries.  After exploring the data, important Business questions will be posed and answered using hypothesis testing

# Methodology: 5 steps for the Scientific Method and Hypothesis Testing
1. In each section a general business question will be posed and then investigated.
2. The data to answer the question will be drawn from the database through SQl queries and explored through EDA
3. The hypothesis to be tested will be formulated and stated.  All hypothesis testing will be done at the $\alpha$ = 0.05 level
4. Testing the hypothesis.  The appropriate hypothesis test for each question will be determined. The undelying assumtions of each test will be examined.  The hypothesis will be tested using the appropriate test for each question.
5. The results will be analyzed and it will be determined if we have evidence to reject the null hypothesis or fail to reject the null hypthesis based on the evidence.  Results will be stated.  Conclusions that can be drawn from the experiment will be reported

# Questions to be Explored
1. Do discounts have a statistically significant effect on the number of products customers order? Part B: What levels of discounts are significant compared to No Discount?
2. Investigating the Revenue Generated from the Different Regions Northwind Serves. Are there differences?
3. Split the Northwind customer base into The Americas and Greater Europe to compare spending and revenue from customers on different sides of the globe. Do we find any differences?
4. Analyze the number of products sold from each of Northwind's product categories. Do sales differ between product categories?
5. Compare Average Sales Totals from 2012-2013 to 2013-2014. Is there statistically significant revenue growth?
6. Some interesting questions for future work.  I briefly investigate employee sales below.  It would also be important to know the performance of Northwind's three shipping companies. Data is incomplete but I start this analysis below.

# Question # 1: Conclusions
* After exploring the Data a difference in the average size of Discounted vs Non-Discounted orders was noticed
* The data was explored to identify the most appropriate hypothesis testing method to test this difference
* The data was well suited for a two sample t-test with unequal variance.
* Our test indicated that the p-value was much less than .05 and we could reject the null hypothesis with a high degree of confidence
* Post hoc analysis seems to confirm this result
* One suprising observation was the Cohen's d statistic. The value was small indicating a small effect size even though our p-value was extremely small.  This is probably due to our large sample size.  Even though the overall effect was relatively small, due to the large sample size, the difference was still statistically significant.
* This gets to the point of properly interpreting p-values and the Cohen's d statistic.  One does not imply the other.  You can have a small effect size and still have very low p-values and high degree of statistical significance.  You are very confident this difference did not happen by chance (as incicated by your p-value).  The difference we measured is still statisticaly significant but the overall difference between the two sample is relatively small as shown by the Cohen's d statistic.

# Question # 1 B: Results and Conclusions
* The null hypothesis can be rejected for all discont levels other than 10%. When compared to the control group no-discount.
* We failed to reject the null hypothesis at a discount level of 10%
* Discount levels of 5%, 15%, 20%, and 25% all showed statistically significant differences in order quantity
* This hypothesis test was set up as two tailed test.  However inspection of the means shows that the mean for discounted order quantities is greater than that for the non discounted group
* It can be infered (not proven) that the statistically significant differences seen in this test indicate higher order quantities for the discount levels where the null hypothesis was rejected.

# Question # 2: Results and Conclusions
* The null hypothesis was rejected for Western Europe when compared To Southern Europe And South America.
* Again, this test is set up as a two tailed test. The mean order amount is greater For Western Europe than either of these regions. This difference can be interpreted that the order amounts are significantly higher than those from Southern Europe and South America. (inferred not proved!)
* The null hypothesis was also rejected for North America compared to Southern Europe.  This can also be inferred as positive difference. The mean order amount from North America is higher than that of Southern Europe.  Our test shows that this difference is unlikely from chance alone.
* Also, it should be noted that some regions have substantial differences in means.  However, the Tukey's test was unable to reject the null Hypothesis.  This give us evidence of the stringency built into the Tukey's test.  Even though the difference in means was relatively large.  Tukey's failed to reject the null hypothesis.  This is likely because those samples did not fully meet the underlying assumptions and were penalized.  That is the power of this test
* It can be seen from the graphs above that customers in Western Europe are the biggest contributor to Northwind’s Revenue.
* It should also be noted that North America, The UK, Northern Europe and South America all have high mean order amounts although they spend less overall than Western Europe.
* Perhaps marketing should be increased these four areas.  These areas are already buying products from Northwind in high amounts when they do order.  Increased Marketing could increase the overall number of orders from these areas.
* Another Consideration is to do some market research and perhaps introduce more products that are important to people in these regions.
* These regions are ordering in quantity when they do place orders. Research and marketing can identify products and strategies to increase the overall revenue from these regions.


# Question # 3: Results and Conclusions
* We failed to reject the null hypothesis
* This indicates that the mean order amounts form the Americas and Greater Europe do not differ statistically
* In fact it appears that the mean order amounts from from these two areas of the globe are very similar
* Failing to reject the null hypothesis in this investigation is not bad news for Northwind
* It is good news, and why it was important to investigate this question
* Northwind Traders is an International trading company
* It is great news to know that the average amount for orders placed was similar for different areas of the customer base
* While Western Europe still produces the highest overall revenue.  It is good to know that average order amounts are still high in many areas.
* This means that Northwind’s products are appealing to many regions.  Customers are ordering.
* Steps can be taken in marketing and product development to enhance the total sales in other regions


# Question # 4: Results and Conclusions
* We failed to reject the Null Hypothesis in all comaprisons
* This indicates that the mean order size is similar across all categories
* This is actually good news for Northwind
* This means that no individual Product Category is lagging behind the others in terms of quantities ordered
* All product categories seeem to be selling equally well in terms of quantity per order

# Question # 5: Results and Conclusions
* Average order totals were slightly higher in the second half. 
* However, a statistically significant difference was not seen, and we failed to reject the null hypothesis
* We are working with data from a limited time period, more data would certainly help us gage the revenue growth for Northwind
* We had to split our data into data into equal groups for fair comparison.  We compared the average order totals for the first half group and compared with the second half group.
* As the table below illustrates this was a fair comparison.  Total revenue and average order totals were slightly higher for the second half group in both cases.  In roughly the same proportion.
* These increases were not at a level where a statistically significant difference could be found.
* Overall it appears that Northwind made progress form the first half to the second half.
* Multi-year data split into months or quarters would be a great help to judge Northwind’s revenue growth in the future

# Conclusions
* It was found that discounts do have a statistically significant positive effect on the number of items ordered
* It was found that the levels of discount with a statistically significant effect were 5%, 15%, 20%, 25%
* Interestingly 5% discount had roughly the same effect as 25% discount.  Further investigation and experimentation could help narrow down the lowest discount level that still produces these results.  This would help profit margin
* It was found that average orders were statistically higher for western Europe compared to South America and Southern Europe. A statistical difference was also seen for North America and Southern Europe
* Western Europe contributes the most revenue to Northwind's bottom line.  However, several other regions were found to have average order amounts close to Western Europe. Since these regions are already have high order totals, future marketing could help increase overall spending in these regions.
* We divided up the orders from the customer base into broader regions.  the Americas and greater Europe.  No statistical difference in order amounts was seen.
* This can be viewed as a positive sign. Northwind is a global trading company. One would hope that sales do equally well around the globe.  We found evidence that this is likely the case.
* We also compared average sales among the different product categories.  No statistical difference was seen. Again, this can be viewed as good news.  As a company we would like all the products we offer to sell equally well.  This indeed appears to be the case
* We also split the orders into first half and second half.  To investigate if revenue has grown.  No statistical difference was found. However, it does appear that total revenue and average amount per sale is trending upward.

#  Business Recomendations
* Discounts Increase Sales
* Do more experimentation with discounts.  Find the lowest discount that consistently drives sales. This will increase profit.
* Market more to the US, the UK Northern Europe and South America. These countries already have large quantities per order.  Marketing can increase the number of orders and the overall revenue from these regions.
* Product categories seem to do equally well overall.  It would be interesting to test some market specific product launches. Test to see if this increased overall revenue by boosting regional sales.  
* Get more multi-year sales data so we can better track the growth of Northwind.
* Get arrival times for shippers. Delivery time is important for customer satisfaction

# Future Directions
* Certainly, Multi-year data would be very useful in future analysis
* This would be useful for many different analyses.  Keeping track of revenue growth chief among them
* It would also be nice to add more quantitative business metrics to our database
* Business Metrics that you would normally see in quarterly or yearly business report.
* There are very few Quantitative measures contained in the database. In most case data had to be connected back with order amount and quantity. As there were some the only quantitative features that could be measured
* Adding more useful information like the shipping information I explore below

# Final Notebook: BD MOD2 Project.ipynb
