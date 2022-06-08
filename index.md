
# Identifying Opportunities for Democrats in Georgia’s Electoral Landscape: Data Analysis of Recent Voting History in Georgia

## Introduction
The Emerge GA Team (from the January 2022 cohort of Bluebonnet Data Fellows) has been working with Maggie Chambers of Emerge Georgia (part of the Emerge America network), which recruits and trains self-identified Democratic women, primarily women of the New American Majority, to run for political office.

The team was tasked with: 
* Identifying geographic areas of opportunity where Emerge should focus their candidate recruitment; 
* Understanding voter opinions of each geographic idea to better shape each candidate's campaign priorities.

To achieve this, we began our project by collecting and computing past election data to create a measure of *Democratic Strength*, and in turn a *Flippability Score*, for each Georgia county. Ultimately, Democratic Strength was visualized on an interactive color map.

## Defining Democratic Strength and Flippability Score

We computed Democratic Strength as the average of the Democratic share of the two-party vote within each county across four elections, namely: 
* The 2016 Clinton v. Trump presidential election
* The 2018 Abrams v. Kemp gubernatorial election
* The 2020 Biden v. Trump presidential election
* The 2021 Ossoff v. Perdue US Senate election


Using Democratic Strength, we then created a Flippability Score, a metric that determines the likelihood of flipping the county from Republican to Democratic control, ranging from 1 as the least flippable to 6 as the most flippable.

To compute the Flippability Score, each county is: 
  1. Checked to meet the **population** threshold, which we’ve set the lower bound to be 5000. Any county with a population less than that is scored “N/A (Population below  threshold)”.

  2. Determined **if the county voted for Biden in 2020**. If so, this county is scored as “N/A (Already voted for Biden)”, which no longer makes it relevant to be considered for flippability. 
  
  3. If not eliminated based on step 1 or 2, the county is then categorized into a score of 1-6 depending on the Democratic Strength metric. 
        <ol type="a">
         <li>Score of 1: Democratic Strength % ranging from 0 - 34.99%</li>
         <li>Score of 2: Democratic Strength % ranging from 35 - 39.99%</li>
         <li>Score of 3: Democratic Strength % ranging from 40 - 44.99%</li>
         <li>Score of 4: Democratic Strength % ranging from 45 - 47.49%</li>
         <li>Score of 5: Democratic Strength % ranging from 47.5 - 49.99%</li>
         <li>Score of 6: Democratic Strength % ranging from 50 - 100%</li>
        </ol>
        
        
We are only interested in measuring the flippability of counties where the Republican party won the presidential vote in 2020 as Emerge’s current focus is on flipping counties from red to blue and not deepening Democratic strongholds.

For example, if county X did not vote for Biden in 2020 but did have substantial Democratic vote gains in the 2021, 2018, and 2016 elections, county X would then be assigned a high Flippability Score. On the other hand, if county Y did vote for Biden in 2020 and similarly had substantial Democratic vote gains in other years, county Y would not be assigned said score. 

We additionally computed a secondary Flippability Score with a greater focus on local elections. The election data, Democratic Strength calculations, population threshold, and score threshold stay the same, but instead of eliminating some counties based on whether the county voted for Biden in 2020, we check the local election results to determine which counties are relevant to be considered for flippability. 

We collected the two-party results for the County Clerk of Superior Court and County Tax Commissioner offices from the November 2020 election, and eliminated counties if they voted for Democrats in both of these offices.

  To calculate Democratic strength, we computed the average of the two-party vote for each county across the above elections as follows:

<center><iframe width="1000" height="126" src="demstrength_equation.png" title="Democratic Strength Equation" frameborder="0"></iframe></center>

## List of Top 20 Most Flippable Counties
Below is the list of counties ranked based on our computed Flippability Scores:

<center><iframe width="300" height="455" src="top20counties.png" title="Top 20 Flippable Counties" frameborder="0"></iframe></center>


