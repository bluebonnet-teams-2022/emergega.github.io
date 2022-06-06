
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
        <ol type="a">
         <li>Score of 1: Democratic Strength % ranging from 0 - 34.99%</li>
         <li>Score of 2: Democratic Strength % ranging from 35 - 39.99%</li>
         <li>Score of 3: Democratic Strength % ranging from 40 - 44.99%</li>
         <li>Score of 4: Democratic Strength % ranging from 45 - 47.49%</li>
         <li>Score of 5: Democratic Strength % ranging from 47.5 - 49.99%</li>
         <li>Score of 6: Democratic Strength % ranging from 50 - 100%</li>
        </ol>
        
        
We are only interested in measuring the flippability of counties where the Republican party won the presidential vote in 2020 as Emerge’s current focus is on flipping counties from red to blue and not deepening Democratic strongholds.

For example, if county X did not vote for Biden in 2020 but did have a strong turnout for Democratic candidates in the 2021, 2018, and 2016 elections, county X would then be assigned a high Flippability Score.

We additionally computed a secondary Flippability Score with a greater focus on local elections. The election data, Democratic Strength calculations, population thresholding, and score thresholding stay the same, but Instead of eliminating some counties based on if the county voted for Biden in 2020, we check the local election results from 2020 to determine which counties are relevant to be considered for flippability. 

We collected the two-party results of the County Clerk of Superior Court and County Tax Commissioner offices from the November 2020 election, and eliminated counties if they voted for Democrats in both of these offices.

  To calculate Democratic strength, we computed the average of the two-party vote for each county across the above elections as follows:

<center><iframe width="1000" height="126" src="demstrength_equation.png" title="Democratic Strength Equation" frameborder="0"></iframe></center>

## List of Top 20 Most Flippable Counties
Below is the list where we have ranked the counties based on our computed Flippability Scores:

<center><iframe width="300" height="451" src="top20list.png" title="Top 20 Flippable Counties" frameborder="0"></iframe></center>


