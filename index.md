

# Technology Accessibility and Educational Attainment: Case Study in Alabama
Pamela, Cassandra, and Rena

## Background
The Covid-19 pandemic has strengthened our reliance on technology in education, replacing traditional classroom functions such as lecture, exams, assignments, office hours, and others with alternatives online using video conferencing tools or online learning software, like Blackboard.<sup>1</sup>

Since March 2019, when campuses closed due to rising Covid-19 cases, colleges nationwide have scrambled to transition to online learning<sup>2</sup>. Class lectures have become synchronous and asynchronous, live on Zoom or recorded. Assignments and exams are also completed and submitted on third-party websites like BlackBoard or Gradescope. Even as the classroom adapts to hybrid modes as Covid-19 regulations ease, all these technologies still remain vital to classroom functions regardless. In K-12 schools,  many children all experience similar impacts of technology in their classrooms. Children as young as 5-year old take their seats in front of their computer to participate in classes online via Zoom. Middle and high school students have moved most of their classroom functions online as well.

However, ever before this pandemic, technology has already spread its roots into our education system. In all subjects taught in school, technology has been used to supplement in-class lectures. In a language class, one might find themselves consulting Google Translate or another online translator. In a math class, one might find themselves searching in Stack Overflow for the answers to their Linear Algebra questions. In a Science class, one might have dumped their Organic Chemistry compounds into a Quizlet to make flashcards to study with. On team assignments, students may have corresponded through Messenger, email, or GroupMe and collaborated on Google Drive. Grades were also updated online. It’s difficult, but not impossible, to imagine the alternatives for all these technologies in an in-person classroom setting.

While this shift has provided more flexibility to people from different backgrounds and time zones, this has changed technology from being a supplement to education in the classroom to a necessity as some classroom operations have been strictly online. It is increasingly harder to accommodate those who do not have access to Zoom meetings or paid training modules. According to the Federal Communications Commission, “broadband availability has been at the heart of the digital divide with an estimated 21.3 million people lacking access in 2019." Although the digital gap between urban and rural communities is narrowing, the connectivity of households in the rural areas is still below the average with only two-thirds of rural Americans reported a home broadband connection. 

<center><iframe width="560" height="315" src="us_internet_map.html" title="Internet by Percent Poverty" frameborder="0"></iframe></center>

This map showcases internet access in different states. Please take the time to hover over different states, zoom in and out, and focus on different locations on the map. Our data sources and variable definitions are all listed at the end of the essay. This map shows Alabama having the worst internet connectivity rates in the United States so we wanted why this is the case. By exploring Alabama, we can help develop targeted solutions to provide internet connection to those who need it. 

### Alabama Analysis
Exploring how internet access differs across Alabama is especially important because the lack of internet access has left many low-income, school-age disadvantaged in completing assignments and other school-related activities as compared to their high-income counterparts in a phenomenon coined by FCC Commissioner Jessica Rosenworcel called “homework gap”<sup>3</sup>. 

<center><iframe width="560" height="315" src="interactive_alabama.html" title="Internet Access Map" frameborder="0"></iframe></center>

Within Alabama, different counties have drastically different internet access rates, so we wanted to explore why some counties were outperforming others. 

<center><iframe width="560" height="315" src="dot_map_with_poverty.html" title="Internet by Percent Poverty" frameborder="0"></iframe></center>

This graph shows, as expected, that an increase in poverty is associated with a lack of internet access. However, it also shows that smaller counties and counties with a higher Black population are associated with the highest poverty and lowest rates of internet access. There is also a cluster of counties with around 20% poverty that have varying rates of internet access. Therefore, poverty is not the only indicator of internet access, and there might be ways to increase internet access without needing an overall decrease in poverty. 

Next, we wanted to determine what the effects of internet access were on education. 

<center><iframe width="560" height="315" src="dot_map_with_pct_black.html" title="Internet by Educational Attainment with Race" frameborder="0"></iframe></center>

Here, we can clearly see that having an increased internet connection leads to an increased change of obtaining at least a high school diploma. However, we recognize that correlation does not equal causation and that overall poverty levels may also be associated with educational attainment. 

<center><iframe width="560" height="315" src="dot_map_poverty_diploma.html" title="Internet by Percent Poverty" frameborder="0"></iframe></center>

Once again, this analysis shows that rural counties with large Black populations have the poorest outcomes. This conclusion is not surprising as its reported that 42 million Americans live in rural communities that don't even allow them to pruchase a broadband internet subscription -- the infrastructe to support it just does not exist.<sup>6</sup> These communities beleive that this injustice continues to slow their economic growth as people will not move to their communities due to lack of internet.<sup>6</sup> This ultimately creates a situtation where people are trapped without internet and therefore do not have access to education. 

