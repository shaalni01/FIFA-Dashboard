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

**Below is the picture of the Implemented FIFA Dashboard**

<img src="https://github.com/shaalni01/FIFA-Dashboard/blob/main/Assets/CreatinG%20FIFA%20dashboard.JPG" />

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

 **The figure 2.1 shows the pre-processing steps of dataset in jupyter notebooks**
 
 <img src="https://github.com/shaalni01/FIFA-Dashboard/blob/main/Assets/Preprocessing%20the%20dataset.JPG" />
 
 5.	The values in the ‘Jersey Number’ and ‘Contract validity’ are of the data type float. These values if displayed in the table just as it is, will be displayed  as bars. To display the value itself, it is converted to string using calculated field. 

**The figure 2.2 shows the pre-processing steps in Tableau**

<img src="https://github.com/shaalni01/FIFA-Dashboard/blob/main/Assets/Preprocessing%20the%20dataset%20fig%202.2.JPG" />

# Section 3: Dashboard Users
The users of the FIFA 19 dashboard are–
`Sports analysts`- This dashboard helps them in getting insights about players data. They can predict if the player is fit for the coming matches by evaluating their performances.

`Football fans`- Football is the most popular sport ever and it has billions of fans. These fans can get the detailed information about their favorite players.

`Sports Channels`- The reporters can retrieve information about each player and help in analyzing their gameplay.

`Football Coaches`- Football coaches can analyze the players performance in the previous games and can help in improving the player’s skills.

`Football club management`- They can analyze the players profile that will help them to decide whether to buy the player or not in an auction.

`Football Players` – The Players themselves can use the dashboard to analyze their own stats and also the opponents’ stats.

# Section 4: Questions
1.	How many players, clubs and nations are participating in FIFA 19?
2.	Identifying the Nationalities of all players of a particular club.
3.	How many players prefer left foot? Likewise, how many players prefer right foot?
4.	Identifying the top players in each club based on overall potential.
5.	What are the age groups and counts of players in each club?
6.	What strategy does the club implement?
7.	Who are the players with highest penalties?
8.	Display the brief view of player’s stats.
9.	Show the wage distribution among the players in FIFA 19
10.	Determine the topmost expensive players of this season.
11.	How many players are right forward, left forward, strikers, LDM in each club?
12.	How does the number of players vary with respect to the work rate?

# Section 5: Plots
1.	The dashboard will have a header which displays the dashboard title, the players count, number of countries and number clubs participating in FIFA 19.
 
      •	**Question** – How many players, clubs and nations are participating in FIFA 19?
   
      •	The total count of the players, clubs and countries in the FIFA 19 is directly displayed on top of the dashboard.

2.	A choropleth map displaying the countries and the number of players in each country for a particular club. A filter on the club column is applied such that when a specific country is selected, the map and values change accordingly on the sheet.

     •	**Question** - Identifying the Nationalities of all players of a particular club.
   
     •	The map highlights the countries of all the players in a club. A club filter is applied on the map, such that when a particular club is selected, the countries of the club’s players is highlighted with displaying the number of players from each country.
     
     <img src="https://github.com/shaalni01/FIFA-Dashboard/blob/main/Assets/Creating%20cloropleth%20map.JPG"/>
     
3.	A pie chart depicting the count of players which is organized based on the player’s preferred foot. 

    •	**Question** – How many players prefer left foot? Likewise, how many players prefer right foot?
    
    •	The preferred foot parameter takes 2 values either left or right. The pie chart gives the count of the number of players preferring right foot and number of players who prefer left foot.
    
    <img src="https://github.com/shaalni01/FIFA-Dashboard/blob/main/Assets/Creating%20the%20pie%20chart.JPG"/>
    
4.	A bar chart displaying the potential of the players in a particular club.

    •	**Question** - Identifying the top players in each club based on overall potential.
    
    •	The Plot shows the potential of all the players in a club. A club filter is applied on the plot such that when a club name is selected the potentials of all the players in the club is displayed.
    
    <img src="https://github.com/shaalni01/FIFA-Dashboard/blob/main/Assets/creating%20the%20bar%20graph.JPG"/>

5.	A bar chart depicting the age distribution of all the players in each club. The ages are grouped into categories of <20, 20s, 30s and 40s. The club filter is also applied to this chart. Answers the question 5.

    •	**Question** - What are the age groups and counts of players in each club?
    
    •	 Calculated field is created to group the ages and a club filter is applied. The club filter lets you choose the club value, and the graph shows the players age distribution.
    
    <img src="https://github.com/shaalni01/FIFA-Dashboard/blob/main/Assets/creating%20bar%20chart-age%20distribution.JPG"/>

6.	A pie chart of team strategy showing the count of attack, defense, and midfielder. A calculated field is created based on position parameters to get the afore mentioned fields.

    •	**Question** – What strategy does the club implement?

    •	The team strategy is defined by three parameters, attack, defense, and midfielder. These parameters are determined by the players positions. A calculated field is created based on the positions.
    
    <img src="https://github.com/shaalni01/FIFA-Dashboard/blob/main/Assets/creating%20pie%20chart%20for%20team%20strategy.JPG"/>

7.	A bar chart showing the top N players with highest penalties

    •	**Question** – Who are the players with highest penalties?
    
    •	The plot shows the top N players with the highest number of penalties in the season. The number of players to be displayed can be inputted by the user through top N filter.
    
    <img src="https://github.com/shaalni01/FIFA-Dashboard/blob/main/Assets/creating%20bar%20chart%20with%20players%20highest%20penalties.JPG"/>

8.	A table describing the stats of each player, this table includes the parameters of club, nationality, position, work rate, body type, jersey number and date joined.

    •	**Question** - Display the brief view of player’s stats.
    
    •	A user interactive filter is applied for the names of the players, such that when a player name is selected, the entire stat of the player is displayed.
    
    <img src="https://github.com/shaalni01/FIFA-Dashboard/blob/main/Assets/Creating%20a%20table%20for%20stats%20of%20each%20player.JPG"/>

9.	A bar chart showing the players distribution based on the wages in the season.

    •	**Question** - Show the wage distribution among the players in FIFA 19
    
    •	A calculated field is created on wages which is grouped into 10k – 20k, 30k – 40k, 50k – 100k, 100k-150k and >150k. The number of players in each wage group is then displayed.
    
    <img src=""/>

10.	A bar chart showing the top expensive players based on values in the season.

    •	**Question** - Determine the topmost expensive players of this season.
    
    •	A top N filter is applied to show the top N valuable players. The player value feature is used for this plot.

11.	A plot showing the number of players with respect to their position for each club.

    •	**Question** – How many players are right forward, left forward, strikers, LDM in each club?
    
    •	The sheet shows the number of players who have different positions i.e., LDM, left forward, right forward etc. The club filter is applied to select each club.

12.	A bar chart showing the number of players in each value of the work rate.

    •	**Question** - How does the number of players vary with respect to the work-rate?
    
    •	The number of players who has different attack/defense work rate is shown in the graph.








