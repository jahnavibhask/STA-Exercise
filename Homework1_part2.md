---
title: "STA426_Homework_1"
author: "JB"
date: "25 September 2018"
output:
  html_document:
    keep_md: True
---



## R Markdown

###Drawing samples from log normal distribution with given mean and sd


```r
m <- 1
sd <- 0.25
mean_norm_dist <- log(m^2 / sqrt(sd^2 + m^2))
sd_norm_dist <- sqrt(log(1 + (sd^2 / m^2)))

sample_draw <- rlnorm(n=100, mean_norm_dist, sd_norm_dist)
print(mean_norm_dist)
```

```
## [1] -0.03031231
```

```r
print(sd_norm_dist)
```

```
## [1] 0.2462207
```

###Plotting histogram of distribution


```r
hist(sample_draw,
     main = "Histogram of Samples")
```

![](Homework1_part2_files/figure-html/unnamed-chunk-2-1.png)<!-- -->

###Plotting histogram of of log transformed distribution


```r
hist(log(sample_draw),
     main = "Histogram of log transformed samples")
```

![](Homework1_part2_files/figure-html/unnamed-chunk-3-1.png)<!-- -->
