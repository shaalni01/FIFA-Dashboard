# Section 1: The Dashboard
Almost every business can benefit from having a dashboard that aligns with their objectives. organizations, like FIFA, must even consider multiple dashboards for different departments to keep track of activities. The main purpose of this dashboard is to provide a comprehensive snapshot of performances.

This dashboard is majorly used by sports analysts, Football fans, Sports Channels, Football Coaches, Football club management, and of course football players.

The dashboard consists of 10 visualizations. They are discussed below.

`Preferred Foot`: This visualization compares the percentage of preferred foot of different players. It was found that majority of players preferred right foot.

`FIFA Strategy`: Each club has different strategies in their gameplay. The most used strategy is found to be ‘defensive’. 

`Player Position`: Different players has different positions in the football field. It was found that Strikers are more in FIFA.

`Player Potential in each Club`: The plot shows the potential of each player for the selected club.

`Identifying the Nationalities in each Club` 

`Most Valuable Players`: The plot shows top players of all time based on their value.

`Players with Highest Penalties`: The plot shows the players with highest number of penalties.

`Wage Distribution`: The plot shows the distribution of wages of each player.

`Age Group Distribution`: The plot shows the distribution of ages of players during FIFA 19.

# Section 2: The Dataset
The dataset selected is ‘FIFA 19 Player dataset’ which is available at ‘Kaggle’ that gives information about every player that has played FIFA 2019. The dataset has detailed information on each player’s stats, club, joined data, nationality, and income. The dataset has around 18000 datapoints and 89 columns, which we will be pre-processing to obtain quality well-formed data. 

**i.	Dataset Attributes**

The description and the data type of each column is as specified below,
1.	`ID` – (Interval) – the ID column has unique values.
2.	`Names` – (Nominal) – the names column consists if the players’ full names.
3.	`Age` – (ratio) – the range of the age column is 29 with minimum age being 16 and the maximum age is 45.	
4.	`Nationality` – (Nominal)- has 164 unique nationalities with England being the most common.
5.	`Overall Rating` – (ratio) – integer values with 46 being minimum rating and 94 being the maximum rating in the dataset.
6. `Potential Rating` – (ratio) – similar to overall rating with min value: 48 and max value: 95
7.	`Club` – (Nominal) – There are 651 different clubs in the dataset with FC Barcelona being the most common.
8.	`Value/wage` – (Ratio) – current market value and current wage of the player.
9.	`Preferred Foot` – (Nominal) – it has 2 values either left or right.
10.	`International Reputation` – (Ordinal) – It is a rating on a scale of 5.
11.	`Weak Foot` – (Ordinal) – rating on a scale of 5.
12.	`Skill Moves` – (Ordinal) – rating on a scale of 5.	
13.	`Work Rate` – (Ordinal) – it has two parameters, attack, and defense work rate. These parameters take the values of medium to high.
14.	`Body Type` – (Ordinal) – describes the body type of the player, has 10 unique values.
15.	`Position` – (Nominal) – describes the players position on the pitch, has 27 values.
16.	`Joined data` – (Interval) – the players joining date
17.	`Height/Weight` – (ratio) – specifies the height and weight of the player. 
18.	It also has other attributes that describe each player’s stats.

**ii.	Dataset Pre-processing**
1.	Our data has 89 columns in them, that represents we are dealing with huge amount of data. The dataset we choose should be processed before working on visualization.
2.	The columns with redundant data which are not used in the dashboard are removed.
3.	The data types of the wage and value columns are changed from string to number. The values in these columns are in the string format [ ex - €130K], tableau doesn’t recognize it as a numeric value, so these values are processed.
4.	Python – pandas is used to transform these values. The code for this is as shown in the below figure. The euro symbol is removed, the value with K is replaced with ‘000’, and the value M is replaced with ‘00000’. The result obtained is the value in integer format. [ ex: 130000].

 **The below figure shows the python pre-processing steps**
 
 <img src="https://github.com/shaalni01/FIFA-Dashboard/blob/main/Assets/Preprocessing%20the%20dataset.JPG" />




