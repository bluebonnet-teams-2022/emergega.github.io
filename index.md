
# Data Analysis of Voting in Georgia 



## Flippability Score and Democratic Strength Computation Explanations

For the purpose of our analysis, we computed Democratic strength, a metric expressed as a percentage that measures the level of partisan strength of the Democratic Party given the election results within a given political subdivision (i.e. county, state senate district, state house district, etc.).

In order to determine Democratic strength, we first collected election results for the last three election cycles for each political subdivision; we gathered the following data: 
<LI>County-level presidential election results to compute Democratic strength of each county
<LI>Congressional district-level presidential election results to compute Democratic strength of each congressional district
<LI>State Senate election results to compute Democratic strength of each State Senate district
 <LI>State House election results to compute Democratic strength of each State House district
 <LI>District Attorney election results to compute Democratic strength of each judicial circuit
  
To calculate Democratic strength, we computed the average of the two-party vote for each political subdivision as follows:

INSERT LATEX EQUATION HERE.

<script type="text/javascript" async="" src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.4/MathJax.js?config=TeX-MML-AM_CHTML"> </script>
\[y = \frac{a}{b} + c^2 + d\]
  
Using Democratic strength, we then created a flippability score, which is a measure that determines the likelihood of flipping a political subdivision from Republican to Democratic control, ranging from 1 as the least flippable to 6 and the most flippable. Political subdivisions already currently under Democratic control are denoted as 0 on the flippability scale.

****INSERT CHART HERE WILL BE CALLED THE CHART FOR DEMOCRATIC STRENGTH AND FLIPPABILITY SCORE


