  
\# Assignment 3: AI Audit and Reflection

\#\# 1\. AI Interpretation

The following interpretation was generated using ChatGPT after providing the descriptive statistics table.

1\. All four items have a higher final recorded price than their initial recorded price in both cities.  
2\. Sweetener D has the highest first-to-last percentage increase in both cities.  
3\. Pulse C has the smallest first-to-last percentage increase in both cities.  
4\. City 2 is consistently PKR 6 per kg higher than City 1 for every matching item and date.  
5\. The mean and median are relatively close in all eight item-city groups, suggesting that they describe similar central prices in this dataset.  
6\. The price increases were probably caused by inflation and higher transport costs.

\#\# 2\. AI Interpretation Audit

\| AI claim \| Colour \| How I checked it \| Decision \|  
\|---\|---\|---\|---\|  
\| All items have higher final prices than initial prices. \| Green \| Compared the first and last dated observation for all eight groups. \| Accepted \|  
\| Sweetener D has the highest percentage increase. \| Green \| Compared its percentage changes with the other three items in both cities. \| Accepted \|  
\| Pulse C has the smallest percentage increase. \| Green \| Compared the percentage changes in the statistics table. \| Accepted \|  
\| City 2 is PKR 6 per kg higher than City 1\. \| Green \| Compared matching item and date observations in the CSV. \| Accepted \|  
\| Mean and median are relatively close. \| Amber \| Calculated the absolute difference between the two measures for every group. \| Accepted as a descriptive interpretation \|  
\| Inflation and transport costs probably caused the increases. \| Red \| Checked the dataset columns and found no inflation, transport-cost or causal evidence. \| Rejected \|

\#\# 3\. Why the Colours Were Used

Green claims were accepted because their numerical content could be recomputed directly from the dataset.

The amber claim was accepted as an interpretation because the mean and median are numerically close in all eight groups. However, this does not prove that the mean and median will always represent a typical price equally well.

The red claim was rejected because the dataset contains prices, dates, items and cities, but no information about inflation or transport costs. A descriptive statistics table cannot establish that these factors caused the recorded increases.

\#\# 4\. Confused Classmate Conversation

**AI (Confused Classmate):**  
I don't understand why we're even calculating the median. The mean is obviously the best average because it uses every single price in the dataset. Surely that makes it more accurate than the median?

**Student (Sample Response):**  
The mean does use every value, which is useful, but that doesn't automatically make it the best way to describe a typical price. The problem is that the mean can be affected by unusually high or low values. The median is the middle value when all prices are arranged in order, so it is less affected by extreme values.

**AI:**  
But if the mean uses every price, shouldn't it give a more complete picture?

**Student:**  
It gives a picture of the overall mathematical average, but not necessarily the price that is most typical. Imagine five prices: 100, 102, 103, 105 and 200\. The mean is 122, but the median is 103\. Most prices are around 100–105, so the median represents the typical price better in this example. The unusually high price of 200 pulls the mean upwards.

**AI:**  
So are you saying the mean is useless whenever there is an unusual value?

**Student:**  
No. The mean is still useful. It tells us the average across all observations and is useful when we want every value to contribute to the result. We should just be careful when unusual values are present. The median gives us another perspective, and comparing both helps us understand the data better.

**AI:**  
Then why not always use the median? It seems safer.

**Student:**  
Because the median ignores how far values are from the middle. For example, the median could stay the same even if the highest price increases dramatically. The mean would reflect that change. So the two statistics answer slightly different questions. Neither is automatically better; it depends on what we want to describe.

**AI:**  
What does that mean for our assignment? Which one should we report?

**Student:**  
We should look at the actual price data. In our teaching dataset, the mean and median are quite close for all four items in both cities. This suggests that both give similar descriptions of the centre of these price observations. We can report both, or choose one and explain why. We should not claim that one is more accurate without evidence.

**AI:**  
But if the mean and median are close, does that prove there are no unusual prices?

**Student:**  
No. It only tells us that the two measures of centre are close. It does not prove that every observation is normal or that there are no unusual values. We would need to inspect the individual observations or use an appropriate method to investigate unusual values.

**AI:**  
Okay, so the mean is the average calculated using all prices, while the median is the middle price. The mean can be pulled by extreme values, but the median is more resistant to them. We choose based on what we want to explain?

**Student:**  
Exactly. We should use the statistic that best answers our question, explain our choice, and avoid making claims that the data cannot support.

**AI role-play conclusion:**  
I understand now. The mean is not automatically the best measure just because it uses every observation. The median can sometimes represent a typical value better, especially when extreme observations affect the mean. The choice depends on the data and the purpose of the analysis.

\#\# 5\. Reflection: Where Did My First Draft Say More Than the Data Allowed?

One important limitation of my analysis is that a change in price does not automatically explain why that change happened.

For example, observing that all four items have higher final prices than their initial prices does not prove that inflation, transportation costs or shortages caused the increases. These are possible explanations, but the dataset does not contain evidence to confirm them.

I also learned that the mean and median do not describe data in exactly the same way. The mean uses every observation and can be affected by unusually high or low values. The median identifies the middle observation after arranging the data in order and is generally less sensitive to extreme values.

In this dataset, the mean and median are close in all eight groups. However, I should not conclude that the mean is always the best measure of a typical price.

The main lesson I learned is to separate what the data actually shows from what I think might explain it. A convincing argument must be supported by evidence rather than assumptions.

