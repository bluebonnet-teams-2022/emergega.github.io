
# Top 20 Most "Flippable" Georgia Counties: Data Analysis of Voting in Georgia 
A Bluebonnet Data Fellowship Project by the Emerge GA Team. Team members include Marcelina Przespolewska, Rena Liu, Ambika Yavatkar, Khushi Darji, and Lois Lo.

## Introduction
The Emerge GA Team (from the January 2022 cohort of Bluebonnet Data Fellows) has been working with Maggie Chambers of Emerge Georgia (part of the Emerge America network), which recruits and trains self-identified Democratic women, primarily women of the New American Majority, to run for political office.

The team was tasked with: 
* Identifying geographic areas of opportunity where Emerge should focus their candidate recruitment; 
* Understanding voter opinions of each geographic idea to better shape each candidate's campaign priorities.

To achieve this, we began our project by collecting, computing, and visualizing past election data to create a measure of Democratic Strength, and in turn a Flippability Score, for each Georgia county. We displayed these scores on an interactive color map. 


## Defining Democratic Strength and Flippability Score

1) We computed **Democratic strength** as **a metric** expressed as a percentage **that measures the level of partisan strength of the Democratic Party given the election results** within the county.

We collected election results for each county from:
* The 2020 and 2016 presidential elections, 

* The 2021 Ossoff v. Perdue US Senate election,v

* The 2018 Abrams v. Kemp Georgia State Governor election

Using Democratic Strength, we then created a Flippability Score, a metric that determines the likelihood of flipping the county from Republican to Democratic control, ranging from 1 as the least flippable to 6 as the most flippable.

To compute the Flippability Score, each county is: 
  1. Checked to meet the **population** threshold, which we’ve set the lower bound to be 5000. Any county with a population less than that is scored “N/A (Population below  threshold)”.

  2. Determined **if the county voted for Biden in 2020**. If so, this county is scored as “N/A (Already voted for Biden)”, which no longer makes it relevant to be considered for flippability. 
  3. If not eliminated based on step 1 or 2, the county is then categorized into a score of 1-6 depending on the *Democratic Strength* metric. 
        a. Score of 1: Democratic Strength % ranging from 0 - 34.99%
        b. Score of 2: Democratic Strength % ranging from 35 - 39.99%  
        c. Score of 3: Democratic Strength % ranging from 40 - 44.99%  
        d. Score of 4: Democratic Strength % ranging from 45 - 47.49%
        e. Score of 5: Democratic Strength % ranging from 47.5 - 49.99% 
        f. Score of 6: Democratic Strength % ranging from 50 - 100% 
        
We are only interested in measuring the flippability of counties where the Republican party won the presidential vote in 2020 as Emerge’s current focus is on flipping counties from red to blue and not deepening Democratic strongholds.

For example, if county X did not vote for Biden in 2020 but did have a strong turnout for Democratic candidates in the 2021, 2018, and 2016 elections, county X would then be assigned a high Flippability Score.

We additionally computed a secondary Flippability Score with a greater focus on local elections. The election data, Democratic Strength calculations, population thresholding, and score thresholding stay the same, but Instead of eliminating some counties based on if the county voted for Biden in 2020, we check the local election results from 2020 to determine which counties are relevant to be considered for flippability. 
//////

  


2) To calculate Democratic strength, we computed the average of the two-party vote for each county across the above elections as follows:

<center><iframe width="1000" height="126" src="demstrength_equation.png" title="Democratic Strength Equation" frameborder="0"></iframe></center>


3) Using Democratic strength, we then created a **flippability score**, a metric that determines the likelihood of flipping the county from Republican to Democratic control, ranging from 1 as the least flippable to 6 and the most flippable. 
 
<center><iframe width="500" height="400" src="flipchart.png" title="Flippability Chart" frameborder="0"></iframe></center>

Counties that voted for Biden in 2020  are denoted as “0 (NA)” on the flippability scale.

## Explanation of the Color Map Display
 
On our color map, the flippability score is translated with the intensity (pale to dark) of the purple color of each county. This interactive map was created using Plotly in R.
 
<center><iframe width="660" height="615" src="interactive_georgia" title="Interactive Georgia Map" frameborder="0"></iframe></center>


