## Understanding the File Directory -- Helpful Guide
All files found in the Website can also be found in our GitHub repository hosted by BlueBonnet on [this GitHub](https://github.com/bluebonnet-teams-2022/emergega.github.io) (you are on the github repository right now).

### Overall Website Content 
All content seen on the website can also be found in the index.md file in the GitHub directory. The content was edited and compiled into the index.md file through the GitHub repository. 

### Interactive Map 
The interactive map code was converted from R to HTML code and then saved in the GitHub repository which can be found under the filename: interactive_georgia.html. 
Next, using HTML code the interactive map was incorporated into the index.md file. 

### Lists and Equation
All lists and the equation can be found saved in the Github repository under the following filenames, respectively: flipchart.png, top20flip.png, and demstrength_equation.png.

## Interactive Electoral Map of Georgia Counties: Visualizing Democratic “Flippability"
This projects visualizes the Democratic strength of Georgia counties on an interactive map that displays county information in a hover box. 

### Tech Used
R is the only programming language used in creating the color map. The end result is saved to a .html format. 

### Structure of the Code
Our team collected an extensive amount of Georgia vote count data at various levels. The result served as the base data set to which new data was joined and off of which visualization was created.

The geometrical data was obtained through accessing Georgia’s Federal Information Processing Standards (FIPS) code through the tigris package within R.

The interactive map was created using the plotly R package.

### Installation
Be sure to install any packages you don’t already have in your R environment. All necessary packages have been included in the body of the code.

### Running the Application
After installing your packages, simply run the entirety of the code starting from loading the various packages, to the last line which saves the interactive map to .html.

### Credits
[Technology Accessibility and Educational Attainment: Case Study in Alabama
](https://clparent121.github.io/hci-project-2-team-15/)
