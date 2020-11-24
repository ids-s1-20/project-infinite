Project proposal
================
INFINITE

``` r
library(tidyverse)
library(broom)
```

## 1\. Introduction

The data set “USvideos” comes from the Kaggle website and was collected
by YouTube API, the data set includes several months of data on the
daily trending US YouTube videos. To determine the year’s top-trending
videos, YouTube uses a combination of factors including measuring user
interaction(number of views, comments, and likes).

The general research question is “What is the most popular video on
Youtube, factoring in the number of views, comments, and likes”.

The variables that we will mainly use would be: category\_id - We will
use this variable to determine the most popular video (find the category
in json file, according to the category\_id); views - This variable will
indicate the number of viewers on a video, likes - THis variable will
indicate the number of likes on a video, comment\_count - This variable
will indicate the number of comments on a video, All three of these
variables will help us determine the popularity of each video. these
three variables indicate the popularity of each video, We will also use
title, channel\_title, tags, and description to further examine how
these have an effect on how popular a video might become.

## 2\. Data

``` r
USvideos <- read_csv("../data/USvideos.csv")
```

    ## Warning: Missing column names filled in: 'X16' [16]

    ## 
    ## ── Column specification ────────────────────────────────────────────────────────
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
    ##   X16 = col_logical()
    ## )

    ## Warning: 1 parsing failure.
    ##   row col           expected                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        actual                   file
    ## 10001 X16 1/0/T/F/TRUE/FALSE YARRR feasters! Spongebob Squarepants will always have a special place in our hearts, and this Kelp Shake has an even special-er place in our BELLIES! Learn how to DIY make a recreation of the infamous Kelp Shake as well as a healthy version you can drink and get strong from as well.More SPONGEBOB Recipes:KRABBY PATTY:https://youtu.be/gvCclQ0jUwETRIPLE GOOBERBERRY SUNDAE:https://youtu.be/0rUAuwb9J8MSend us your creations on Instagram, Facebook, and Twitter!http://www.twitter.com/FeastOfFictionhttp://www.instagram.com/FeastOfFictionhttp://www.facebook.com/FeastOfFiction=================Download our Kelp Shake logo here:http://www.mediafire.com/file/683k1ilkffy415x/Kelp%20Shake%20Label.jpgIngredients:3 cups Soy milkHandful spinach1 tsp Kelp extract (ordered) secret ingredient1 cup Pineapple 1 Green apple1 BananaDirections:Blend all ingredients in a blender. Serve in special kelp shake bottle. Well. That was easy.=================Download the Soundtrack:http://jimmywong.bandcamp.com/album/feast-of-fiction-music-from-marbleotTwitter: http://www.twitter.com/FeastOfFictionhttp://www.twitter.com/jfwonghttp://www.twitter.com/ashleyquizFacebook: http://www.facebook.com/FeastOfFictionhttp://www.facebook.com/therealjimmyInstagram:http://www.instagram.com/FeastOfFictionhttp://www.instagram.com/jfwonghttp://www.instagram.com/ashrachelle=================Produced by John-Paul Hoang '../data/USvideos.csv'

``` r
glimpse(USvideos)
```

    ## Rows: 10,001
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
    ## $ X16                    <lgl> NA, NA, NA, NA, NA, NA, NA, NA, NA, NA, NA, NA…

## 3\. Data analysis plan

The outcome variables will be number of views, comments, and likes; and
predictor variables will be category\_id.

We plan to make comparisons on different categories, to research which
category generally is the most popular one.

We are also planning to summarize each video category’s total number of
views. Besides, we we will also calculate the proportion of comments
(comments/views) and the proportion of likes (likes/views). Since we
believe that apart from having many viewers, a popular video should also
receive high proportion of likes as well as comments （the video content
should inspire viewers to discuss).

We plan to use bar plot to visualize the data, as it can directly and
clearly display the comparison between different video types.

Our exploration theme is to find out the most popular type of video,
these statistics analysis should indicate a certain type of youtube
video that generally receives most likes, views, and comments, as the
most popular type.

We expect the video type that has highest likes and comments proportion
is the same type, also it has high number of viewers.

``` r
USvideos %>%
  count(category_id, views, likes, comment_count) %>%
  group_by(category_id) %>%
  mutate(prop_like = likes/views, prop_comment = comment_count/views) %>%
  select(prop_like, prop_comment)
```

    ## Adding missing grouping variables: `category_id`

    ## # A tibble: 10,001 x 3
    ## # Groups:   category_id [17]
    ##    category_id prop_like prop_comment
    ##          <dbl>     <dbl>        <dbl>
    ##  1           1   0.00772     0.00122 
    ##  2           1   0.00769     0.00105 
    ##  3           1   0.00765     0.000956
    ##  4           1   0.00781     0.000901
    ##  5           1   0.00749     0.000864
    ##  6           1   0.00778     0.000834
    ##  7           1   0.0201      0.00926 
    ##  8           1   0.00391     0.000586
    ##  9           1   0.00376     0.000564
    ## 10           1   0.00267     0.000667
    ## # … with 9,991 more rows
