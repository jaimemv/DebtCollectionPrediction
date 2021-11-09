# 1. Frame the problem
The objective of this notebook is fitting a model that predicts the likelihood of debtors to repay their debts within the next 12 months.

To achieve this objective, three separate models will be fitted to predict the likelihood of repay within the following 3, 6 and 12 months respectively.

Therefore the problem is a Classification one. Instead of training one Classifier to predict the likelihood to pay in the next 3, 6, 12 months or not pay at all, 3 independent binary classifiers will be fitted to get the likelihood of payment at each of the mentioned periods.

In terms of metrics, I consider the most important one optimise is **precision**. It is because at the time of establishing a budget allocation for the financial year, False Positives may lead the Company believe that can count with X amount of money collected back from debts.

Since I do not have perfect information about the dataset and I do not know which specific outliers may be miss-type or any other kind of error, some of them will be dropped in order to not blurry the model.

However, since debt collection is a sensitive issue, I would perform specific risk studies for each of the complex cases.

# Conclusions
- **Accuracy** oscillates between ~85%-94% for the three periods in advance. It is a good result.
- **Precision** ranges from ~48-66%. For 12 and 6 months in advance the results are fair. However for the 3 months in advance the results are poor, it is even better random guess. This result can be improved by testing new models, performing a more extensive data post-processing and of course by gathering more data.

# Further work

This project is a first approach to a robust debt collection Classificator. For further work I would continue by:

- Fitting and testing more models may lead to better results.

- The features of the data are a bit scarce so any algorithm may find hard to infere patterns from it. Adding more quality signals may bring a big improvement. Working closer to the Data Engineering team that establish the data collection criteria and the signals to be collected may be a handy solution.

- In order to make the model more reliable, data should be enlarged in both: (1) number of time-periods for currently included debtors and (2) more debtors.

- Talk to an expert who knows about the dataset to get a better understanding of it, potential erroneous values, etc.

- Perform oversampling of the undersampled target.
