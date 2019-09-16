# DatoFutbol
The official repository of the project Dato Fútbol

![](1001_goal.gif)

* web: http://datofutbol.cl 
* Twitter: https://twitter.com/DatoFutbol_cl


Here you can find the databases and respective processing codes related to some analysis.

There are another resources as part of this project:

* http://datofutbol.cl/satRdaySCL2018-soccer-analytics-R/index.html
* http://datofutbol.cl/revolucion-datos-soccer-analytics-seminario-UAI-2019/

Articles (Medium):

* https://medium.com/datos-y-ciencia/una-mirada-al-soccer-analytics-usando-r-parte-i-ab6b704b4c7f
* https://medium.com/datos-y-ciencia/una-mirada-al-soccer-analytics-usando-r-parte-ii-5aadb0ff6ab2
* https://medium.com/@ismaelgomezs/una-mirada-al-soccer-analytics-usando-r-parte-iii-3bdff9cd3752

Please feel free to do comments and give feedback.
Enjoy it!



```{r global_options, include=FALSE}
library(knitr)
knitr::opts_chunk$set(echo=F, warning=FALSE, message=FALSE)
```

**DATO FUTBOL** is a personal project that started in 2017 and it is focus on get a deeper knowledge in the field of Soccer (Football) Analytics. This way i've been developing different resources related, like this blog, which was created using [RStudio](https://www.rstudio.com), the package [blogdown](https://github.com/rstudio/blogdown) and deploying [Shiny](http://shiny.rstudio.com) apps for some posts.

##### Another resources here:

* A [Github](https://github.com/Bustami/DatoFutbol) repository.

* A [Twitter](https://twitter.com/DatoFutbol_cl) account.

* Conferences :

1) [Una mirada al Soccer Analytics usando R](http://datofutbol.cl/satRdaySCL2018-soccer-analytics-R/index.html)

2) [La revolución de los datos en Soccer Analytics](http://datofutbol.cl/revolucion-datos-soccer-analytics-seminario-UAI-2019/)

* Another articles about using R for Soccer Analytics (Medium):

[Parte I](https://medium.com/datos-y-ciencia/una-mirada-al-soccer-analytics-usando-r-parte-i-ab6b704b4c7f)

[Parte II](https://medium.com/datos-y-ciencia/una-mirada-al-soccer-analytics-usando-r-parte-ii-5aadb0ff6ab2)

[Parte III](https://medium.com/@ismaelgomezs/una-mirada-al-soccer-analytics-usando-r-parte-iii-3bdff9cd3752)

## Examples

Generally, to choose topics for writing depends on available data. So, i propose 3 data categories: A) Historical data, B) Event data & C) Tracking data. Here some examples:

##### 1) Historical data

*Champions ranking
<br/ >
<br/ >
```{r c1, out.width = "500px"}
include_graphics("campeones.png")
#![](campeones.png)
```
<br/ >


##### 2) Event data

*Shotmap
<br/ >
<br/ >
```{r c2, out.width = "500px"}
include_graphics("events1B.png")
#![](events1B.png)
```
<br/ >


*Passing Networks
<br/ >
<br/ >
```{r c3, out.width = "500px"}
include_graphics("events3B.png")
#![](events3B.png)
```
<br/ >
<br/ >
```{r c4, out.width = "500px"}
include_graphics("events4B.png")
#![](events4B.png)
```
<br/ >


##### 3) Tracking data

Animation with Voronoi diagrams ([code in Github](https://github.com/Bustami/DatoFutbol/tree/master/TrackingDataTest)):
<br/ >
<br/ >
```{r c5, out.width = "500px"}
include_graphics("1001_goal.gif")
#![](1001_goal.gif)
```
<br/ >

If you have any request don't hesitate to contact me by email:

##### ismaelgomezs@gmail.com
