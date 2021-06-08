# Interpreting the Causes of Negative Ecommerce Reviews
## Classification Project MVP
#### Nicholas Dell'Aquilo

The goal of this project is to analyze a dataset of orders and reviews on an ecommerce website. In this analysis, the primary metric of analysis will be recall- I want to make sure I can identify all potential sources of negative reviews, even if there are some false positives. Precision is a lower priority; consider that if there is some negative feature associated with an order, not every customer will neccesarily leave a bad review because of it, but it is still important to identify it.

![image](https://user-images.githubusercontent.com/22899761/121262294-df711a80-c881-11eb-93cd-af956c8228ee.png)

According to the distribution of review scores, I will have to work to alleviate class imbalance in order to have a better model. Additionally, to make the model more interpretable and not as needlessly granular, I combined review scores of 1 & 2 and 4 & 5, and removed scores of 3. My model will therefore be binary and consider whether a review is negative or positive, respectively.

![image](https://user-images.githubusercontent.com/22899761/121261138-4f7ea100-c880-11eb-9085-f1c3cb95706a.png)

The above image visualizes the accuracy(0) and precision(1) of a KNN classification model. This is relatively few neighbors for the size of the sample (52,000), but informs how I might choose to evaluate my model in the future.

In my final project, I also aim to use a logistic regression model, as well as decision tree and random forest models.

The code for my MVP is located [here](https://github.com/nickdellaquilo/Classification-Project/blob/main/MVP.ipynb).
