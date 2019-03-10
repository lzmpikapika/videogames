# videogames
The motivation for the project is to show game platform manufacturers the impact of changes in advertising spending on product sales. Creating a report, based on statistical models, linear models and random forest analysis of game data, comparing Nintendo and Sony and Microsoft's sales and advertising investment, and predicting the trend of Nintendo's advertising sales in 2019, planning a reasonable Nintendo company's advertising investment in 2019 Money interval. Based on descriptive analysis and predictive analysis, the project analyzes Nintendo's advertising investment amount, which is beneficial to increase consumer groups and increase profits in the most reasonable way.
## Introduction of the data
### We use 3  datasets from KAGGLE. Frome the datasets we can see all the gaming company data through 1985-2017. Include: rank of the company, global earning, Sales by region EU/NA/JP, Advertisement spending of each company, and Sales of different game types in different regions.


## Analysis Motivation
### Each game company will redeploy its future sales strategy based on sales in previous years in different regions. And the new sales strategy is often reflected in advertising investment. Based on this we will analyze based on known variables. Whether it is necessary to increase advertising investment in a certain region or a certain type of game in different regions according to past sales.


## Analysis report (Tools: STATISTIC ANOVA. Linear Regression. RandomForest)
### The first use of statistical models is to see how different variables affect the ultimate benefit of each company. 
### Through the statistical model ANOVA we can see that North American sales have the greatest impact on final sales (the highest proportion). At the same time, North America has the highest spending on shooting games. The Japanese market for role-playing games accounted for the highest proportion. Therefore, through the statistical model, it can be seen that when the shooting type game is put into the North American market, the advertising investment and publicity efforts can be increased to obtain higher profits.

### Second, we use a linear model to linearly analyze advertising spending and revenue across all regions. Through the linear model, we can see that the game market has a positive correlation between advertising investment and revenue. However, the game advertising investment in all regions is quite time-sensitive, that is, the game will generate huge profits in a short time. Then the yield curve will drop.

```{r pressure, echo=FALSE}
plot(lr )
```


### We can draw conclusions through statistical models and linear models. When launching a shooting game in North America, the game company should increase its advertising efforts in the initial stage to obtain the highest revenue. Of course, some small companies have a lot of player bases when they start the game, so scoring this variable has become very useful. When the game scores more than a certain amount, the sales of such games will also increase dramatically.



```{r}
library(rpart)
game1 = rpart(AD~EU_Sales + JP_Sales + NA_Sales, data = game,method = "anova")
summary(game1)
```


### Through the rpart we can see that most of the gaming company has very low error rate shows the solution was correcct and can used in most of the gaming saling stratigy.























Note that the `echo = FALSE` parameter was added to the code chunk to prevent printing of the R code that generated the plot.
