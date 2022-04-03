
# Data Analysis of Voting in Georgia 



## Flippability Score and Democratic Strength Computation Explanations

For the purpose of our analysis, we computed Democratic strength, a metric expressed as a percentage that measures the level of partisan strength of the Democratic Party given the election results within a given political subdivision (i.e. county, state senate district, state house district, etc.).

In order to determine Democratic strength, we first collected election results for the last three election cycles for each political subdivision; we gathered the following data: 
<OL START=”1″>
<LI>County-level presidential election results to compute Democratic strength of each county
<LI>Congressional district-level presidential election results to compute Democratic strength of each congressional district
<LI>State Senate election results to compute Democratic strength of each State Senate district
 <LI>State House election results to compute Democratic strength of each State House district
 <LI>District Attorney election results to compute Democratic strength of each judicial circuit
  
</OL>


To calculate Democratic strength, we computed the average of the two-party vote for each political subdivision as follows:

INSERT LATEX EQUATION HERE. 
  <script type="text/javascript" async="" src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.4/MathJax.js?config=TeX-MML-AM_CHTML">
</script>
<p><span class="math display">\[y = \frac{a}{b} + c^2 + d\]</span></p>

Using Democratic strength, we then created a flippability score, which is a measure that determines the likelihood of flipping a political subdivision from Republican to Democratic control, ranging from 1 as the least flippable to 6 and the most flippable. Political subdivisions already currently under Democratic control are denoted as 0 on the flippability scale.

****INSERT CHART HERE WILL BE CALLED THE CHART FOR DEMOCRATIC STRENGTH AND FLIPPABILITY SCORE <FIRST CHART> 
 

 

### Color Map Display Explanation
On our color map, the flippability score is translated with the intensity (pale to dark) of the purple color of each political area subdivision.

**NEED TO ADD THIS HERE** written in red in actual doc:
"On the map below
Link to spreadsheet, how to edit and rerun map code
Most flippable counties" **NEED TO ADD THIS HERE** written in red in actual doc 
 

## Data Collection and Link to Spreadsheet
Our election result data collection was primarily pulled from the follwing sites: 
 <OL>
<LI>Georgia Secretary of State Website 
<UL>
<LI>https://results.enr.clarityelections.com/GA/
</UL>
<LI>Dave Leip's Atlas of U.S. Elections 
<UL>
<LI>https://uselectionatlas.org/RESULTS/
</UL>
 <LI>Washington Post's Election Reporting  
<UL>
<LI>https://www.washingtonpost.com/elections/election-results/georgia-senate-runoffs-2021/
</UL>
</OL>

<UL>
<LI>have we gotten confirmation for sharing the data site? Check Slack! 
</UL>

 
## Spreadsheet Calculations Explained
 <OL>
<LI>To calculate if a given political area subdivision currently already has a Democarat in office, we used the following: 
<UL>
<LI>IF() function, = IF(J2 > K2, 1, 0)
<LI>where, J2 is a cell within the column listing the # of Democratic votes 
<LI>where, K2 is a cell within the column listing the # of Republican votes 
<LI>Conditional Statement used: insert latex statement 
</UL>
<LI>To calculate the democratic strength of a given political area subdivision, we used the following: 
<UL>
<LI>SUM()function to compute the arithmetic mean, =sum(M2, U2, Q2, I2)/4
<LI>M2, U2, Q2, I2 are all cells within the columns listing the expression below for each respective election cycle
<LI>Expression: 
</UL>
 <LI>Next, we computed the flippability score. To do this, a more complex conditional using the IF() function is needed, which corresponds to the table listed above **say which section it is listed in!**
<UL>
<LI>=IF(C2 = 1, 0, IF(D2 < 34.99, 1, IF(D2 < 39.99, 2 ,IF(D2 < 44.99, 3, IF(D2 < 47.49, 4, IF(D2 < 49.99, 5, 6))))))
<LI>"C2" is a cell within the column which lists a 0 if the current political office is held by a Republican and a 1 if it is otherwise held by a Democrat  
<LI>D2 is a cell in the column listing the Democratic Strength 
</UL>
</OL>

<!DOCTYPE html>
<html>
  <head>
  </head>
  <body>
    <p>insert latex equation or image here! use this code for number 1 and 2 in this section (note for ambika)</p>
  </body>
</html>
 
 

 
 

## Top 20 Most Flippable Counties List 
Given the above calculations performed on Georgia counties for the 2016 (Clinton and Trump ) and 2020 (Biden and Trump) presidential elections, the 2018 midterm gubernatorial elections (Abrams and Kemp), and the 2021 U.S. Senate Runoff election (Ossoff and Perdue), a list of the top 20 counties with the highest flippability scores are listed below:
 
 INSERT TABLE HERE 


## Meet Our Team! 
 We are a team of 5 Blue Bonnet Fellows working with the Emerge GA 527 Team and Maggie Chambers of Georgia branch of the Emerge organization! The Emerge Organization is a nonprofit aiming to recruit and train women and minorities to run for local offices. 
<UL>
<LI>Marcelina is an Elections Researcher at BallotReady and a recent Smith College graduate. 
<LI>Rena is a recent graduate from Johns Hopkins University, studying computer science and social policy. She’s super passionate about applying her technical skills to social impact initiatives, and excited to work with you all before joining Microsoft full-time in August. 
<LI>Ambika is a current junior at Rutgers University, studying computer science and minoring in business and cognitive science. She is excited to apply her technical skills using political data and being a part of this team! 
<LI>Khushi is a sophomore at Rutgers University, majoring in computer science and minoring in cognitive science. She’s interested in the intersection of tech & politics and very excited to get started on this data team!
<LI>Lois is working as a financial analyst in Corporate America by day and a political organizer by nights/weekends. She is a graduate of the University of Virginia (Go Hoos!), where she studied Public Policy and Business. She is excited to be making her foray in working with political data with Emerge Georgia, with hopes to one day make it her full-time job. )
</UL>


