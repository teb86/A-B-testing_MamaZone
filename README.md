# A-B-testing_MamaZone
A/B test based on the convert rate to decide whether to launch a new web page or not
<h3>Project:</h3>

MamaZone.com has developed a new web page in order to try and increase the number of users who "convert," meaning the number of users who decide to pay for the company's product. My goal is to work through this notebook to help the company understand if they should implement this new page, keep the old page, or perhaps run the experiment longer to make their decision.
<h3>Content:</h3>

* Ckecking-up (exploring and cleaning)
* A/B test
* Regression
<h3>Packages:</h3>

Python 3 + pandas, numpy, random, matplotlib, statsmodels.api
<h3>Steps:</h3>

* A/B testing:<br>
I will assume under the null hypothesis, p_new and p_old both have "true" success rates equal to the **converted** success rate regardless of page - that is p_new and p_old are equal. Furthermore, I will assume they are equal to the **converted** rate in **ab_data.csv** regardless of the page. <br><br>
I will use a sample size for each page equal to the ones in **ab_data.csv**.  <br><br>
Then, I will perform the sampling distribution for the difference in **converted** between the two pages over 10,000 iterations of calculating an estimate from the null.  <br><br>

* Regression:<br>
The goal is to see if there is a significant difference in conversion based on which page a customer receives.  
First, I needed to create a column for the intercept, as well as a dummy variable column for which page each user received (1 when an individual receives the treatment and 0 if **control)
 Then, I fitted the model and printed the statistical output.
After that, I found it useful to add another variable, which is the location in order to see the effect based on which country a user lives. 
