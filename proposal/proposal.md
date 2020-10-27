Project proposal
================
INFINITE

``` r
library(tidyverse)
library(broom)
```

## 1\. Introduction

The dataset “USvideos” came from the Kaggle website and was collected by
YouTube API, the dataset includes several months of data on the daily
trending US YouTube videos. To determine the year’s top-trending videos,
YouTube uses a combination of factors including measuring users
interactions(number of views, comments, and likes).

The general research question is “Which factors affect how popular a
YouTube video will be?” We are assuming that the popularity is
determined by the factors of number of views, comments, and likes.

The variables are video\_id, trending\_date, title, channel\_title,
category\_id, publish\_time, tags, views, likes, dislikes,
comment\_count, thumbnail\_link, comment\_disabled, rating\_disabled,
video\_error\_or\_removed, description.

## 2\. Data

``` r
USvideos <- read_csv("../data/USvideos.csv")
```

    ## Parsed with column specification:
    ## cols(
    ##   video_id = col_character(),
    ##   trending_date = col_character(),
    ##   title = col_character(),
    ##   channel_title = col_character(),
    ##   category_id = col_double(),
    ##   publish_time = col_datetime(format = ""),
    ##   tags = col_character(),
    ##   views = col_double(),
    ##   likes = col_double(),
    ##   dislikes = col_double(),
    ##   comment_count = col_double(),
    ##   thumbnail_link = col_character(),
    ##   comments_disabled = col_logical(),
    ##   ratings_disabled = col_logical(),
    ##   video_error_or_removed = col_logical(),
    ##   description = col_character()
    ## )

    ## Warning: 1533544 parsing failures.
    ## row  col           expected actual                   file
    ##   2 tags delimiter or quote      | '../data/USvideos.csv'
    ##   2 tags delimiter or quote      l '../data/USvideos.csv'
    ##   2 tags delimiter or quote      | '../data/USvideos.csv'
    ##   2 tags delimiter or quote      j '../data/USvideos.csv'
    ##   2 tags delimiter or quote      | '../data/USvideos.csv'
    ## ... .... .................. ...... ......................
    ## See problems(...) for more details.

``` r
glimpse(USvideos)
```

    ## Rows: 40,949
    ## Columns: 16
    ## $ video_id               <chr> "2kyS6SvSYSE", "1ZAPwfrtAFY", "5qpjK5DgCt4", "…
    ## $ trending_date          <chr> "17.14.11", "17.14.11", "17.14.11", "17.14.11"…
    ## $ title                  <chr> "WE WANT TO TALK ABOUT OUR MARRIAGE", "The Tru…
    ## $ channel_title          <chr> "CaseyNeistat", "LastWeekTonight", "Rudy Mancu…
    ## $ category_id            <dbl> 22, 24, 23, 24, 24, 28, 24, 28, 1, 25, 17, 24,…
    ## $ publish_time           <dttm> 2017-11-13 17:13:01, 2017-11-13 07:30:00, 201…
    ## $ tags                   <chr> "SHANtell martin", "last week tonight trump pr…
    ## $ views                  <dbl> 748374, 2418783, 3191434, 343168, 2095731, 119…
    ## $ likes                  <dbl> 57527, 97185, 146033, 10172, 132235, 9763, 159…
    ## $ dislikes               <dbl> 2966, 6146, 5339, 666, 1989, 511, 2445, 778, 1…
    ## $ comment_count          <dbl> 15954, 12703, 8181, 2146, 17518, 1434, 1970, 3…
    ## $ thumbnail_link         <chr> "https://i.ytimg.com/vi/2kyS6SvSYSE/default.jp…
    ## $ comments_disabled      <lgl> FALSE, FALSE, FALSE, FALSE, FALSE, FALSE, FALS…
    ## $ ratings_disabled       <lgl> FALSE, FALSE, FALSE, FALSE, FALSE, FALSE, FALS…
    ## $ video_error_or_removed <lgl> FALSE, FALSE, FALSE, FALSE, FALSE, FALSE, FALS…
    ## $ description            <chr> "SHANTELL'S CHANNEL - https://www.youtube.com/…

## 3\. Data analysis plan

The outcome variables will be number of views, comments, and likes; and
predictor variables will be video\_id, category\_id, and publish\_time.

We plan to make comparisons on different categories, to research which
category generally is the most popular one.

We are planning on using a ridge plot or histogram to visualize the data
as this fulfills our plan to use fill.

We are also planning on using basic summary statistics such as median,
minimum value, and maximum value. Using the summary statistics for the
views, likes, and comments, will give us representative numbers of the
average amount for every video category. We need statistical methods to
display which type of videos is the most popular.

Lastly, these statistics analysis should indicate a certain type of
youtube video that generally receives most likes, views, and comments,
as the most popular type.
