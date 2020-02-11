432 Homework 2
================

# The Answer Sketch (and Grading Rubric) for Homework 2 is now available.

- [PDF](https://github.com/THOMASELOVE/2020-432/blob/master/homework/hw02/sketch/sketch_hw2.pdf) including both the sketch and rubric.
- [R Markdown](https://github.com/THOMASELOVE/2020-432/blob/master/homework/hw02/sketch/sketch_hw2.Rmd) used to build the PDF.
- As of 2020-02-11, Homework 2 grades are now posted to http://bit.ly/432-2020-grades. Check your email for your HW-Code.


# General Instructions

Submit your work via [Canvas](https://canvas.case.edu/). The deadline is
specified on [the Course
Calendar](https://github.com/THOMASELOVE/2020-432/blob/master/calendar.md).

  - Your response should include an R Markdown file and an HTML document
    that is the result of applying your R Markdown file to the
    `oh_counties_2017.csv` data, available in the main directory for
    this homework, as well as on our Data and Code page.
  - Start a separate R Project for Homework 2, as your first step, and
    place the data in that project’s directory or (perhaps better) in a
    data sub-directory.
  - In all of our homeworks, do not include R output without complete
    sentences describing what you are doing in each step, and what you
    conclude from that work.

## Data Set for this Assignment

The `oh_counties_2017.csv` data set I have provided describes a series
of variables, pulled from the data for the 88 counties of the the State
of Ohio from the [County Health
Rankings](http://www.countyhealthrankings.org/rankings/data/oh) report
for 2017.

  - You may also be interested in looking at the details of the [2017
    Ohio Summary report
    (pdf)](http://www.countyhealthrankings.org/sites/default/files/state/downloads/CHR2017_OH.pdf),
    or at the [Excel data
    file](http://www.countyhealthrankings.org/sites/default/files/state/downloads/2017%20County%20Health%20Rankings%20Ohio%20Data%20-%20v2.xls)
    from which I created the `oh_counties_2017.csv` file.
  - Note that later data sets are now available, but we will concentrate
    in this assignment on the 2017 results.

The available variables are listed below. Each variable describes data
at the **COUNTY** level.

|        Variable        | Description                                                                                                                        |
| :--------------------: | ---------------------------------------------------------------------------------------------------------------------------------- |
|          fips          | Federal Information Processing Standard code                                                                                       |
|         county         | name of County                                                                                                                     |
|   years\_lost\_rate    | age-adjusted years of potential life lost rate (per 100,000 population)                                                            |
|     sroh\_fairpoor     | % of adults reporting fair or poor health (via BRFSS)                                                                              |
|       phys\_days       | mean number of reported physically unhealthy days per month                                                                        |
|       ment\_days       | mean number of reported mentally unhealthy days per mo                                                                             |
|        lbw\_pct        | % of births with low birth weight (\< 2500 grams)                                                                                  |
|      smoker\_pct       | % of adults that report currently smoking                                                                                          |
|       obese\_pct       | % of adults that report body mass index of 30 or higher                                                                            |
|       food\_env        | indicator of access to healthy foods, in points (0 is worst, 10 is best)                                                           |
|     inactive\_pct      | % of adults that report no leisure-time physical activity                                                                          |
|      exer\_access      | % of the population with access to places for physical activity                                                                    |
|       exc\_drink       | % of adults that report excessive drinking                                                                                         |
|       alc\_drive       | % of driving deaths with alcohol involvement                                                                                       |
|       sti\_rate        | Chlamydia cases / Population x 100,000                                                                                             |
|      teen\_births      | Teen births / females ages 15-19 x 1,000                                                                                           |
|       uninsured        | % of people under age 65 without insurance                                                                                         |
|       pcp\_ratio       | Population to Primary Care Physicians ratio                                                                                        |
|       prev\_hosp       | Discharges for Ambulatory Care Sensitive Conditions/Medicare Enrollees x 1,000                                                     |
|        hsgrads         | High School graduation rate                                                                                                        |
|       unemployed       | % of population age 16+ who are unemployed and looking for work                                                                    |
|       poor\_kids       | % of children (under age 18) living in poverty                                                                                     |
|     income\_ratio      | Ratio of household income at the 80th percentile to income at the 20th percentile                                                  |
|      associations      | \# of social associations / population x 10,000                                                                                    |
|         pm2.5          | Average daily amount of fine particulate matter in micrograms per cubic meter                                                      |
|        h2oviol         | Presence of a water violation: Yes or No                                                                                           |
|      sev\_housing      | % of households with at least 1 of 4 housing problems: overcrowding, high housing costs, or lack of kitchen or plumbing facilities |
|      drive\_alone      | % of workers who drive alone to work                                                                                               |
|   age.adj.mortality    | premature age-adjusted mortality                                                                                                   |
|        dm\_prev        | % with a diabetes diagnosis                                                                                                        |
|  freq\_phys\_distress  | % in frequent physical distress                                                                                                    |
| freq\_mental\_distress | % in frequent mental distress                                                                                                      |
|     food\_insecure     | % who are food insecure                                                                                                            |
|     insuff\_sleep      | % who get insufficient sleep                                                                                                       |
|     health\_costs      | estimated mean health care costs                                                                                                   |
|     median\_income     | estimated median income                                                                                                            |
|       population       | population size                                                                                                                    |
|       age65plus        | % of population who are 65 and over                                                                                                |
|       african-am       | % of population who are African-American                                                                                           |
|        hispanic        | % of population who are of Hispanic/Latino ethnicity                                                                               |
|         white          | % of population who are White                                                                                                      |
|         female         | % of population who are Female                                                                                                     |
|         rural          | % of people in the county who live in rural areas                                                                                  |

# Question 1 (20 points)

Create a visualization (using R) based on some part of the
`oh_counties_2017.csv` data set, and share it (the visualization and the
R code you used to build it) with us. The visualization should be of a
professional quality, describe information from at least three different
variables listed above, include proper labels and a title, as well as a
caption of no more than 50 words that highlights the key result.
Although you may fit a model to help show patterns, your primary task is
to show **the data** in a meaningful way, rather than to simply
highlight the results of a model.

  - You are welcome to find useful tools for visualizing data in R that
    we have yet to see in the slides in class, but which you’ve found in
    your reading of David Spiegelhalter’s *The Art of Statistics* or in
    other venues.
  - We will grade Question 1 strictly based on the quality of the
    visualization, its title and caption, in terms of being attractive,
    well-labeled and useful for representing the County Health Rankings
    data for Ohio, and how well it adheres to general principles for
    good visualizations we’ve seen in 431 and 432.

# Question 2 (20 points)

Write an essay (between 150 and 250 words) describing the creation and
meaning of the visualization you created in Question 1, providing us
with the context we need to understand why this is a useful
visualization. In your short description, be sure to address:

  - How does this visualization help its audience understand the data
    better?
  - Why is this particular visualization effective, and what are the
    design features it uses that we can learn from to help us make more
    effective visualizations?

# Question 3 (20 points)

Create a linear regression model to predict `obese_pct` as a function of
`food_env` adjusting for `median_income`, and treating all three
variables as quantitative, using all counties with complete data on
those three variables. Specify and then carefully interpret the
estimated coefficient of `food_env` and a 90% uncertainty interval
around that estimate in context using nothing but complete English
sentences. A model using main effects only, entered as linear
predictors, will be sufficient.

# Question 4 (10 points)

Evaluate the quality of the model you fit in Question 3 in terms of
adherence to regression modeling assumptions, through the specification
and written evaluation of residual plots and other diagnostics. What
might be done to improve the fit of the model you’ve developed in
Question 3? Identify by name any outlying counties, in terms of the
relationship you’re studying, and explain why they are flagged as
outliers.

# Question 5 (20 points)

Create a logistic regression model to predict the presence of a water
violation (as contained in `h2oviol`) on the basis of `sev_housing` and
`pm2.5`. Specify and then carefully interpret the estimated coefficient
of `sev_housing` and a 90% uncertainty interval around that estimate in
context using nothing but complete English sentences. A model using main
effects only, entered as linear predictors, will be sufficient.

# Question 6 (10 points)

Produce and interpret the meaning of a confusion matrix which describes
the quality of the predictions you have developed in Question 5. How
well does the model you fit make predictions about `h2oviol`?

### Please add the session information.

Finally, at the end of this homework and all subsequent assignments
(including the projects), please add the session information. My
preferred way for you to do this is:

``` r
sessioninfo::session_info()
```

### This is the end of Homework 2.