It is important to note, that there is still work to be done even in urban areas. Within the highest performing counties, internet access rates still top out at around 85% meaning that over 1 in 10 kids do not have resources to successfully learn online. To better understand the injustices that could be affecting these communities, we wanted to analyze what some counties were doing to increase their internet access.  

## County-Specific Analysis

Although tech accessibility initiatives are not ubiquitous in all Alabama, there has been some, such as the one in called “One Laptop per Child” in  Birmingham, AL 2012  where “…some 15,000 of the group’s XO laptops were distributed to all first- through fifth-grade public school students and their teachers”<sup>4</sup>. We further narrow our scope to three Alabama counties, Montgomery, Jefferson (where Birmingham is located), and Mobile, because all three are ranked differently from most educated to least educated counties.

To better understand the three Alabama counties we chose, we first explored background statistics describing households in each county. Please click the bubbles in the chart below to examine these statistics.

<iframe srcdoc=' &lt;!doctype HTML&gt;
&lt;meta charset = &#039;utf-8&#039;&gt;
&lt;html&gt;
  &lt;head&gt;
    
    &lt;link rel=&#039;stylesheet&#039; href=&#039;//cdnjs.cloudflare.com/ajax/libs/nvd3/1.1.15-beta/nv.d3.min.css&#039;&gt;
    
    
    
    &lt;script src=&#039;//ajax.googleapis.com/ajax/libs/jquery/1.8.2/jquery.min.js&#039; type=&#039;text/javascript&#039;&gt;&lt;/script&gt;
    
    &lt;script src=&#039;//d3js.org/d3.v3.min.js&#039; type=&#039;text/javascript&#039;&gt;&lt;/script&gt;
    
    &lt;script src=&#039;//cdnjs.cloudflare.com/ajax/libs/nvd3/1.1.15-beta/nv.d3.min.js&#039; type=&#039;text/javascript&#039;&gt;&lt;/script&gt;
    
    &lt;script src=&#039;//nvd3.org/assets/lib/fisheye.js&#039; type=&#039;text/javascript&#039;&gt;&lt;/script&gt;
    
    
    &lt;style&gt;
    .rChart {
      display: block;
      margin-left: auto; 
      margin-right: auto;
      width: 600px;
      height: 400px;
    }  
    &lt;/style&gt;
    
  &lt;/head&gt;
  &lt;body &gt;
    
    &lt;div id = &#039;chart33e81fc051f1&#039; class = &#039;rChart nvd3&#039;&gt;&lt;/div&gt;    
    &lt;script type=&#039;text/javascript&#039;&gt;
 $(document).ready(function(){
      drawchart33e81fc051f1()
    });
    function drawchart33e81fc051f1(){  
      var opts = {
 &quot;dom&quot;: &quot;chart33e81fc051f1&quot;,
&quot;width&quot;:      600,
&quot;height&quot;:      400,
&quot;x&quot;: &quot;County&quot;,
&quot;y&quot;: &quot;Households&quot;,
&quot;group&quot;: &quot;Label&quot;,
&quot;type&quot;: &quot;multiBarChart&quot;,
&quot;id&quot;: &quot;chart33e81fc051f1&quot; 
},
        data = [
 {
 &quot;Label&quot;: &quot;Total Households&quot;,
&quot;County&quot;: &quot;Jefferson County&quot;,
&quot;Households&quot;: 261390 
},
{
 &quot;Label&quot;: &quot;Households with Internet&quot;,
&quot;County&quot;: &quot;Jefferson County&quot;,
&quot;Households&quot;: 203998 
},
{
 &quot;Label&quot;: &quot;Households in Poverty&quot;,
&quot;County&quot;: &quot;Jefferson County&quot;,
&quot;Households&quot;: 44730 
},
{
 &quot;Label&quot;: &quot;Total Households&quot;,
&quot;County&quot;: &quot;Mobile County&quot;,
&quot;Households&quot;: 153794 
},
{
 &quot;Label&quot;: &quot;Households with Internet&quot;,
&quot;County&quot;: &quot;Mobile County&quot;,
&quot;Households&quot;: 113049 
},
{
 &quot;Label&quot;: &quot;Households in Poverty&quot;,
&quot;County&quot;: &quot;Mobile County&quot;,
&quot;Households&quot;: 28490 
},
{
 &quot;Label&quot;: &quot;Total Households&quot;,
&quot;County&quot;: &quot;Montgomery County&quot;,
&quot;Households&quot;: 89776 
},
{
 &quot;Label&quot;: &quot;Households with Internet&quot;,
&quot;County&quot;: &quot;Montgomery County&quot;,
&quot;Households&quot;: 71197 
},
{
 &quot;Label&quot;: &quot;Households in Poverty&quot;,
&quot;County&quot;: &quot;Montgomery County&quot;,
&quot;Households&quot;: 16927 
} 
]
  
      if(!(opts.type===&quot;pieChart&quot; || opts.type===&quot;sparklinePlus&quot; || opts.type===&quot;bulletChart&quot;)) {
        var data = d3.nest()
          .key(function(d){
            //return opts.group === undefined ? &#039;main&#039; : d[opts.group]
            //instead of main would think a better default is opts.x
            return opts.group === undefined ? opts.y : d[opts.group];
          })
          .entries(data);
      }
      
      if (opts.disabled != undefined){
        data.map(function(d, i){
          d.disabled = opts.disabled[i]
        })
      }
      
      nv.addGraph(function() {
        var chart = nv.models[opts.type]()
          .width(opts.width)
          .height(opts.height)
          
        if (opts.type != &quot;bulletChart&quot;){
          chart
            .x(function(d) { return d[opts.x] })
            .y(function(d) { return d[opts.y] })
        }
          
         
        
          
        

        
        
        
      
       d3.select(&quot;#&quot; + opts.id)
        .append(&#039;svg&#039;)
        .datum(data)
        .transition().duration(500)
        .call(chart);

       nv.utils.windowResize(chart.update);
       return chart;
      });
    };
&lt;/script&gt;
    
    &lt;script&gt;&lt;/script&gt;    
  &lt;/body&gt;
&lt;/html&gt; ' scrolling='no' frameBorder='0' seamless class='rChart  nvd3  ' id='iframe-chart33e81fc051f1'> </iframe>
 <style>iframe.rChart{ width: 100%; height: 400px;}</style>

We then looked closer at each of the three county's education outcomes and racial makeup. Despite choosing them initially for their diversity of educational achievement in the three counties, the proportions of the population with different internet access types are relatively similar and the percentage of the population 25 or older with high school diploma across the three counties is relatively similar. Montgomery County, out of the three, is the only majority black county, and does have the lowest proportion of the population with a high school diploma, at 13.4%, but as mentioned above, does not differ significantly in internet access.

{::options parse_block_html="true" /}
<div class="infogram-embed" data-id="bdef3946-d43f-493f-a53a-ffd247cbd405" data-type="interactive" data-title="Jefferson County"></div><script>!function(e,i,n,s){var t="InfogramEmbeds",d=e.getElementsByTagName("script")[0];if(window[t]&&window[t].initialized)window[t].process&&window[t].process();else if(!e.getElementById(n)){var o=e.createElement("script");o.async=1,o.id=n,o.src="https://e.infogram.com/js/dist/embed-loader-min.js",d.parentNode.insertBefore(o,d)}}(document,0,"infogram-async");</script>

{::options parse_block_html="true" /}
<div class="infogram-embed" data-id="9ac5ff99-17f4-4ea1-a5ea-2199b3eae33e" data-type="interactive" data-title="Mobile County"></div><script>!function(e,i,n,s){var t="InfogramEmbeds",d=e.getElementsByTagName("script")[0];if(window[t]&&window[t].initialized)window[t].process&&window[t].process();else if(!e.getElementById(n)){var o=e.createElement("script");o.async=1,o.id=n,o.src="https://e.infogram.com/js/dist/embed-loader-min.js",d.parentNode.insertBefore(o,d)}}(document,0,"infogram-async");</script>

<div class="infogram-embed" data-id="61a8466a-9a29-4420-b50f-169460786980" data-type="interactive" data-title="Montgomery County"></div><script>!function(e,i,n,s){var t="InfogramEmbeds",d=e.getElementsByTagName("script")[0];if(window[t]&&window[t].initialized)window[t].process&&window[t].process();else if(!e.getElementById(n)){var o=e.createElement("script");o.async=1,o.id=n,o.src="https://e.infogram.com/js/dist/embed-loader-min.js",d.parentNode.insertBefore(o,d)}}(document,0,"infogram-async");</script>

{::options parse_block_html="false" /}

Jefferson County, where the Birmingham laptop to students initiative occurred in 2012, did not seem to have a significant per capita difference in educational attainment or internet access. The fact that technology accessibility, however, is complicated and involves internet access as well as laptop device access, may explain why educational attainment did not improve significantly. Simply mass distributing laptops to students and teachers is not enough if household internet access is not readily available.  

### Conclusions
Both the large-scale statewide and county case study results show that people living in rural communities are disadvantaged when it comes to internet access. In particicular, people of color are disproportionately affected. This is particularly unjust considering the reliance on internet to perform school activities in the era of COVID-19.<sup>5</sup> So while, there is an association in our graphs with lack of internet access leading to not receiving a high school diploma, we expect this discrepency will be furthered in future data. For instance, when large-scale ddata becomes available for 2020-2022, we expect that internet access will be even more strongly correlated with schooling outcomes. 

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
