# Predicting the type of physical activity (eg, walking, climbing stairs) from smartphone triaxial accelerometer data

## Input Data
The input data used for training in this project consists of two files. The first file, train_time_series.csv, contains the raw accelerometer data, which has been collected using the Beiwe research platform, and it has the following format:

- timestamp, UTC time, accuracy, x, y, z

The second file, train_labels.csv, contains the activity labels contains the activity labels.  These labels are used to train your model. Different activities have been numbered with integers. We use the following encoding: 1 = standing, 2 = walking, 3 = stairs down, 4 = stairs up. Because the accelerometers are sampled at high frequency, the labels in train_labels.csv are only provided for every 10th observation in train_time_series.csv.

## Activity Classification
This code classify different physical activities as accurately as possible(>93%). 

```python
print(pd.crosstab(y_test, preds, rownames=['Actual Result'], colnames=['Predicted Result']))
Predicted Result  1   2   3  4
Actual Result                 
1                 5   0   0  0
2                 0  41   1  1
3                 0   0  18  0
4                 0   0   0  9

print(accuracy_score(y_test, preds))
0.9733333333333334
```

### All rights reserved
All rights of use are reserved, so any copy must be made with the permission of the author.

### Web Page
[personal website](https://raulaviles.netlify.app/)