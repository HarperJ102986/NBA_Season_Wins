# NBA  season wins

Capstone: Jose Harper

## Main Files:
- NBA_season_wins.csv
- Presentation.pdf
- NBA_season_winsF.ipynb

### Stakeholder: 
I was hired by Houton Rockets Organization to explore other methods of predicting a team's season-long rank and what features contribute to that prediction from the data provided.

## Business problem: 
Most NBA sports algorithms try to predict winning each individual game instead of looking at the season as a whole. Algorithms only take into account features such as Points Allowed, Points For, Shooting percentage, Turnovers and Rebounds from the last 10 games or so. I must dig deeper and find out the best model to predict highest overall season wins and pull out the principal components that are highley correlated to most wins using stats from 1986 until the first half of the 2022 season stats.¶


# Data Understanding:
- I will be using data in the form of csv files from the site https://www.sports-reference.com/. I am using the teams data on 27 features/variables: 25 Continous, 1 categorical (team name), 1 binary (total wins).
- This data will be on the NBA. I will use 35 season starting from the 1986 season until the first half of the current 2022 season. Feature categories include: Pounts total, offensive rebounds, defensive rebounds, 3 point attempts, 3 pointers made, field goal attempts, field goals made, 2 point attempts, 2 points made, personal fouls, free throws, free throw attempts, assists, steals, blocks and turnovrs. I am going to utlize this information to predict the best winning record or "Rank". 

## Data Gathering
Went to site and scrolled down to "Share and Export" section of the team summary data.
copied and pasted that data into an Excel spreadsheet.
Made the data fit the format by using the "text to columns" function in Excel
Saved the data for that year and then repreated this for 35 NBA seasons to get enough data for modeling

### Data Preparation EDA 
-Step 1: Data consists of 2 separate data frames. data frame one contains 24 features. 1 categorical column (Team Name). Data frame 2 contains information that should be dropped. Drop: first row of int., player, position, nationality, and college.¶

-Step 2: create columns with list values with each teams Average weight, height, age, and experience.

-Step 3: Concatinate both data frames so that the features are all condensed for modeling

-Step 4: create new collumn with team wins for target value.

## Modeling
- Baseline Model
Strongest correlated feature starying with single regression model
RMSE: 47
R2: 37

- Model 4
Using all the data not from the multicolinearity assumption funtion to see if it can improve model metrics.
RMSE: 24
R@: 63

## Evaluate Models
- After running the 6 models I was able to determine that the 8 features multiple linear regression was the best model due to its high R squared value and lowest RSME.  

Using the best trained model which was the 8 feature multiple linear regression model since it was the best with an R squared value of .63 and the lowest RMSE or condition numbers. The key metrics in determining season high wins is 3 point percentage, high amount of total points per game scored, Field goal percentage, Rebounds, steals, and assists.


## Conclusions:
- The best features for ensuring the best possible record for the season in terms of wins would be over all points scored, 3 point field goals made, rebounds, steals and assists. 



## Future analysis:
- In future analysis I want to use an api that updates the stats in real time.
- Use a much smaller data set such as the last 10 seasons compared to 35. The game has changed drastically so the newer the information the better at predicting the best team for wins
- Also compare salary caps in terms of picking players (Drafting v trading). 
-Add features to data set such as average age, weight, and height for players that average at least 5 minutes per game. 

## For more information or questions, please reach out to Jose Harper at harper.jose@gmail.com

## Repository Structure
- .git
- .ipynb_checkpoints
- data
- .gitignore
- initial heatmap
- general presentation pdf
- NBA_Season_WinsF.ipynb
