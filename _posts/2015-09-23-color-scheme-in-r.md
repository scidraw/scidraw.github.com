---
layout: post
title: "Color scheme in R package"
description: "Color scheme in R package"
tagline: by Luye & zhoujj
category: r
tags: [color, r]
---
{% include JB/setup %}

Design color scheme for a picture is very important for presenting your good result.

<!--more-->


## Learn how to produce a graph in R

[http://www.statmethods.net/graphs/index.html](http://www.statmethods.net/graphs/index.html)

Heatmap in r

[http://sebastianraschka.com/Articles/heatmaps_in_r.html](http://sebastianraschka.com/Articles/heatmaps_in_r.html)

[http://www2.warwick.ac.uk/fac/sci/moac/people/students/peter_cock/r/heatmap/](http://www2.warwick.ac.uk/fac/sci/moac/people/students/peter_cock/r/heatmap/)


## Pick up color

w3schools

[http://www.w3schools.com/tags/ref_colorpicker.asp](http://www.w3schools.com/tags/ref_colorpicker.asp)

[http://www.stat.columbia.edu/~tzheng/files/Rcolor.pdf](http://www.stat.columbia.edu/~tzheng/files/Rcolor.pdf)

[https://www.nceas.ucsb.edu/~frazier/RSpatialGuides/colorPaletteCheatsheet.pdf](https://www.nceas.ucsb.edu/~frazier/RSpatialGuides/colorPaletteCheatsheet.pdf)

[http://www.stat.ubc.ca/~jenny/STAT545A/block14_colors.html](http://www.stat.ubc.ca/~jenny/STAT545A/block14_colors.html)

[http://colorbrewer2.org/](http://colorbrewer2.org/)

## colorRampPalette

Default R color picker

{% highlight r %}
pal <- colorRampPalette(c("red", "blue"))

plot(rnorm(1000), seq(1, 1000, by = 1)
      , col = pal(1000)
      , xlab = "x"
      , ylab = "y"
      , main = "Fun with rnorm + colorRampPalette")

# => view Plot 1

pal <- colorRampPalette(c("red", "yellow", "blue"))

plot(rnorm(1000), seq(1, 1000, by = 1)
      , col = pal(1000)
      , xlab = "x"
      , ylab = "y"
      , main = "Fun with rnorm + colorRampPalette (double rainbow)")

# => view Plot 2

pal <- colorRampPalette(c("dark blue", "light blue"))

plot(rnorm(1000), seq(1, 1000, by = 1)
      , col = pal(1000)
      , xlab = "x"
      , ylab = "y"
      , main = "Fun with rnorm + colorRampPalette (the blues)")

# => view Plot 3
{% endhighlight %}

[https://gist.github.com/jeffreyiacono/4747104](https://gist.github.com/jeffreyiacono/4747104)

[http://www.inside-r.org/r-doc/grDevices/colorRampPalette](http://www.inside-r.org/r-doc/grDevices/colorRampPalette)

## Get color scheme in R

Part 1:

[http://www.r-bloggers.com/choosing-colour-palettes-part-i-introduction/](http://www.r-bloggers.com/choosing-colour-palettes-part-i-introduction/)


Part 2:

[http://www.r-bloggers.com/choosing-colour-palettes-part-ii-educated-choices/](http://www.r-bloggers.com/choosing-colour-palettes-part-ii-educated-choices/)


