

# Data Analysis of Voting in Georgia 
The Emerge Georgia BlueBonnet Team:
<UL>
<LI>Rena, Marcelina, Lois, Khushi, Ambika 
</UL>


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
To calculate if a given political area subdivision currently already has a Democrat in office, we used the IF() function, = IF(J2 > K2, 1, 0)where J2 is a cell within the column listing the # of Democratic votes and K2 is a cell within the column listing the # of Republican votes. which translates to the conditional statement of: 
<!DOCTYPE html>
<html>
  <head>
  </head>
  <body>
    <h1>insert the latex equation in here</h1>
    <p>Welcome to my GitHub Pages site!</p>
  </body>
</html>


 
 

## Conclusions
Both the large-scale statewide and county case study results show that people living in rural communities are disadvantaged when it comes to internet access. In particicular, people of color are disproportionately affected. This is particularly unjust considering the reliance on internet to perform school activities in the era of COVID-19.<sup>5</sup> So while, there is an association in our graphs with lack of internet access leading to not receiving a high school diploma, we expect this discrepency will be furthered in future data. For instance, when large-scale data becomes available for 2020-2022, we expect that internet access will be even more strongly correlated with schooling outcomes. 

Based on our analysis, we recommend policies that increase internet access in rural and minority communities especially in Alabama. It seems that these ideas are already in discussion at the national level with the most recent passed infrastructure bill providing 14 billion dollars in funding to provide broadband internet connection to rural America.<sup>5</sup> While this is a great first step, in many ways, this proposal is too late to undo the harms of COVID-19 on people's education. Therefore, we also recommend policies to support high-school dropouts in the COVID-19 pandemic to correct these injusticies.

### Data Sources and Visuals
The data visualized on the Infogram interactive graph slide deck comes from census data and specifically, the American Community Survey. We pulled data for:

1. Statewide internet accessibility, educational success, and other demographics using the 2017 American Community 5-year survey
2. Alabama internet accessibility, educational success, and other demographics by county using the 2017 American Community 5-year survey

To quantify our chosen issue of internet accessibility and educational success, the relevant census data outcome labels we found were 
- a breakdown of internet access types (# households with an internet subscription, # households with internet access but no subscription, # households with no internet access)
- % population 25 or older with high school diploma
- % of population who identified as Black or African American along with other racial breakdowns.

Data was pulled in R using the censusapi package. Visuals were made using R with ggplot2, tigris, rCharts and sf packages as well as Infogram. 

### References
- [1] https://www.weforum.org/agenda/2020/04/coronavirus-education-global-covid19-online-digital-learning/  
- [2] https://hbr.org/2020/09/the-pandemic-pushed-universities-online-the-change-was-long-overdue 
- [3] https://www.brookings.edu/blog/techtank/2020/03/17/what-the-coronavirus-reveals-about-the-digital-divide-between-schools-and-communities/
- [4] https://morganya.org/research/warschauer-olpc-birmingham.pdf 
- [5] https://www.nytimes.com/2021/08/02/us/broadband-infrastructure.html
- [6] https://www.nytimes.com/2021/05/17/business/infrastructure-rural-broadband.html
