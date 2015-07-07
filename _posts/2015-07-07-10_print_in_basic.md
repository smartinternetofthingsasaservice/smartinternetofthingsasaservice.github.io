---
title  : 10 PRINT in R
author : Jonas Schöley
date   : 2015-07-07
tags   : rstats fun basic
layout : post
---

![](/assets/2015-07-07-10_print_in_r/10_print.png)

Currently I'm reading [`10 PRINT`](http://10print.org/), *"a book about a one-line Commodore 64 `BASIC` program."* I covered the program using `R`.

```r
repeat cat(ifelse(round(runif(1)),"╱","╲"))
```

You will need a terminal with Unicode support in order to replicate the output.

cc-by Jonas Schöley