# Data Visualization and D3.js  

## The differences among the performance of the baseball players

### Summary

The data set containing 1,157 baseball players including their handedness (right or left handed), height, weight, batting average, and home runs. We want to create a visualization that shows differences among the performance of the baseball players.

### Design

#### Data Visualization (R)

I downloaded the data from [Baseball Data](https://www.google.com/url?q=https%3A%2F%2Fs3.amazonaws.com%2Fudacity-hosted-downloads%2Fud507%2Fbaseball_data.csv&sa=D&sntz=1&usg=AFQjCNEkK8NRImfPdhM7cLkivKaJ0WldFA). Exploratory data analysis was conducted using Rstudio as follows: 
![Initial R Plot](https://raw.githubusercontent.com/ShaneKao/Data-Visualization-and-D3.js/master/plot/r_plot.png)

* x: `height`, y: `weight`
* circle:  right handed hitter, triangle: left handed hitter, square : switch hitter
* darker color, higher batting average
* bigger size, more home run

#### Data Visualization (d3.js)

* Use different color to describe `handedness` instead of different shape(green: right handed hitter, blue: left handed hitter, red: switch hitter) 
* Adding tooltip such that the plot can traceback to the original data point
![Initial d3 Plot](https://raw.githubusercontent.com/ShaneKao/Data-Visualization-and-D3.js/master/plot/d3_plot_v1.png)

### Feedback
