---
title       : Course Project
subtitle    : Reproducible Pitch
author      : Talley Lattimore
job         : student
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : []            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
---

## Developing Data Products Pitch
Talley Lattimore
26 December 2015

---

## Introduction

* American football is hugely popular and statistics are becoming an increasingly important part of this.
* Players, coaches, analysts, and fans are trying to figure out how best to measure and predict performance.
* Adjusted Net Yards per Attempt (ANY/A) is one of the best and simplest statistics used to measure passing.


---

## ANY/A

* ANY/A takes into account all aspects of passing.
* It accounts for touchdowns and interceptions and subtracts sack yards from passing yards.
* It does not control for defense.
* It does not control for situation.

---

## Yards per Attempt Can Be Misleading

* Much like 2 datasets with the same mean and variance can be very different, 2 quarterbacks with the same Yards per Attempt can be very different.
* Let's imagine 2 quartbacks, A and B, both average 10 yards per attempt. At first glimpse they appear identical.
* However, a closer look reveals major differences:
* A: 3000 yds, 300 attempts, 30 touchdowns, 5 interceptions
* B: 1000 yds, 100 attempts, 4 touchdowns, 5 interceptions

```
## [1] "A:  10 Y/A,  11.25  ANY/A"
```

```
## [1] "B:  10 Y/A,  8.55  ANY/A"
```
* A and B have identical Yards per Attempt, but ANY/A goes further and shows the differences between them.
* These quarter backs are obviously very different with A being far more productive.

---

## Explanation

* ANY/A is not a mystery like some other advanced statistics.
* It is calculated with a simple equation.
* (Yards + (TDs * 20) - (Ints * 45) - SackYards)/(Atts + Sacks)
* The multipliers for TDs and Ints were not chosen at random.
* Chase Stuart that a TD pass was equivalent to a 20 yard gain while an Int was equivalent to a 45 yd loss.
* ANY/A is a simple stastic, but it is a hassle to calculate. This app does that calculation for you.