You can find our detailed computations on the spreadsheet, and further explanation on the ReadMe and tutorial video.
* [Democratic Strength Variables Spreadsheet](https://docs.google.com/spreadsheets/d/1bVX-4I39reLE3f5CCt2wAaGsLF5hJ_UcgSB6As4XY7U/edit#gid=311527563)
* [Democratic Strength Variables ReadMe](https://docs.google.com/document/d/1e62ffYGvuV6brS6XKNG7lrS-JCA5KrDi5fhfdi45KiE/edit)
* [Democratic Strength Variables Video Walk Through](https://drive.google.com/file/d/1uneIA1Al-2iH2RhOnii25twAd9n_uNix/view?usp=sharing)

## Explanations of the Color Map 
To visualize the Democratic Strength for each county across the entire state, we created a map using Tableau in which counties are colored using different shades of blue (pale to dark) according to the magnitude of their Democratic Strength Tableau.

<script type="module" src="https://public.tableau.com/javascripts/api/tableau.embedding.3.latest.min.js"></script>

<tableau-viz id="tableauViz"       
  src='https://public.tableau.com/shared/35967HKB8?:display_count=n&:origin=viz_share_link'      
  height='600px' width='600px' toolbar='bottom' hide-tabs>
</tableau-viz>

By default, all counties are shaded. Two filters and a search bar, however, are available to users.
  1. “Biden Won County?” filter: Users can select the checkbox for “0” or “1”, where 0 means that Biden did not win the county in 2020, and 1 means         that he did.

  2. “Population as of 2020” filter: Users can move the two sliders on the scale to set a population floor and ceiling that forms the range  determining what counties are displayed on the color map. Users can also insert population floor and ceiling manually. 
  
  3. The search bar allows users to directly enter the name of a county of interest to pinpoint it on the at least 40%, regardless of county          population size.



## Candidate Priorities 
To help candidates better understand voter behavior and shape their campaign priorities, we analyzed 2018 exit polls data to create candidate profiles on voter demographic information as well as general opinion on a variety of political topics.

### Voters’ Political Preferences: Analysis
In order to determine voters’ political preferences in the most flippable counties (all counties that voted for Trump in 2020 with the scores of 3-6, or all counties that voted for Trump in 2020 with the Democratic Strength of a least 40%), we utilized a 2018 survey conducted by YouGov, results of which were subsequently published by the Cooperative Congressional Election Study. We decided to opt for the 2018 poll results since no post-2018 CCES survey would allow us to conduct a county-level analysis. The sample size of our general dataset equals 108, and we will be referring to all respondents as voters in our analysis, regardless of whether they did or did not vote in the most recent elections.

### Voting, Ideological, and Party Preference
In the most flippable 16 counties, around 75% of voters cast their ballots in the 2016 general election, and nearly half (**49%**) of voters cast their ballots **early** in-person. From those who answered the question on presidential candidate preference (81), around ***52%** of voters said they had cast their ballots for Donald Trump in 2016*, compared to ***33%** who voted for Hillary Clinton that year*. At the same time, voters in these counties overwhelmingly identify as Republicans and conservatives, as shown in the tables below:

*Party Preference of Voters in the Most Flippable Counties*
<center><iframe width="500" height="272" src="partypref.png" title="Party Preference of Voters in the Most Flippable Counties" frameborder="0"></iframe></center>


*Political Ideology of Voters in the Most Flippable Counties*
<center><iframe width="500" height="188" src="politicalidealogy.png" title="Political Ideology of Voters in the Most Flippable Counties" frameborder="0"></iframe></center>

As indicated above, 39% of voters identify as Republicans, and 47% of voters identify as conservatives. There is also a considerable bloc of voters who identify as Independents and/or moderates; 32% describe themselves as Independents or leaning Independents, and 30% describe themselves as moderates.

### Demographic Profile
Demographically, about **61%** of voters in these counties are white, **31%** are Black, and **5%** are Hispanic/Latino, and the majority of voters are either high school graduates or have completed some college, as shown in the table below.

*Education Levels of Voters in the Most Flippable Counties*
<center><iframe width="500" height="225" src="educationlevel.png" title="Education Levels of Voters in the Most Flippable Counties" frameborder="0"></iframe></center>

Moreover, in the aforementioned counties, the median income is within the $60,000-$69,999 range, and the age distribution of voters is presented in the table below.

*Age Distribution of Voters in the Most Flippable Counties*
<center><iframe width="500" height="129" src="agedist.png" title="Age Distribution of Voters in the Most Flippable Counties" frameborder="0"></iframe></center>

Finally, the median age of voters in the most flippable counties is **49**.

### Policy Positions

Generally, voters in the most flippable counties are supportive of lower corporate tax rates, Medicare for All, and increased spending on law enforcement.

In detail, about **59%** of voters, in 2018, supported cutting the corporate tax rate from 39% to 21%. As for Medicare for All, similarly, **59%** supported such health care policy; in the case of law enforcement spending, about **70%** of voters supported increased state funding for related programs.

On race-related issues, about **41%** agree with the statement that generations of slavery and discrimination have created conditions that make it difficult for Black people to work their way out of the lower class, while about **50%** disagree.

### Candidate Profile

Based on these results, Democratic candidates should try and appeal to the Republican base, given the number of Republican and conservative voters in these counties. Notably, we found that the voters in most cases support policy positions more associated with the Republican Party and conservative values, except for the issue of healthcare, where the voters expressed an overwhelming support for Medicare for All. Finally, we recommend that any GOTV efforts should focus on in-person early voting, as we found that **49%** of voters had chosen such a method.

## Data Collection Details
Our election results data (presidential, congressional, gubernatorial [Abrams v. Kemp], US Senate [Ossoff v. Perdue]) was primarily pulled from the following sites:
*  [Georgia Secretary of State Website](https://results.enr.clarityelections.com/GA/)
* [Dave Leip's Atlas of U.S. Elections](https://uselectionatlas.org/RESULTS/)
* [Washington Post's Election Reporting](https://www.washingtonpost.com/elections/election-results/georgia-senate-runoffs-2021/)
* [Daily Kos Election Data Collection](https://www.dailykos.com/stories/2020/11/19/1163009/-Daily-Kos-Elections-presidential-results-by-congressional-district-for-2020-2016-and-2012)

For local offices at the county level, data was pulled from the official [GA Secretary of State website](https://results.enr.clarityelections.com/GA/105369/web.264614/#/access-to-races), using the 2020 general election results.

For candidate priority profiles, we used the 2018 [Cooperative Election Study](https://dataverse.harvard.edu/dataset.xhtml?persistentId=doi%3A10.7910/DVN/ZSBZ7K) exit polls dataset.

The relevant data, and the computations explained, are hosted/performed on the [Google Sheets](https://docs.google.com/spreadsheets/d/1bVX-4I39reLE3f5CCt2wAaGsLF5hJ_UcgSB6As4XY7U/edit). This data is also what the R code pulls from when populating the interactive color map.

## Meet Our Team!
We are a team of 5 Bluebonnet Data Fellows working with the Emerge GA Team and Maggie Chambers of Emerge Georgia. Emerge is a non-profit organization aiming to recruit and train women and minorities to run for local offices.

*  [Marcelina](https://www.linkedin.com/in/marcelinaprzespolewska) (she/her) is an Elections Researcher at BallotReady and a recent Smith College graduate. She will soon begin a graduate program at Sciences Po, further delving into the intersection of electoral politics and technology.
*  [Rena](https://www.linkedin.com/in/renaaliu/) (she/her) is a recent graduate from Johns Hopkins University, studying computer science and social policy. She’s super passionate about tech policy, responsible AI and applying her technical skills to social impact initiatives. She’ll be joining Microsoft full-time in Seattle in September.
*  [Ambika](https://www.google.com/url?q=https://www.linkedin.com/in/ambikay/&sa=D&source=docs&ust=1654314370937015&usg=AOvVaw0tDlPqm-s7AtTus9eI3byD) (she/her) is a senior at Rutgers University graduating May 2023 and is studying computer science with minors in business administration and cognitive science. She has a passion for politics and ethical/sustainable tech and loves her BlueBonnet team! 
*  [Khushi](https://www.linkedin.com/in/khushidarji/) (she/her) is a junior at Rutgers University, majoring in computer science and minoring in cognitive science. She’s interested in the intersection of tech & politics.
* [Lois](https://www.linkedin.com/in/lois-lo/) is a Hong Kong-born community organizer. She devotes her time to a grassroots political organization that builds people power in Lake County, IL and a working-class mutual aid gardening collective that strengthens our ecology and builds food autonomy for the working class. She is currently working as a financial analyst. Gaining fluency in working with electoral data, the ability to leverage any data for a political goal and a deeper understanding of organizations supporting the Democratic party were her top goals in this fellowship.
