# Data Analyst

At Dozee, our mission is to improve the quality of life through continuous health and well-being monitor. Our sensor tracks the quality of sleep and body vitals while a user is sleeping.

You are given 10 CSV files. Each CSV file contains the data from one night’s sleep. The length of the sleep can be variable depending on how much a person sleeps that night.

Dozee measures the vitals of a person like heart rate (HR), breathing rate (BR) and multiple other parameters in every 30 seconds (1 epoch) while they are asleep.

Each given CSV have multiple rows, depending on the length of sleep. The number of rows can be found by this formula:

** n_rows = sleep_duration (in seconds) / epoch_duration (30 seconds) **

**Example:** If sleep is of 7 hrs 25 minutes, the number of rows = 890 rows

Each CSV will have 3 columns:

**Time coordinate**

1. epoch_unix_timestamp (https://www.epochconverter.com/)

**Features**

2. epoch HR (beats / minute)
3. epoch BR (breaths / minute)

**Tasks**

You have to run an analysis on every sleep individually, on a non-overlapping window of 1 hour, for each feature individually. If the duration of the sleep is not an exact multiple of 1 hour, let the last window be of the remaining duration. Your analysis should achieve the following tasks for each feature separately:

1. Find certain statistics for the data in the given window that helps in identifying the trend of data in that window. For example, whether the HR is rising or falling or is stable or erratic in that window. It could be simple descriptive statistics or higher order statistics.

2. When completed with task 1 successfully, you will have the statistics (call it features) for every window for every sleep and for every feature. For example, if all the 10 sleeps are 8 hours each (for every sleep, 8 windows of 1 hour) then you will have 80 windows. And let’s assume that you have made 2 statistical values for a feature, say HR, in task 1, you will have 2 values for each of these 80 windows. Classify users based on the features extracted from task 1.

3. Based on the classes made in task 2, look at the points falling in each class and give an explanation as to what kind of data that class might represent and associate an appropriate label to that class.

4. Visualize your results in the best possible way, using python or MS Excel or GoogleSheets - showing the class in which each hour of every sleep is falling and the label given by you to that class, featurewise.

5. Some of the CSVs have anomalies in them, such as gaps in the data, outliers, etc.. Figure out the best possible way to tackle them.
