# NBA maximum season wins


## Business Understanding
Capstone: Jose Harper

## Main Files:
- NBA_season_wins.csv
- Presentation.pdf
- NBA_season_wins.ipynb

### Stakeholder: 
NBA Team Analyst or Scout hired by lower rank team to figure out the best way to increase wins per NBA 2022 season based on 27 features. I must help them predict the best draft picks along with what potential trades could make for a better winning outcome for the over all season.

## Business problem: 
Most NBA sports algorithms try to predict winning each individual game instead of looking at the season as a whole. Algorithms only take into account features such as Points Allowed, Points For, Shooting percentage, Turnovers and Rebounds from the last 10 games or so. I must dig deeper and find out the best model to predict highest overall season wins and pull out the principal components that are highley correlated to most wins using stats from 1986 until the first half of the 2022 season stats.¶


# Data Understanding:
- I will be using data in the form of csv files from the site https://www.sports-reference.com/. I am using the teams data on 27 features/variables: 25 Continous, 1 categorical (team name), 1 binary (total wins).
- This data will be on the NBA. I will use 35 season starting from the 1986 season until the first half of the current 2022 season. Feature categories include: Pounts total, offensive rebounds, defensive rebounds, 3 point attempts, 3 pointers made, field goal attempts, field goals made, 2 point attempts, 2 points made, personal fouls, free throws, free throw attempts, assists, steals, blocks and turnovrs. I am going to utlize this information to predict the best winning record or "Rank". 

## Data Gathering
Since the sports-reference sites API code was not working and I could not debug in time I had to manually scrape the data from each webpage to get the season data from 1986-2022. I did this by creating a CSV file for each season and importing it into an excel spreadsheet. After doing that to each season I then did preprocessing for the data. 

### Data Preparation EDA 
Step 1: Data consists of 35 separate data frames. data frame each contains 24 features. 1 categorical column (Team Name). 
Step 2: Concatanate all 35 data frames using glob tool to condense the dataframe for modeling. 
Step 3: Drop all columns with Null values
Step 4: Change the Target value or Rank to ordinal data so that the algorithm can use the data properly.
step 5: Plot heatmap to show which features have high multicolinearity
step 6: set up scatter plots of the features to the target values to show linear correlation (if any)
step 7: create baseline model from simple linear regression
step 8: make multiple variable linear regression models
step 9: make classifier models

## Modeling
- LR model: Run train, test split with entire data set for features as X value, as for the Y value being the target value (Wins).

- Hand picked LR (Test set features: added average teams height, weight, age, and experience And drop features that are highley multicolinear).

- Created  function to do 4 models at once. I used Random forest, KNearest Neighbors, decision Tree and XGX gradient boost classifiers.

## Evaluate Models
- After running the 4 models I was able to determine that the 8 features multiple linear regression was the best model due to its high R squared value and lowest RSME.  

Using the best trained model which was the 8 feature multiple linear regression model since it was the best with an R squared value of .89 and the lowest RMSE or condition numbers. The key metrics in determining season high wins is 3 point percentage, high amount of total points per game scored, Field goal percentage, Rebounds, steals, and assists.


## Conclusions:
- The best features for ensuring the best possible record for the season in terms of wins would be over all points scored, 3 point field goals made, rebounds, steals and assists. 

-Since 


## Future analysis:
- In future analysis I want to use an api that updates the stats in real time.
- Use a much smaller data set such as the last 10 seasons compared to 35. The game has changed drastically so the newer the information the better at predicting the best team for wins
- Also compare salary caps in terms of picking players (Drafting v trading). 
-Add features to data set such as average age, weight, and height for players that average at least 5 minutes per game. 

## For more information or questions, please reach out to Jose Harper at harper.jose@gmail.com

## Repository Structure