## Data Collection and Link to Spreadsheet
Our election result data collection was primarily pulled from the following sites: 
* [Georgia Secretary of State Website](https://results.enr.clarityelections.com/GA/)
* [Dave Leip's Atlas of U.S. Elections](https://uselectionatlas.org/RESULTS/)
* [Washington Post's Election Reporting](https://www.washingtonpost.com/elections/election-results/georgia-senate-runoffs-2021/)

More specifically, the election data we collected and the source of each are listed below:
* **Local Offices at the County Level** data (County Clerk of Superior Court and Tax Commissioner) used [GA Secretary of State Data](https://results.enr.clarityelections.com/GA/105369/web.264614/#/access-to-races) from the Nov 2020 election broken down by county   
* **2020 Presidential Election** data used [Dave Leip’s Atlas of U.S. Elections](https://uselectionatlas.org/RESULTS/) for Georgia, broken down by county  
* **2021 U.S. Senate Election** (Ossoff v. Perdue) data used [Washington Post’s Election Reporting](https://www.washingtonpost.com/elections/election-results/georgia-senate-runoffs-2021/), broken down by county  

The relevant data and computations explained are hosted/performed on a [Google Sheets](https://docs.google.com/spreadsheets/d/1bVX-4I39reLE3f5CCt2wAaGsLF5hJ_UcgSB6As4XY7U/edit?usp=sharing) (sheet named "County"). This data is also what the R code pulls from when populating the interactive color map. 


## Top 20 Most Flippable Counties List 
Given the above calculations performed on Georgia counties for the 2016 (Clinton and Trump) and 2020 (Biden and Trump) presidential elections, the 2018 midterm gubernatorial elections (Abrams and Kemp), and the 2021 U.S. Senate Runoff election (Ossoff and Perdue), a list of the top 20 counties with the highest flippability scores are listed below:
 
<center><iframe width="206" height="640" src="top20flip.png" title="Top 20 Flippable Counties" frameborder="0"></iframe></center>

Counties with a population under 5000 have been excluded.

## Meet Our Team! 
We are a team of 5 Bluebonnet Data Fellows working with the Emerge GA 527 Team and Maggie Chambers of the Georgia branch of the Emerge organization! The Emerge Organization is a nonprofit aiming to recruit and train women and minorities to run for local offices. 
- Marcelina is an Elections Researcher at BallotReady and a recent Smith College graduate. 
- [Rena](https://www.linkedin.com/in/renaaliu/) is a recent graduate from Johns Hopkins University, studying computer science and social policy. She’s super passionate about applying her technical skills to social impact initiatives, and is excited to work with you all before joining Microsoft full-time in August. 
- Ambika is a current junior at Rutgers University, studying computer science and minoring in business and cognitive science. She is excited to apply her technical skills using political data and be a part of this team! 
- Khushi is a sophomore at Rutgers University, majoring in computer science and minoring in cognitive science. She’s interested in the intersection of tech & politics and is very excited to get started on this data team!
- Lois is working as a financial analyst in Corporate America by day and a political organizer by nights/weekends. She is a graduate of the University of Virginia (Go Hoos!), where she studied Public Policy and Business. She is excited to be making her foray in working with political data with Emerge Georgia, with hopes to one day make it her full-time job.

## Appendix
### Top 20 Most Flippable Counties List - Taking into Account County Population
We are also in the process of creating a color map that can filter out some counties based on (a user inputted) population size. As a proof of concept, below is the top 20 list of most flippable counties where counties with a population size under 5000 are greyed out. 

INSERT LIST HERE
<!-- <center><iframe width="300" height="429" src="" title="5k Filter Top 20 Flippable Counties" frameborder="0"></iframe></center> -->

### Top 20 Most Flippable Counties List - Taking into Account Local Political Offices
To best determine which counties to prioritize future recruitment in, we also collected data regarding the party of the county's Clerk of Superior Court and Tax Commissioner  offices, which are much more local roles, since they are at the county level (as opposed to Governor, US Senator, or President). Below is a list of the top 20 most flippable counties where there is a Republican in at least one of these offices **and** the county did not vote for Biden in 2020 and does not have a population size smaller than 5000.

INSERT LIST HERE

### Spreadsheet Calculations Explained
To calculate if a given county currently already has a Democrat in office, we used the following: 

IF() function, = IF(J2 > K2, 1, 0)
- where, J2 is a cell within the column listing the # of Democratic votes 
- where, K2 is a cell within the column listing the # of Republican votes 

**Conditional Statement used:** insert latex statement 

To calculate the democratic strength of a given political area subdivision, we used the following: 
SUM()function to compute the arithmetic mean, =sum(M2, U2, Q2, I2)/4
- M2, U2, Q2, and I2 are all cells within the columns listing the expression below for each respective election cycle

**Expression:**

Next, we computed the flippability score. To do this, a more complex conditional using the IF() function is needed, which corresponds to the table listed above.

- =IF(C2 = 1, 0, IF(D2 < 34.99, 1, IF(D2 < 39.99, 2 ,IF(D2 < 44.99, 3, IF(D2 < 47.49, 4, IF(D2 < 49.99, 5, 6))))))
- "C2" is a cell within the column that lists a 0 if the current political office is held by a Republican and a 1 if it is otherwise held by a Democrat  
- D2 is a cell in the column listing the Democratic Strength 
