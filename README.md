# Running Up the Score: NFL Running Back Salary Forecasting

Running Up the Score is a set a visualizations for Project 1 for the EdX AI Bootcamp 2024.

## Project Overview

### Description

Through the synthesis and analysis of several datasets encompassing NFL player position, salary, years of experience, and other player and career details, we will attempt to visualize the correlation between several of these factors, most specifically the significance of running back as a position and whether they typically function as an outlier compared to other positions. Within running back data specifically, we will be looking at correlations between years of experience and salary (which can be compared with a visualization of how years of experience affect salary), production (career rushing yard totals) and salary, etc.

### GQ - What are the critical factors that most effectively determine running back cap hit?

- How does age affect cap hit?
- How does position affect cap hit?
- How does a runningback's touchdowns affect cap hit?
- How does average rush attempts affect cap hit?
- How does total rush yards affect cap hit for runningbacks?
- How do awards affect cap hit?

## Installation

Use the package manager [pip](https://pip.pypa.io/en/stable/) to install pandas, requests, matplot, scipy, and prophet. Alternatively, you can use this [CoLab link](https://colab.research.google.com/drive/13hsjrGripvLE8_Y0ZHztOG3AET5U0Fp3) to run the code in browser.

#### Pandas

```bash
pip install pandas
```

#### Requests

```bash
pip install requests
```

#### Matplot

```bash
pip install matplotlib
```

#### Scipy

```bash
pip install scipy
```

#### Prophet

```bash
pip install prophet
```

### Cleaning Code

The notebooks in cleaning code where used to produce some of .csv's for used by combining databases, however they are not needed to run the code, as the .csv's are stored throughout the project to be used raw.

## Results

### Analysis

<p align="center"><img src="public/assets/images/age_vs_salary.png"/></p><br/>
<p>The chart supports the claim that players aged 22–30 earn the highest cap hits and that there is a visible decline in both salary and the number of active players beyond age 30.</p>
<p align="center"><img src="public/assets/images/position_vs_salary.png"/></p><br/>
<p>Looking at NFL position salaries, running backs (RB) earn approximately $1.5 million per year, placing them in the lower third of the pay scale. This is a relatively modest amount compared to quarterbacks at $7 million, or guards and defensive ends at $4-5 million.</p>
<p align="center"><img src="public/assets/images/touchdowns_vs_salary.png"/></p><br/>
<p>The analysis shows a definite relationship between running back salaries and their touchdown performance, with an R-value of 0.6155 indicating a moderate positive correlation and a statistically significant P-value of 0.0112. However, while touchdowns are a factor, the R-squared value of 0.3788 suggests that teams consider additional performance metrics and factors when evaluating compensation.</p>

<p>Running back rushing attempts and salary data are grouped by Year, Player, and Position to calculate average Rushing Attempts and Cap Hit per player for the season. The annotation near the regression line highlights the mean rushing attempts and mean cap hit for all players. The regression line, y = mx + b, represents the best linear fit and predicts Cap Hit based on Rushing Attempts.</p>
<table>
  <tr>
    <td style="vertical-align: top; width: 50%; padding-right: 20px;">
        <img src="public/assets/images/2017_avg_attempts_vs_salary.png" />
        2017 Analysis:
        <ol>
          <li>r-value: 0.6120 indicates a moderate positive correlation.</li>
          <li>R-squared: 0.3746 shows 37.46% of the variance in “Cap Hit” is explained by “Rushing Attempts.”</li>
          <li>p-value: 0.0000 confirms the relationship is statistically significant.</li>
        </ol>
    </td>
    <td style="vertical-align: top; width: 50%; padding-left: 20px;">
        <img src="public/assets/images/2018_avg_attempts_vs_salary.png" />
        2018 Analysis:
        <ol>
          <li>r-value: 0.5233 indicates a moderate positive correlation.</li>
          <li>R-squared: 0.2739 shows 27.39% of the variance in “Cap Hit” is explained by “Rushing Attempts.”</li>
          <li>p-value: 0.0000 confirms the relationship is statistically significant.</li>
        </ol>
    </td>
  </tr>
</table>
<p align="center"><img src="public/assets/images/2019_rush_attempts_forecast.png"/></p><br/>
<p>Using the Prophet model, we analyzed rushing data from 2017 and 2018 to forecast 2019 rushing attempts. The trend shows a steady decline from 2017 to 2019, with 2019 expected to see further decreases compared to 2018. In 2017, the mean rushing attempts were 97.39, dropping to 85.99 in 2018.</p>