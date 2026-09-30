# Five key insights

- Data quality: 52 duplicate rows were removed, leaving 48,790 records. Before deduplication, workclass, occupation and native country had 2,799, 2,809 and 857 missing values; these predictor values were retained as Unknown.

- Income is imbalanced: 76.1% earn <=50K and 23.9% earn >50K. A future model should be evaluated with precision, recall and F1 as well as accuracy.

- Education is associated with income: 41.3% of bachelor's graduates earn >50K, compared with 15.9% of high-school graduates. Education code has a correlation of 0.33 with the high-income indicator; this is an association, not proof of causation.

- The >50K group works an average of 45.5 hours weekly, versus 38.8 hours for the <=50K group. Their medians are 40 and 40 hours, respectively, so the distributions still overlap.

- Capital gain is zero for 91.7% of records. The >50K rate is 61.7% with positive gains and 20.5% with zero gains. Log features reduce the long tail; positive gains should not automatically be deleted as outliers.
