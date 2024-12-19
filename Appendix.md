# Appendix

## A. Additional References

- [Kaggle] (https://www.kaggle.com/datasets/f4k25g/nfl-salaries)

- [Pro Football References] (https://www.pro-football-reference.com/years/2017/rushing.htm)

- [Official NFL Stats] (https://www.nfl.com/stats/player-stats/category/rushing/2017/REG/all/rushingyards/DESC)

- [Stathead] (https://stathead.com/football/player-season-finder.cgi?request=1&year_min=2017&year_max=2017&positions%5B%5D=rb)

## B. Terminology

- API : Kaggle used for 2014 thru 2020 Running back salary data
- API : Pro Football Reference used to gather 2017 - 2018 running Players statistics
- API : Official NFL Stats used to gather 2017 - 2019 Actual NFL Player Statistics
- API : Stathead provided 2017 - 2018 player position Data

## C. Dataset Information 

## This code snippet is building a clean and organized dataset of 2017 NFL rushing:
    Data Collection: It starts by scraping data from a website (https://www.pro-football-reference.com/years/2017/rushing.htm) which contains NFL rushing statistics. This data is then stored in a Pandas DataFrame called df_2017_NFL_Rushing.
  Data Cleaning: The code then cleans the data to make it more usable. This includes:
Simplifying the column names.
Removing extra spaces in column names.
Replacing missing values (NaN) in the 'Age' and 'Rk' columns with 0.
Converting specific columns (Player, Tm, Age, Rk) to appropriate data types (string and integer).
Adding a new column 'Year' with the value 2017 to indicate the year of the data.
Data Saving: Finally, the cleaned data is displayed using display(df_2017_NFL_Rushing.info()) and display(df_2017_NFL_Rushing.head(5)). It is then saved to a CSV file named 2017_nfl_rushing.csv in the 'output' directory.

## Combining data about NFL players' rushing statistics and their salaries for the year 2017.
    Import and Clean Rushing Data: It starts by importing data about NFL players' rushing performance from a website. It cleans this data by simplifying column names, handling missing values, and ensuring correct data types.
Import and Clean Salary Data: Next, it imports data about NFL players' salaries from a CSV file. It also cleans this data by removing leading/trailing spaces from column names and converting relevant columns to the string data type.
Merge Rushing and Salary Data: The most crucial step is to merge these two datasets into a single DataFrame. It uses an "inner join" based on the 'Player' and 'Tm'(team) column. Meaning it only keeps rows where a player is found in both the rushing and salary datasets.
Export Merged Data: Finally, it saves the merged data, containing both rushing statistics and salary information, into a new CSV file.


