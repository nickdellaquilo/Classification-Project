# Diagnosing Negative Ecommerce Reviews
Nicholas Dell'Aquilo

## Abstract
The goal of this project was to use classification models to determine the cause of negative reviews on an ecommerce website, with the goal of reducing customer churn. I used a [dataset from Kaggle](https://www.kaggle.com/olistbr/brazilian-ecommerce) to analyze features that correlated with negative reviews. I was able to create a logistic regression model that achieved some level of success, and measured its success upon multiple metrics.

## Design
This project is motivated by an [article](https://www.inc.com/andrew-thomas/the-hidden-ratio-that-could-make-or-break-your-company.html) that theorizes the effect that a single negative review can have on a business. In summary, an experience that is negative enough to lead to someone leaving a negative review almost always results in them not only ceasing to do business with a company, but to also tell others about said experience. It is estimated that a single negative review counteracts 40 positive ones, so in order to reduce customer churn, finding the cause of negative reviews must be a priority.

## Data
The dataset contains 100,000 rows with informaton on reviews of orders from an ecommerce website. The target class is engineered from the original review score, with a score of a 1 or 2 being considered negative, and a score of a 4 or 5 being considered positive. ~8,200 review scores of 3 were disregarded to retain simplicity and interpretability in the model. The 10 features used in the model include price paid, the length of text elements of a product, the number of photos on the product page, the item's weight, and its physical dimensions.

#### Feature Engineering:
* Converted review score into binary negative/positive target class. (Reviews with a score of 3 were removed)
* Multiplied length, width, and height features to measure volume

## Algorithms

The data was split into 80/20 train/test portions, and the training portion was upsampled to have an even split of positive and negative classes represented.

#### Models:
* Logistic Regression
* K-Nearest Neighbor

Of these, K-nearest neighbor appeared to score better, but isn't interpretable, and was likely overfitting, so logistic regression was tested on the holdout data.

#### Scores on holdout test data:
   * Accuracy: 0.53
   * Precision: 0.87
   * Recall: 0.54
   * F1: 0.66

## Tools
* Numpy
* Pandas
* Scikit-learn
* Matplotlib 
* Seaborn

## Communication
My code notebook can be found [here](https://github.com/nickdellaquilo/Classification-Project/blob/main/Code.ipynb).

My slide deck can be found [here](https://github.com/nickdellaquilo/Classification-Project/blob/main/Project-Presentation.pdf).

![image](https://user-images.githubusercontent.com/22899761/121682676-5f69d100-ca8a-11eb-8805-0ef8810e5ca1.png)
