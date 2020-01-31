# 432 Spring 2020 Class 07: 2020-02-04

## Key Materials

Slides in PDF | Slides in R Markdown | Audio Recording | Need Help?
------------: | :------------------: | :--------------: | ---------------------------
[Class 07 Slides](https://github.com/THOMASELOVE/2020-432/blob/master/classes/class07/432_2020_slides07.pdf) | [Class 07 .Rmd](https://github.com/THOMASELOVE/2020-432/blob/master/classes/class07/432_2020_slides07.Rmd) | [Shared Drive](http://bit.ly/432-2020-audio) | Email **431-help at case dot edu** or visit [Office Hours](https://github.com/THOMASELOVE/2020-432/blob/master/calendar.md#tas-and-office-hours)

## Today's Announcements

1. I revised the Week 3 Slides ([PDF](https://github.com/THOMASELOVE/2020-432/blob/master/classes/class06/432_2020_week03.pdf), [RMarkdown](https://github.com/THOMASELOVE/2020-432/blob/master/classes/class06/432_2020_week03.Rmd)) to fix a typo in the denominator of Specificity in slide 39.
2. I added the [ModernDive example with interaction and parallel slope plots](https://github.com/THOMASELOVE/2020-432/blob/master/classes/class06/modern_dive_example.md) that were missing in Class 6.
3. rstudio::conf2020 was last week. 
    - [RStudio, Inc. is now RStudio, PBC](https://blog.rstudio.com/2020/01/29/rstudio-pbc/). PBC stands for Public Benefit Corporation. The first of their Public Benefit Reports is [now available](https://rstudio.com/about/pbc-report/).
    - Check out [Emily's ggplot2 nails](https://twitter.com/AmeliaMN/status/1223033747030757376?s=20).
4. The [Stats and Stories podcast](https://statsandstories.net/health1/the-philosophy-of-biostatistics) episode for last Thursday was Frank Harrell, on his recent efforts to write down a Philosophy of Biostatistics. It's brief, and [there's a transcript](https://statsandstories.net/health1/the-philosophy-of-biostatistics). A lot of Frank's work is now at [DataMethods](https://discourse.datamethods.org/).

## On Your Project, Sample Size and Logistic Regression Models

When fitting regression models, a common question is "how big a sample do I need?"

This depends on a lot of things, including what you want to use to determine whether a regression model is strong enough. For linear regression, most people who want to build a simple rule base it on the number of predictors, P, that you intend to consider in your modeling. As a starting point, I would recommend that if N (your sample size) is 100P or larger, then you'll likely be able to distinguish R-squared values pretty meaningfully down to the second decimal place, so that an R-squared of 0.32 really does mean something different from 0.31. Some of my motivation from this comes from this [old post by Frank Harrell on StackExchange](https://stats.stackexchange.com/posts/59128/revisions).

To fit a logistic regression model, we need a larger sample size, given the same number of predictors. [This tweet](https://twitter.com/f2harrell/status/936230071219707913?lang=en) links to some details. One set of "rules" I use is:

1. Select the number of predictors you want to study in your logistic regression (includes everything you plan to consider, regardless of whether it makes it into your final model) and call that P.
2. Denote the sample size as follows - if you have an outcome where you have N1 people with "1" and N0 people with "0" then let N = min(N0, N1).
3. To fit a logistic regression model with P+1 coefficients (adding one for the intercept) you need that N to be at least 96 + 8P, realistically, in order to get a margin of error of +/- 0.1 in estimating probabilities.

- So if you have a rare event that occurs less than 96 times, your logistic regression model will be so weak that even an intercept won't be reliably estimated.
- For the project, I'd operationalize this to say that if both "1" and "0" occur 200 times, they should be fine for our purposes for any sample size up to 1000.
- For people with fewer than 256 observations overall, their logistic regression models will be very weak, since even with just 4 predictors, you'd really want 128 "1" and 128 "0" results. 
- Since I've set the minimum sample size for Project 1 at 100, there will be some people in that setting. The rule I'll apply in future versions of the course will require at least 400 observations on all data, and at least 200 "1" and 200 "0" in their binary outcome. If you can meet that standard with the data set you plan to use, great. If not, prepare for your logistic regression model to be a little disappointing.

## Next Few Deliverables (from [the Course Calendar](https://github.com/THOMASELOVE/2020-432/blob/master/calendar.md))

Date | Deliverable
---------: | -----------------------------------------------------------------------
Today | [Homework 2](https://github.com/THOMASELOVE/2020-432/tree/master/homework/hw02) due at 5 PM.
Tomorrow | You should have your data for [Project 1](https://github.com/THOMASELOVE/2020-432/tree/master/projects/project1) in hand.
Thursday | Read *The Art of Statistics* Chapter 7 (Estimates and Intervals)
Friday | There will be a Minute Paper after Class 8 due at 2 PM. **Link to come.**
2020-02-11 | [Homework 3](https://github.com/THOMASELOVE/2020-432/tree/master/homework/hw03) due at 5 PM. 
2020-02-13 | Read *The Art of Statistics* Chapter 8 (Probability)
2020-02-14 | [Project 1 Proposal](https://github.com/THOMASELOVE/2020-432/tree/master/projects/project1) due at 2 PM.

## One Last Thing: The Iowa Caucuses are Tonight.

Caucuses are especially hard to predict, and the Iowa Caucus is going to be especially hard to predict this year:

- [The Iowa Caucuses Are In 4 Days. Almost Anything Could Still Happen](https://fivethirtyeight.com/features/the-iowa-caucuses-are-in-4-days-almost-anything-could-still-happen/) by Nate Silver (2020-01-30)
- [Bernie Sanders is the Iowa favorite, but he is far from a sure thing](https://www.cnn.com/2020/01/30/politics/bernie-sanders-polls-analysis/index.html) by Harry Enten (2020-01-30)
- [Election Update: A New Batch Of Iowa Polls Still Shows A Tight Race Between Sanders And Biden](https://fivethirtyeight.com/features/election-update-a-new-batch-of-iowa-polls-still-shows-a-tight-race-between-sanders-and-biden/) by Geoffrey Skelly (2020-01-29)
- [Where Are All The Iowa Polls This Year?](https://fivethirtyeight.com/features/where-are-all-the-iowa-polls-this-year/) by Geoffrey Skelly (2020-01-31)
- [What You Should Know about Primaries and Caucuses](https://fivethirtyeight.com/features/what-you-should-know-about-primaries-and-caucuses/) by Anna Rothschild and Galen Druke

We'll take a moment this afternoon to check in on:

- [RealClearPolitics' Poll Average for Iowa](https://www.realclearpolitics.com/epolls/2020/president/ia/iowa_democratic_presidential_caucus-6731.html)
- [The PredictIt Prediction Market for the Iowa Caucuses](https://www.predictit.org/markets/detail/5241/Who-will-win-the-2020-Iowa-Democratic-caucuses) and, of course,
- [FiveThirtyEight's Forecast for Iowa](https://projects.fivethirtyeight.com/2020-primary-forecast/iowa/)