You can find our detailed computations on the spreadsheet, and further explanation on the ReadMe and tutorial video.
* [Democratic Strength Variables Spreadsheet](https://docs.google.com/spreadsheets/d/1bVX-4I39reLE3f5CCt2wAaGsLF5hJ_UcgSB6As4XY7U/edit#gid=311527563)
* [Democratic Strength Variables ReadMe](https://docs.google.com/document/d/1e62ffYGvuV6brS6XKNG7lrS-JCA5KrDi5fhfdi45KiE/edit)
* [Democratic Strength Variables Video Walk Through](https://drive.google.com/file/d/1uneIA1Al-2iH2RhOnii25twAd9n_uNix/view?usp=sharing)

## Explanations of the Color Map Display
To visualize the Flippability Score for each county across the entire state, we created a color map where different shades of purple (pale to dark) correspond to the spectrum of scores (low to high). The interactive map was created using Plotly in R.

<script type="module" src="https://public.tableau.com/javascripts/api/tableau.embedding.3.latest.min.js"></script>

<tableau-viz id="tableauViz"       
  src='https://public.tableau.com/shared/35967HKB8?:display_count=n&:origin=viz_share_link'      
  height='600px' width='600px' toolbar='bottom' hide-tabs>
</tableau-viz>

Given that the project sets out to show the scores of counties to supplement Emerge’s existing strategy on candidate recruitment, and due to how we computed the score itself, the color map will only shade counties:
  1. That exceed 5,000 (we could only accommodate one set population threshold at this time) in population;

  2. Where Republicans won in the 2020 presidential election. 

Eliminating counties that meet one or both of these conditions helps focus Emerge’s resources in counties where there are more opportunities for recruitment.

Nonetheless, we have added map visualizations of the excluded counties to add context and understanding of their geographic distribution and/or pattern for Emerge’s current and future endeavors.

<center><iframe width="800" height="545" src="8counties.png" title="Counties with Population Below 5,000" frameborder="0"></iframe></center>
The above map shades counties where the population is below 5,000. They include:
<center><iframe width="400" height="267" src="8countieslist.png" title="List of 8 Counties" frameborder="0"></iframe></center>

<center><iframe width="800" height="445" src="22counties.png" title="Counties That Voted Democratic" frameborder="0"></iframe></center>
The above map shows 22 counties that voted Democratic in the 2020 presidential election. They include:
<center><iframe width="300" height="552" src="22countieslist.png" title="List of 22 Counties" frameborder="0"></iframe></center>


## Candidate Priorities 
To help candidates better understand voter behavior and shape their campaign priorities, we analyzed 2018 exit polls data to create candidate profiles on voter demographic information as well as general opinion on a variety of political topics.

### Voters’ Political Preferences: Analysis
In order to determine voters’ political preferences in the most flippable counties (all counties that voted for Trump in 2020 with the scores of 3-6, or all counties that voted for Trump in 2020 with the Democratic strength of a least 40%), we utilized a 2018 survey conducted by YouGov, results of which were subsequently published by the Cooperative Congressional Election Study. We decided to opt for the 2018 poll results since no post-2018 CCES survey would allow us to conduct a county-level analysis. The sample size of our general dataset equals 108, and we will be referring to all respondents as voters in our analysis, regardless of whether they did or did not vote in the most recent elections.

### Voting, Ideological, and Party Preference
In the most flippable 16 counties, around 75% of voters cast their ballots in the 2016 general election, and nearly half (**49%**) of voters cast their ballots **early** in-person. From those who answered the question on presidential candidate preference (81), around ***52%** of voters said they had cast their ballots for Donald Trump in 2016*, compared to ***33%** who voted for Hillary Clinton that year*. At the same time, voters in these counties overwhelmingly identify as Republicans and conservatives, as shown in the tables below:

*Party Preference of Voters in the Most Flippable Counties*
<center><iframe width="500" height="272" src="partypref.png" title="Party Preference of Voters in the Most Flippable Counties" frameborder="0"></iframe></center>


*Political Ideology of Voters in the Most Flippable Counties*
{insert table here}

As indicated above, 39% of voters identify as Republicans, and 47% of voters identify as conservatives. There is also a considerable bloc of voters who identify as Independents and/or moderates; 32% describe themselves as Independents or leaning Independents, and 30% describe themselves as moderates.

### Demographic Profile
Demographically, about **61%** of voters in these counties are white, **31%** are Black, and **5%** are Hispanic/Latino, and the majority of voters are either high school graduates or have completed some college, as shown in the table below.

*Education Levels of Voters in the Most Flippable Counties*
[insert table here]

Moreover, in the aforementioned counties, the median income is within the $60,000-$69,999 range, and the age distribution of voters is presented in the table below.

*Age Distribution of Voters in the Most Flippable Counties*
[insert table here]

Finally, the median age of voters in the most flippable counties is **49**.

### Policy Positions

Generally, voters in the most flippable counties are supportive of lower corporate tax rates, Medicare for All, and increased spending on law enforcement, as shown in the tables below.

In detail, about **59%** of voters, in 2018, supported cutting the corporate tax rate from 39% to 21%. As for Medicare for All, similarly, **59%** supported such health care policy; in the case of law enforcement spending, about **70%** of voters supported increased state funding for related programs.

On race-related issues, about **41%** agree with the statement that generations of slavery and discrimination have created conditions that make it difficult for Black people to work their way out of the lower class, while about **50%** disagree.

### Candidate Profile

Based on these results, Democratic candidates should try and appeal to the Republican base, given the number of Republican and conservative voters in these counties. Notably, we found that the voters in most cases support policy positions more associated with the Republican Party and conservative values, except for the issue of healthcare, where the voters expressed an overwhelming support for Medicare for All. Finally, we recommend that any GOTV efforts should focus on in-person early voting, as we found that **49%** of voters had chosen such a method in 2018.

## Data Collection Details
Our election results data (presidential, congressional, gubernatorial [Abrams v. Kemp], US Senate [Ossoff v. Perdue]) was primarily pulled from the following sites:
*  [Georgia Secretary of State Website](https://results.enr.clarityelections.com/GA/)
* [Dave Leip's Atlas of U.S. Elections](https://uselectionatlas.org/RESULTS/)
* [Washington Post's Election Reporting](https://www.washingtonpost.com/elections/election-results/georgia-senate-runoffs-2021/)
* [Daily Kos Election Data Collection](https://www.dailykos.com/stories/2020/11/19/1163009/-Daily-Kos-Elections-presidential-results-by-congressional-district-for-2020-2016-and-2012)

For local offices at the county level, data was pulled from the official [GA Secretary of State website](https://results.enr.clarityelections.com/GA/105369/web.264614/#/access-to-races), using the 2020 general election results.

For candidate priority profiles, we used the 2018 [Cooperative Election Study](https://dataverse.harvard.edu/dataset.xhtml?persistentId=doi%3A10.7910/DVN/ZSBZ7K) exit polls dataset.

The relevant data, and the computations explained are hosted/performed on the [Google Sheets](https://docs.google.com/spreadsheets/d/1bVX-4I39reLE3f5CCt2wAaGsLF5hJ_UcgSB6As4XY7U/edit). This data is also what the R code pulls from when populating the interactive color map.

## Meet Our Team!
We are a team of 5 Bluebonnet Data Fellows working with the Emerge GA Team and Maggie Chambers of Emerge Georgia. Emerge is a non-profit organization aiming to recruit and train women and minorities to run for local offices.

*  [Marcelina](https://www.linkedin.com/in/marcelinaprzespolewska) (she/her) is an Elections Researcher at BallotReady and a recent Smith College graduate. She will soon begin a graduate program at Sciences Po, further delving into the intersection of electoral politics and technology.
*  [Rena](https://www.linkedin.com/in/renaaliu/) (she/her) is a recent graduate from Johns Hopkins University, studying computer science and social policy. She’s super passionate about tech policy, responsible AI and applying her technical skills to social impact initiatives. She’ll be joining Microsoft full-time in Seattle in September.
*  [Ambika](https://www.google.com/url?q=https://www.linkedin.com/in/ambikay/&sa=D&source=docs&ust=1654314370937015&usg=AOvVaw0tDlPqm-s7AtTus9eI3byD) (she/her) is a senior at Rutgers University graduating May 2023 and is studying computer science with minors in business administration and cognitive science. She has a passion for politics and ethical/sustainable tech and loves her BlueBonnet team! 
*  [Khushi](https://www.linkedin.com/in/khushidarji/) (she/her) is a junior at Rutgers University, majoring in computer science and minoring in cognitive science. She’s interested in the intersection of tech & politics.
* [Lois](https://www.linkedin.com/in/lois-lo/) (she/her) is a Hong Kong-born community organizer currently residing in Lake County, IL. She devotes her time to a working-class mutual aid gardening collective that builds food autonomy for the working class, helps heal and strengthen our ecology, and builds people power. She is currently working a waged job as a financial analyst. Through working with Emerge Georgia through this fellowship, she looks forward to gaining fluency in working with electoral data and leveraging any data for a political goal and deepen her understanding of organizations supporting the Democratic party.
