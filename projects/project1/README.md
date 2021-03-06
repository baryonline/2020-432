Instructions for 432 Project 1
================

  - [Introduction](#introduction)
      - [Project 1 involves two tasks.](#project-1-involves-two-tasks.)
      - [Am I working alone, or in a
        group?](#am-i-working-alone-or-in-a-group)
      - [What Makes an Acceptable Data
        Set?](#what-makes-an-acceptable-data-set)
  - [Deliverable 1. The Proposal](#deliverable-1.-the-proposal)
      - [The Nine Parts of Your
        Proposal](#the-nine-parts-of-your-proposal)
          - [Evaluating the Project 1
            Proposal](#evaluating-the-project-1-proposal)
      - [NEW\! Some Additional Thoughts after reviewing the Proposal
        Drafts](#new-some-additional-thoughts-after-reviewing-the-proposal-drafts)
      - [NEW\! Project 1 Portfolio
        Templates](#new-project-1-portfolio-templates)
      - [NEW\! The Group Meetings are
        Cancelled](#new-the-group-meetings-are-cancelled)
  - [NEW\! Deliverable 2. The Poster and The
    Portfolio](#new-deliverable-2.-the-poster-and-the-portfolio)
      - [The Portfolio](#the-portfolio)
          - [Section 10: Linear Regression
            Analyses](#section-10-linear-regression-analyses)
          - [Section 11: Logistic
            Regression](#section-11-logistic-regression)
          - [Section 12: The Discussion](#section-12-the-discussion)
      - [NEW\! The Poster](#new-the-poster)

As a substantial part of your course grade, you will complete two
Projects this semester. This document describes Project 1. Instructions
for Project 2 will appear later in the term.

# Introduction

It is hard to learn statistics (or anything else) passively; concurrent
theory and application are essential. Expert clinical researchers and
statisticians repeatedly emphasize how important it is that people be
able to write well, present clearly, work to solve problems, and show
initiative. This project assignment is designed to help you develop your
abilities and have a memorable experience.

In Project 1, you will be analyzing, presenting and discussing a pair of
regression models, specifically a linear regression and a logistic
regression, describing a data set you identify.

## Project 1 involves two tasks.

1.  Develop a proposal, which includes a presentation of the data. This
    proposal is due in mid-February. The proposal is graded by the TAs
    using a formal rubric prepared by Dr. Love. You will iterate (as
    necessary) on your proposal until you receive full credit. The
    proposal is worth 25% of the project 1 grade, and the portfolio
    version of the portfolio that you will submit as part of the second
    task is worth another 25%.

2.  Develop an electronic poster of your work. This poster is due in
    early March. The poster is evaluated by Dr. Love. The poster is
    worth the remaining 50% of the project 1 grade.

See the [Course
Calendar](https://github.com/THOMASELOVE/2020-432/blob/master/calendar.md)
for deadlines.

## Am I working alone, or in a group?

You can choose either to work alone, or with one other person, to
complete Project 1.

  - At times, we may require you to share drafts of your work with other
    people in small groups, but the actual data collection, analysis and
    report-building work is for you (or you and your partner) to do.

## What Makes an Acceptable Data Set?

1.  **Shareable with the World**. The data must be available to you, and
    shared with me and everyone else in the world (without any
    identifying information) as a well-tidied .csv file on 2020-02-14.
    If the data is from another source, the source (web or other) must
    be completely identified to me. Ongoing projects that require
    anyone’s approval to share data are not appropriate for Project 1,
    but can be used (with Dr. Love’s approval) for Project 2.
    
      - You should have the data in R by 2020-02-05, so that you will
        have sufficient time to complete the other elements of this
        proposal. Any data you cannot have by that time is a bad choice.
      - For Project 1, you may not use any data set that was used in the
        431 or 432 teaching materials. You may not use any data set
        included in [an R package that we are
        installing](https://github.com/THOMASELOVE/2020-432/blob/master/software.md)
        this semester, other than NHANES.
      - You must use meaningfully different data sets in 432 Projects 1
        and 2.
      - You **are** allowed to use NHANES data in Project 1, but only if
        you are combining information from at least three NHANES data
        sets. If you used NHANES data in your 431 project, you can use
        NHANES data again this semester, but you must study new
        outcomes.
      - You are permitted to use BRFSS data, but you are not permitted
        to use data from SMART BRFSS, since we will be using that
        regularly in class.

2.  **Size**. A **minimum** of 100 complete observations are required on
    each variable. It is fine if there are some missing values, as well,
    so long as there are at least 100 rows with complete observations on
    all variables you intend to use in each model. The **maximum** data
    set size is 1000 observations, so if you have something larger than
    that, you’ll need to select a subset.

3.  **Outcomes**. The columns must include at least one quantitative
    outcome and one binary categorical outcome. If necessary, the binary
    outcome can be generated from the quantitative outcome (as an
    example, your quantitative outcome could be resting heart rate in
    beats per minute, and your binary outcome could be whether the
    resting heart rate is below 70 beats per minute.)

4.  **Inputs**. You will need at least four regression inputs
    (predictors) for each of your two models. At least one of the four
    must be quantitative (a variable is **not** quantitative for this
    purpose unless it has at least 10 different, ordered, observed
    values), *and* at least one must be multi-categorical (with at least
    3 categories, each containing a minimum of 30 subjects) for each
    model. Your other inputs can represent binary, multi-categorical or
    quantitative data. You can examine different candidate predictors
    for each outcome, or use the same ones in both your linear and
    logistic regression models. Depending on your sample size, you can
    study more regression inputs. Specifically, if you have N complete
    observations in your data set, you are permitted to study up to 4 +
    (N-100)/100 candidate regression inputs, rounding down.

# Deliverable 1. The Proposal

The proposal is to be submitted via file uploads to
[Canvas](https://canvas.case.edu).

Your proposal will include - (a) a single `.csv` file of the data you
have chosen - (b) a R Markdown file containing the information listed
below, and - (c) an HTML document which is the unedited result of
knitting your Markdown file.

## The Nine Parts of Your Proposal

*Title*: Your project should have a meaningful title (not 432 Proposal)
but rather something describing your actual data and plans. Please keep
the title to no more than 85 characters, including spaces.

The nine pieces of information we should find in the Markdown and HTML
versions of your proposal (with the section names we prefer in **bold**)
are:

1.  **Data Source** Complete information on the source of the data: how
    did you get it, how was it gathered, by whom, in what setting, for
    what purpose, and using what sampling strategy.
2.  **Loading and Tidying the Data** Code to load the raw `.csv` file
    into a tibble, and tidy/clean up the data to be useful for your
    modeling work.
3.  **Listing of the Tibble** A listing of the tibble, with all
    variables correctly imported (via your code) as the types of
    variables (factor/integer/numeric, etc.) that you need for modeling.
    Be sure that your listing specifies the number of rows and number of
    columns in your tidy data set. This should be a listing, not a
    glimpse or anything else.
4.  **The Subjects** A description (one or two sentences) of who or what
    the subjects (rows) are in your data set.
5.  **The Code Book** A code book, which provides, for each variable in
    your tibble, the following information:
      - The name of the variable used in your tibble
      - The type of variable (binary, multi-categorical, quantitative)
      - The details for each variable
          - if a categorical variable, what are the levels, and what %
            of subjects fall in each category
          - if a quantitative variable, what is the range of the data,
            and what are the units of measurement
          - if there are missing data, tell us how many observations are
            missing, and why, if you know why.
6.  **Describing the Variables** A sentence or two for each variable
    (column) providing a description of what the variable measures or
    describes, in English.
      - Please use the variable names that appear in your code book and
        tibble in this section, along with their description. We prefer
        that you put the variable names in `codefont` by surrounding
        them with the \` symbol, in Sections 5-8.
7.  **Plans for the Linear Regression** A sentence or two telling us
    what you will use your linear regression model to explain or
    predict, *followed by* a sentence or several telling us very
    precisely which (quantitative) variable will serve as your outcome
    in your linear regression model, and which four (or more) candidate
    predictors you intend to use for that model.
      - Please use the variable names that appear in your code book and
        tibble in this section, along with their description. We prefer
        that you put the variable names in `codefont` by surrounding
        them with the \` symbol, in Sections 5-8.
8.  **Plans for the Logistic Regression** A sentence or two telling us
    what you will use your logistic regression model to explain or
    predict, *followed by* a sentence or several telling us very
    precisely which (binary) variable will serve as your outcome in your
    logistic regression model, and which four (or more) candidate
    predictors you intend to use for that model.
      - Please use the variable names that appear in your code book and
        tibble in this section, along with their description. We prefer
        that you put the variable names in `codefont` by surrounding
        them with the \` symbol, in Sections 5-8.
9.  **Affirmation** This section contains affirmation that the data set
    meets all of the requirements specified here, most especially that
    the data can be shared freely over the internet, and that there is
    no protected information of any kind involved. You need to be able
    to write “I am certain that it is completely appropriate for these
    data to be shared with anyone, without any conditions. There are no
    concerns about privacy or security.” If you are unsure whether this
    is true, select a different data set.
      - If you need to provide any **references**, we prefer that you
        create a subsection here called **References** before the
        session information and after the affirmation.
      - This affirmation should be followed by a subsection containing
        the **Session Information**, for which we’d like you to use
        `sessioninfo::session_info()`.

### Evaluating the Project 1 Proposal

  - Your project will be evaluated on a scale of 0-10, with one point
    for submitting all necessary materials (.csv, .Rmd and HTML)
    successfully, and then one additional point for each of the nine
    tasks if they are successfully completed.
  - If you receive a grade lower than 10, you will need to redo until
    you reach 10.

The full [Project 1 Proposal
Rubric](https://github.com/THOMASELOVE/2020-432/blob/master/projects/project1/project1_proposal_rubric.md)
is available now. Please review that material closely, so that your
submission will meet all requirements and score a 10 on the first try.

## NEW\! Some Additional Thoughts after reviewing the Proposal Drafts

  - Revised proposals are due 2020-02-24 at 9 AM. We will attempt to
    finish reviewing those revisions by 9 PM on 2020-02-24.
  - If an additional revision is required, it will be due 2020-02-26 at
    9 AM.

Every proposal should …

  - **not** use `skim_with(numeric = list(hist = NULL), integer =
    list(hist = NULL))` since it leads to a lengthy and pointless
    function listing. If you want to skim without charts use
    `skim_without_charts` which came into existence in 2019.
  - **not** use `source("Love-boost.R")` or any other R script or
    package unless you actually need something it provides
  - have a meaningful **title** (not containing 432 or Proposal)
    containing no more than 85 characters, including spaces
  - load the tidyverse last, and not anywhere else, and avoid loading
    other packages that are loaded already by the tidyverse. The
    complete list of packages that the tidyverse loads is [the set of
    core packages listed at this
    link](https://www.tidyverse.org/packages/).
  - should use **code-folding** in the HTML result (add code\_folding:
    show to your YAML)
  - should use the **tidyverse** for data management, almost without
    exception
  - use appropriate subsection headings (which you identify with
    hashtags on new lines in your R Markdown file) and with numbers
    automatically applied by R to match the task list numbering
      - Be sure `number_sections: true` is in your YAML section at the
        top of your R Markdown file.
      - to create a numbered section called “Data Source”, use the code
        `# Data Source` preceded and followed by a blank line in your R
        Markdown file
      - to create a numbered subsection called “First Source”, use the
        code `## First Source` preceded and followed by a blank line in
        your R Markdown file
      - to create an unnumbered section called “Packages”, use the code
        `# Packages {-}` preceded and followed by a blank line in your R
        Markdown file
  - use `message = FALSE` in the code chunk where the packages are
    listed to eliminate the messages in the HTML showing warnings about
    when packages were built or how objects were masked
  - use `comment = NA` in the setup chunk to avoid R output being
    preceded by hashtags `##`
  - be run using **R version 3.6.2** or later, and include **session
    info** at the end of the document by running the
    `sessioninfo::session_info()` function.
  - use the ENTER key sufficiently to prevent any code chunks in the
    HTML file from requiring a scrolling window in order to be seen
    (note that this is a particularly common problem when people list
    many, many packages on the same line, separated by semicolons)
  - use `clean_names()` to clean up the names in the variables in the
    final tidied version of the data, and have no names that are longer
    than they need to be (10 characters or less is a good plan for
    variable names)
  - should have a completely tidied data set at the end of Section 2,
    and should
  - include a **tidied version of the data file**, in .csv format,
    perhaps in addition to the raw data, and this tidied version should
    adhere to the requirements for minimum and maximum number of rows
    and columns, with a row (subject) identifier at the far left of the
    .csv file. This is a new and additional requirement for the revised
    proposal, to demonstrate that you’ve done the necessary work.

## NEW\! Project 1 Portfolio Templates

I built three templates to make it a little easier to meet the
requirements specified here. You’ll find them [at this
link](https://github.com/THOMASELOVE/2020-432/tree/master/projects/project1/templates).
You are not required to use a template, but it might be helpful to you,
and the use of one should help you avoid some problems and produce an
attractive proposal or portfolio result.

## NEW\! The Group Meetings are Cancelled

  - On 2020-02-27, we will no longer be meeting as a group. The TAs will
    be available for office hours on that day, as usual.

# NEW\! Deliverable 2. The Poster and The Portfolio

## The Portfolio

The portfolio submission for Project 1 consists of 13 sections, 10 of
which come (essentially) straight from the proposal, and the last of
which requires a single line of code in R. The truly new sections are
10, 11 and 12, and we explain those sections below.

  - Any preliminaries (including loading packages) should be placed in
    an unnumbered section called **Preliminaries** that can have as many
    subsections as you need.
  - Sections 1-8 are exactly the same as what you prepared for the
    proposal. You should nail down any details that were not yet
    specified in your original submissions of the proposal. Sections
    5-8, in particular, should be adjusted as necessary to reflect the
    actual analyses you wound up doing.
  - Section 9 is now just the **Affirmation** that the data can be
    shared with us, as we’re moving the session info and references (if
    needed) to the bottom of the document.
  - Section 10 is **new**, should be labeled “Linear Regression
    Analyses” and is dedicated to that work.
  - Section 11 is **new**, should be labeled “Logistic Regression
    Analyses” and is dedicated to that work.
  - Section 12 is also **new**, should be labeled “Discussion” and is a
    roughly 200 word discussion of your thoughts on the process of
    producing this project.
  - Section 13 is the session information material, labeled **Session
    Information**, which should show that you’re using R 3.6.2 or later.
      - Our preferred way for you to execute this is to run
        `sessioninfo::session_info()`.
      - If you need to have a section called **References** we would
        like you to place that just before the session information
        (making **References** section 13 and **Session Information**
        section 14.)

### Section 10: Linear Regression Analyses

In Section 10, we expect you to present all relevant code used to
produce your final results. No output should be presented in this
section (or in Section 11) without commentary. This should describe the
fitting and evaluation of two models: a “main effects” model (model A),
and an “augmented” model (model B). We’re primarily interested in a
clear presentation. The following 8 elements should be presented, in
properly labeled subsections of section 10, using the labels in bold
below.

1.  **Missingness** your approach to dealing with missing data, if
    applicable
      - we prefer imputation (simple or multiple) to complete case
        analysis, but it’s not mandatory
      - if you have a sample with no missing data, specify that (again)
        here
2.  **Outcome Transformation** your approach to transforming the outcome
    variable, including an appropriate Box-Cox assessment
3.  **Scatterplot Matrix and Collinearity** a scatterplot matrix
    including the (possibly transformed) outcome and all predictors that
    make it into your “main effects” model
      - be sure to evaluate collinearity between predictors, either
        through perusing and discussing the correlations in the
        scatterplot matrix, or with variance inflation factors
4.  **Model A**: your initial “main effects” model
      - remember that your model must include at least four predictors,
        of which at least one must be quantitative and one must be
        multi-categorical.
      - we discourage the use of best subsets or other model selection
        strategies here, instead please use your problem-based
        understanding to select variables and use them all.
      - in presenting your main effects model you should show:
          - a tidied table of regression coefficients
          - key fit summary statistics like R-square, AIC and BIC, and
            we also suggest you develop and display a validated R-square
            statistic using the `validate` function in `ols` here.
          - the four key diagnostic plots of residuals, with an
            appropriate interpretation of what you see
5.  **Non-Linearity** your process for making decisions about how to
    capture potential non-linearity
      - what did the Spearman rho-squared plot suggest and how did you
        spend your degrees of freedom
          - If the (apparently strongest - furthest to the right)
            predictor in the rho-square plot is quantitative, you should
            be thinking first about a restricted cubic spline with 4
            knots, maybe 5,
          - If the largest rho-square is associated with a binary or a
            multi-categorical predictor, create an interaction term with
            the second-largest rho-squared predictor.
          - If you still have degrees of freedom you’re willing to spend
            after this, proceed down to the second largest predictor in
            terms of rho-squared, and proceed similarly to the third
            largest after that.
      - Regardless of your sample size, please use between 3 and 6
        additional degrees of freedom beyond the main effects model to
        account for non-linearity, and add no more than 3 non-linear
        terms to your model.
6.  **Model B**: fitting your “augmented model” incorporating non-linear
    terms
      - unless you’re doing multiple imputation you’ll want to be sure
        you demonstrate that you can fit this using either `ols` or
        `lm`, since you might need either approach for a complete
        assessment of the model (if you’re doing multiple imputation,
        you can stick with `ols`)
      - you’ll need at a minimum to present a nomogram and plot of the
        effects from `plot(summary(modelname))` for this augmented
        model, using `ols`.
      - you’ll want to look at an ANOVA comparison of Model B to Model A
        in order to understand whether the changes you’ve made led to
        statistically detectable improvements in prediction.
      - you’ll also need to present the residual plots for the model
        you’ve fit, which is easiest to do if you fit the model with
        `lm`.
          - if you’ve used multiple imputation, prepare a residuals
            vs. fitted values plot and evaluate it using `ols`.
7.  **Validating the Models** the results of a validation comparison of
    the “augmented model” B to the “main effects” model A which should
    help you select a “final model” from the two possibilities. Feasible
    ways to do this include:
      - an initial partition into training and test samples,
      - or a k-fold cross-validation strategy,
      - you may also want to produce validated R-square statistics for
        Model B within `ols` through the `validate` function and present
        a comparison of results across the two models
8.  **Final Model** This section should end with a clear statement of
    the model you prefer (the “main effects model A” or the “augmented
    model B”) based on your overall assessment of fit quality, adherence
    to assumptions as seen in residuals, and whether adding the terms in
    the augmented model yields an improvement that is worth the
    complication of adding the non-linear terms.
      - You should land on a single, final model, using both statistical
        and non-statistical considerations to make a decision between
        model A and model B.
      - An appropriate summary of the final model you landed on should
        start with a listing of the model parameters for a model fit to
        the entire data set (after imputation as needed) with
        appropriate confidence intervals, and a table or (better) plot
        of the effect sizes.
          - Specify the effect sizes for all elements of your final
            model numerically (with both a point estimate and a
            confidence interval), and graphically (with a plot of those
            effects (probably through `plot(summary(yourmodel)`).
          - Then write a detailed and correct description of the effect
            of **at least one** predictor on your outcome for your
            linear regression model, providing all necessary elements of
            such a description, and link this directly to what the plot
            is telling you.
          - We prefer you discuss a statistically and scientifically
            meaningful effect, should one exist. Pick an effect to
            describe that is interesting to you.
      - You should display an appropriate (corrected through validation)
        estimate of R-square for your final model
      - The final part of your summary of the final model should be a
        nomogram with a demonstration of a prediction (and appropriate
        prediction interval) for a new subject of interest.
          - Your prediction (and its prediction interval) should be back
            transformed to the original scale of your outcome, if you
            transformed your outcome before building your model.

### Section 11: Logistic Regression

In Section 11, we expect you to present all relevant code used to
produce your final results. As in Section 10, no output should be
presented in this section without commentary. Also as in Section 10,
this section will describe the fitting and evaluation of two models: a
“main effects” model (model Y), and an “augmented” model (model Z).
We’re primarily interested in a clear presentation. The following 6
elements should be presented, in properly labeled subsections of section
11, using the labels in bold below.

1.  **Missingness** your approach to dealing with missing data, if
    applicable
      - we prefer imputation (simple or multiple) to complete case
        analysis, but it’s not mandatory
      - if you have a sample with no missing data, specify that (again)
        here
      - you can use the same approach as in Section 10, or a different
        one, if you prefer
2.  **Model Y**: your initial “main effects” model
      - remember that your model must include at least four predictors,
        of which at least one must be quantitative and one must be
        multi-categorical.
      - we discourage the use of stepwise or other model selection
        strategies here, instead please use your problem-based
        understanding to select variables and use them all.
      - in presenting your main effects model you should show:
          - a tidied table of regression coefficients
          - key fit summary statistics like the Nagelkerke R-square and
            the area under the ROC curve as they are presented in the
            `lrm` output
          - a confusion matrix based on an explicitly specified
            prediction rule (perhaps `.fitted` \>= 0.5, but something
            else if you prefer) and you’ll need to specify the
            specificity, sensitivity and positive predictive value for
            this model.
          - a nomogram describing the model.
3.  **Non-Linearity** your process for making decisions about how to
    capture potential non-linearity
      - what did the Spearman rho-squared plot suggest and how did you
        spend your degrees of freedom
          - If the (apparently strongest - furthest to the right)
            predictor in the rho-square plot is quantitative, you should
            be thinking first about a restricted cubic spline with 4
            knots, maybe 5,
          - If the largest rho-square is associated with a binary or a
            multi-categorical predictor, create an interaction term with
            the second-largest rho-squared predictor.
          - If you still have degrees of freedom you’re willing to spend
            after this, proceed down to the second largest predictor in
            terms of rho-squared, and proceed similarly to the third
            largest after that.
      - Regardless of your sample size, please use between 3 and 6
        additional degrees of freedom beyond the main effects model to
        account for non-linearity, and add no more than 3 non-linear
        terms to your model.
4.  **Model Z**: fitting your “augmented model” incorporating non-linear
    terms
      - most of you will choose to use `lrm` to do most of this work,
        I’d expect, and that’s fine, but you’ll want to fit the model
        with `glm`, too, to help with building the confusion matrix.
      - you’ll need at a minimum to present a nomogram and plot of the
        effects from `plot(summary(modelname))` for this augmented
        model, using `lrm`.
      - you’ll want to look at an ANOVA comparison of Model Z to Model Y
        in order to understand whether the changes you’ve made led to
        statistically detectable improvements in prediction.
      - again, we’ll want you to produce an appropriate confusion matrix
        using the same prediction rule that you used in Model Y, and
        you’ll need to provide (and compare to Model Y) the
        specificity, sensitivity and PPV for Model Z using that
        prediction rule.
      - you’ll also need to show the Nagelkerke R-square and C statistic
        from the `lrm` output.
5.  **Validating the Models** the results of a validation comparison of
    the Nagelkerke R-square and the C statistic for the “augmented
    model” Z to the “main effects” model Y through the `validate`
    function in `lrm` fits.
6.  **Final Model** This section should end with a clear statement of
    the model you prefer (the “main effects” model Y or the “augmented”
    model Z) based on your overall assessment of fit quality, and
    whether adding the terms in the augmented model yields an
    improvement that is worth the complication of adding the non-linear
    terms.
      - You should land on a single, final model, using both statistical
        and non-statistical considerations to make a decision between
        models Y and Z.
      - An appropriate summary of the final model you landed on should
        start with a listing of the model parameters for a model fit to
        the entire data set (after imputation as needed) in terms of
        odds ratios, with appropriate confidence intervals, and a table
        or (better) plot of the effect sizes.
          - Specify the effect sizes for all elements of your final
            model numerically (with both an odds ratio point estimate
            and a confidence interval), and graphically (with a plot of
            those effects (probably through `plot(summary(yourmodel)`),
            properly interpreted.
          - Then write a detailed and correct description of the effect
            of **at least one** predictor on your outcome for your
            chosen logistic regression model, providing all necessary
            elements of such a description, and link this directly to
            what the plot is telling you.
          - We prefer you discuss a statistically and scientifically
            meaningful effect, should one exist. Pick an effect to
            describe that is interesting to you.
      - Next, we want you to provide a plot of the ROC curve for the
        “final model” in the entire data set.
      - You should display an appropriate (corrected through validation)
        estimate of Nagelkerke R-square and the C statistic for your
        final model, using the entire data set.
      - The final part of your summary of the final model should be a
        nomogram with a demonstration of a predicted probability
        associated with two new subjects of interest that differ in
        terms of some of the parameters in your model.
          - Your predictions in Section 11 should describe two different
            people. You don’t have to call them Harry and Sally, but it
            is helpful to give them actual names.

### Section 12: The Discussion

This should be a short (somewhere in the neighborhood of 200 words)
discussion of your thoughts on the entire Project 1 process. Topics (be
sure to address at least two of these) include:

  - What was substantially harder or easier than you expected, and why?
  - What do you wish you’d known at the start of this process that you
    know now, and why?
  - What was the most confusing part of doing the project, and how did
    you get past it?
  - What was the most useful thing you learned while doing the project,
    and why?

## NEW\! The Poster

You’ll be using the [posterdown
package](https://github.com/brentthorne/posterdown) to build your poster
for Project 1.

  - Learn more about `posterdown` [at its
    repository](https://github.com/brentthorne/posterdown), and with
    this [installation and usage
    guide](https://github.com/brentthorne/posterdown/wiki/Installation-&-Usage-Guide).

The key things to know at this time:

1.  Your audience for the poster includes Dr. Love, the TAs and your
    fellow students. Prepare your poster with that audience in mind.
    What will they need to know to understand what you’ve done, and get
    excited about it?
2.  Dr. Love has prepared a **poster template** for you, using
    `posterdown` and [you can find it
    here](https://github.com/THOMASELOVE/2020-432/tree/master/projects/project1/templates#new-poster-template).
    There is complete R Markdown code, and the resulting [HTML poster
    can be viewed at
    RPubs](https://rpubs.com/TELOVE/poster_template_2020-432).
3.  (Essentially) **every word and every image/table/chart** on your
    poster should come directly from the materials contained in the
    first 12 sections of your portfolio. You will not be developing any
    new material for the poster (just restating things you’ve already
    done) once you have the portfolio. As a result, we encourage you to
    complete the portfolio first.

<!-- end list -->

  - The development of the poster involves selecting useful information
    to present and then arranging it within the poster.
  - Your poster will include no R code (you’ll be using `echo = FALSE`
    to ensure this) but instead will provide nicely formatted figures
    and tables along with text.
  - You’ll have to cut 90-95% of your portfolio, and you should follow
    your instincts regarding your audience (Dr. Love, the TAs and your
    fellow students are your audience) and the template Dr. Love has
    prepared to help think about this.
  - Developing the poster is where **you** have to make decisions about
    what’s most important to show an audience about your work. That’s a
    critically important skill.
