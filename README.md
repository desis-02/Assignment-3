Project Overview
This project is designed to analyze basketball player performance data to extract insights into shooting accuracies, efficiency, and defensive contributions across various seasons. The goal is to assist coaches, sports analysts, and fans in understanding player strengths and areas for improvement, helping in strategic planning and player development.

The data set contains the following performance metrics for basketball players:
FGM: Field Goals Made
FGA: Field Goals Attempted
3PM: Three Pointers Made
3PA: Three Pointers Attempted
FTM: Free Throws Made
FTA: Free Throws Attempted
PTS: Points
MIN: Minutes Played
BLK: Blocks
STL: Steals

Implementation - The script utilizes Python libraries, NumPy for data manipulation, and pandas for handling data in a tabular format. 

Key operations include:
Data Conversion: Columns are converted into NumPy arrays for efficient numerical operations.
Metric Calculation: Metrics like field goal accuracy, three-point accuracy, free throw accuracy, and averages per game or minute are calculated using NumPy.
Aggregation: Data is grouped by player and season to compute mean values of the metrics.
Code Structure -
Data Loading: Data is loaded from a CSV file into a pandas DataFrame.
Array Conversion: Key statistic columns are converted from pandas Series to NumPy arrays for computation. (to_numpy())
Metric Calculation:
field_goal_accuracy = np.divide(fgm, fga, where=fga!=0)
three_point_accuracy = np.divide(tpm, tpa, where=tpa!=0)
free_throw_accuracy = np.divide(ftm, fta, where=fta!=0)
average_points_per_minute = np.divide(pts, min_played, where=min_played!=0)
Grouping and Aggregation: Uses pandas' groupby method to aggregate statistics by player and season.
Output Generation: Summarizes the top results using head() method and prints them.
