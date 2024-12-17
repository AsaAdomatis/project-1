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
<p align="center"><img src="public/assets/images/touchdowns_vs_salary.png"/></p><br/>
<p>Looking at NFL position salaries, running backs (RB) earn approximately $1.5 million per year, placing them in the lower third of the pay scale. This relatively modest compensation compared to quarterbacks at $7 million, or guards and defensive ends at $4-5 million, raises an interesting question: how does actual performance impact RB salaries? This leads us to our next analysis examining the relationship between touchdowns and salary.
</p>
<p align="center"><img src="public/assets/images/touchdowns_vs_salary.png"/></p><br/>
<p>Looking at NFL position salaries, running backs (RB) earn approximately $1.5 million per year, placing them in the lower third of the pay scale. This relatively modest compensation compared to quarterbacks at $7 million, or guards and defensive ends at $4-5 million, raises an interesting question: how does actual performance impact RB salaries? This leads us to our next analysis examining the relationship between touchdowns and salary.
</p>
<p align="center"><img src="public\assets\images\Avg Salary v Types of Awards Won.png"/></p><br/>
<p>
Our visualization on avg. salary (mean cap hit) v. Types of Awards Won supports the observation that player who received awards earn on a higher cap hit.
</p>
<p align="center"><img src="public\assets\images\Fumbles v Cap Hit.png"/></p><br/>
<p>
Analyzing the relationship between fumbles and salary reveals a weak positive correlation of 0.22, with only 5% of salary variation explained by fumbles. Despite reaching statistical significance, the scattered plot and low R-squared value suggest that fumbles have minimal impact on a player's salary. 

</p>
<p align="center"><img src="public\assets\images\Predicted Rushing Attempts.png"/></p><br/>
<p>
Using prophet, we predicted 2019 mean rushing yards and compared them to actual results. Prophet predicted 340 mean rushing yards for 2019 when the actual was 324 mean rushing yards. The actual mean rushing yards decreased more than the predicted rushing yards.
</p>
<p align="center"><img src="public\assets\images\Total Rushing Yards for Running Backs.png"/></p><br/>
<p>
The regression of Total Rush Yards v. Salary Cap Hit revealed an r-value of 0.5325 meaning the total rush yards of NFL running backs has a moderate positive correlation to cap hit. The p-value of 0.0002 supports the statistical significance of the finding. This means that Total rushing yards is a significant component in determing a NFL player's salary.
</p>

