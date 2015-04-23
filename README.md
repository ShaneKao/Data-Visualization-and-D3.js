# Data Visualization and D3.js  

## The differences among the performance of the baseball players

### Summary

The data set containing 1,157 baseball players including their handedness (right or left handed), height, weight, batting average, and home runs. We want to create a visualization that shows differences among the performance of the baseball players.

### Design

#### Data Visualization (R)

I downloaded the data from [Baseball Data](https://www.google.com/url?q=https%3A%2F%2Fs3.amazonaws.com%2Fudacity-hosted-downloads%2Fud507%2Fbaseball_data.csv&sa=D&sntz=1&usg=AFQjCNEkK8NRImfPdhM7cLkivKaJ0WldFA). Exploratory data analysis was conducted using Rstudio as follows: 
![Initial R Plot](https://raw.githubusercontent.com/ShaneKao/Data-Visualization-and-D3.js/master/plot/r_plot.png)

Here I put all variable in the plot as follows, nomarlly, height and weight are correlated, so I use these two variable to determine the site of data point, `handedness` is discrete, I think different shape may be a good choice, `avg` and `HR` are continuous, I use darkness and size to represent them.

* x: `height`, y: `weight`
* circle:  right handed hitter, triangle: left handed hitter, square : switch hitter
* darker color, higher batting average
* bigger size, more home run

#### Data Visualization (d3.js)

* Use different color to describe `handedness` instead of different shape(green: right handed hitter, blue: left handed hitter, red: switch hitter) 
* Adding tooltip such that the plot can traceback to the original data point
![Initial d3 Plot](https://raw.githubusercontent.com/ShaneKao/Data-Visualization-and-D3.js/master/plot/d3_plot_v1.png)

### Feedback

#### Interview #1

> Adding legend will make your plot more understandable

#### Interview #2

> The darkness of points is not obvious

#### Interview #3

> Some data points overlap, it is hard to observe the effect of different type of hitter

### Post-feedback Design

* Adding legend at the lower right corner

* There are many batter with zero batting average (23%), after scaling, the darkness of points is not obvious, hence, I drop data of `avg`=0. In order to strengthen the visual effect, I use subset which the range of `avg` in IQR

* I added a `click` event for the paragraph, so it would show different type of hitter indivisually

![Second d3 Plot](https://raw.githubusercontent.com/ShaneKao/Data-Visualization-and-D3.js/master/plot/d3_plot_v2.png)

![Third d3 Plot](https://raw.githubusercontent.com/ShaneKao/Data-Visualization-and-D3.js/master/plot/d3_plot_v3.png)

### Revised Design

I'd like to explore how height correlate to number of home runs, I make a bar chart with height on the x-axis and median home-runs on the y-axis

![Fourth d3 Plot](https://raw.githubusercontent.com/ShaneKao/Data-Visualization-and-D3.js/master/plot/d3_plot_v4.png)

### Conclude

Based on those plots, we can see batters with high height are not powerful, less likely to hit home run. 

### Resources

[Data Visualization and D3.js](https://www.udacity.com/course/ud507)

[Interactive Data Visualization for the Web](http://shop.oreilly.com/product/0636920026938.do)

### Certificate

![Certificate](https://raw.githubusercontent.com/ShaneKao/Data-Visualization-and-D3.js/master/certificate.png)
