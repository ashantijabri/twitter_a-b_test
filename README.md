# **New Ad Product A/B Testing Results Analysis**
### *Project lead by Ashanti Jabri*

### **Introduction**

Twitter provides a platform where businesses can create advertising ​campaigns​ to increase awareness of their brands or to increase adoption of their products or services. Our current ad product operates in the manner in which advertisers pay us each time a user clicks on their ad.

Each campaign has a ​budget​ (how much money the advertiser is willing to spend during a period of time). An advertiser never has to pay more than their budget, so if we were to spend more than the campaign’s budget, we would not be able to bill the advertiser for the additional spend. This is called ​overspending​. Since Twitter only charges advertisers for actual clicks on their ads, the charges can take a while to enter into the system after some (random) delay. For example, suppose a campaign has $10 of the budget remaining and the ad serving systems serves out 1000 ads, expecting 10 of them to generate a click resulting in 1 of revenue each. If however, 20 ads end up generating clicks, we would receive 20 worth of events and not be able to bill the advertiser for 10 of them. Ultimately, this implies Twitter has “wasted” 10 worth of ad placements and therefore has incurred a cost.

We have been noticing an increase in overspend on the platform. In an attempt to reduce the amount of overspend, we decided to create a new product where advertisers pay each time their ad appears in a user’s viewport rather than each time it is clicked on -- presumably these engagements would be received at a lower latency. To test the new product, we ran an A/B test. We randomly split the advertisers on the platform. Half of the
advertisers remained on the old product and half received the new product. A week later we have some data and want to determine whether or not the experiment was a success.

### **Hypothesis**
Null hypothesis (H0): Twitter ad campaigns that receive the new product will not reduce overspending compared to campaigns that receive the old product.

Alternative hypothesis (H1): Twitter ad campaigns that receive the new product will reduce overspending compared to campaigns that receive the old product.

### **Success Metric**
For an ad campaign with a \$3 million budget, 1%, 2%, and 3% overspend would be \$30,000, \$60,000, and \$90,000 respectively. For the purpose of this analysis, a new product that could save Twitter even 1% of overspend would be largely beneficial. So for the sake of our experiment, we'll consider the new product a success if overspend is reduced by at least 1%.

### **Methodology**

I'll use a series of methods to determine if we can reject our Null hypothesis:

- We'll conduct in-depth Exploratory Data Analysis to gain insights into our data that could shape or skew our results.

- Check for Randomization, Selection, and Confounding Bias, to ensure that our treatment groups were properly split for testing purposes.

- Conduct the hypothesis test using ANOVA and Kruskal tests.

- Determine Feature Importance using Random Forest Regression.
