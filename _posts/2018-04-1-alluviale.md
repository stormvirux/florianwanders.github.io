---
layout: post
title: Hello Hydeout
excerpt_separator:  <!--more-->
---

Learned: If something is not working, check first if it is indeed not working. 

A colleague wanted to change the colors in an alluviale plot. The code included `scale_fill_brewer(type = "qual", palette = "Set1")` from the [vignette](https://cran.r-project.org/web/packages/ggalluvial/vignettes/ggalluvial.html), but coloring did not seem to work. So I decided to get I to work with a hack: 


```r
library(grid)
g <- 
gg <- ggplot_build(g)
gg
```


gg[["data"]][[1]][["fill"]] [gg[["data"]][[1]][["fill"]]=="#F8766D"] <- "red"
gg[["data"]][[1]][["fill"]] [gg[["data"]][[1]][["fill"]]=="#00BFC4"] <- "green"

```