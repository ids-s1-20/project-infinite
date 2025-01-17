What makes a Youtube video popular?
================
INFINITE

## Summary

This data analysis has been a success and it has been fun researching
something that we use every day. The dataset we used was ‘USvideos’,
gives us analytical information about videos on YouTube such as the
number of likes, views, dislikes, comment\_count. Data varies from 2008
to 2018 with 10000 rows but reduced to half because the large dataset
resulted in errors.

Our research question was “What makes a YouTube video popular. Is it the
most amount of likes, comments, or views? It would be of course the
number of views but videos such as ‘Baby’ by Justin Bieber which has a
total of 11 million dislikes and a like to dislike ratio of 15:11. The
absurd amount of dislikes disqualifies a video from being in the top 10
most popular videos. So to investigate our research question, we came
out with five additional questions, what is the most viewed video, what
category is uploaded most, during what time of day do YouTubers post,
effects of clickbait on views, and a statistical question which asks”How
many likes will a video with 7.8 billion views get?” In addition, we
used the adjusted r squared and the root mean squared error to
complement the statistical question.

To visualize our findings, we first had to combine the duplicate rows.
We viewed the most popular videos using the group\_by function to group
both title and views. Next, we set a time frame to a time interval and
ranked them to determine the time of day with the most uploads. To
discover clickbait, we filtered the top videos with capital letters
using the string package and ranked them by views, likes, and dislikes
to determine if clickbait caused viewers to dislike the video because of
a misleading title. Lastly, we wanted to estimate how many likes a video
would receive it were to reach 2 billion views. We selected the
regression line by comparing the adjusted r squared and the root mean
squared error of two different models.

Our findings were somewhat surprising. We found that 3/5 of the top 5
YouTube videos were music videos, 1/5 was a movie trailer and the last
one was a YouTube Rewind of the most memorable videos on YouTube. Music
videos being the majority was expected as music videos are generally
posted on Youtube, it is evident because the frequencies of common
categories was music which was usually uploaded in the afternoon. Next,
we found the frequency of the different times of day for uploading
YouTube videos and turns out, majority of the uploads occur in the
afternoon. We expected that it would be uploaded during the evening due
to leisure time.

We were particularly interested in clickbait because we wanted to know
if it impacts the view count and if it was worth while for them to
deceive viewers to gain viewers at the cost of dislikes. Our research
shows that by adding capital letters, it attracts more views compared to
a simple title. Nonetheless the clickbait came at a cost, they received
more dislikes compared to the regular videos. The proportions of
dislikes showed that clickbait videos were two times more than all
videos. We could assume that the larger comment count for clickbait
could be a result of the viewers expressing their anger for the
deception. Finally, we finished the data analysis with a least-squares
regression. But before we decided on what line to draw, we tested the
adjusted r squared and the root mean squared error of two models. There
is no evident difference between their accuracies, so we decided to use
the simpler model for prediction. We concluded that the appropriate
equation for the regression line is y = 5212 plus (3/100)x, this implies
that with 0 views a video would receive 4355 likes which doesn’t make
sense. We calculated the r squared to have a value of 0.83 which was
solid enough to make statistical inferences on the data. Therefore, we
applied the regression line to predicted the number of likes for the
most popular video, “Échame La Culpa” would receive if it had 2 billion
views. While the difference in the predicted likes and actual likes in
the video was off by approximately 53 million, we can infer a few
things. People re-watch but they cannot re-like the videos or they don’t
have a Google account which doesn’t allow them to like.

    ## ── Attaching packages ─────────────────────────────────────── tidyverse 1.3.0 ──

    ## ✓ ggplot2 3.3.2     ✓ purrr   0.3.4
    ## ✓ tibble  3.0.4     ✓ dplyr   1.0.2
    ## ✓ tidyr   1.1.2     ✓ stringr 1.4.0
    ## ✓ readr   1.4.0     ✓ forcats 0.5.0

    ## ── Conflicts ────────────────────────────────────────── tidyverse_conflicts() ──
    ## x dplyr::filter() masks stats::filter()
    ## x dplyr::lag()    masks stats::lag()

    ## here() starts at /cloud/project

    ## 
    ## ── Column specification ────────────────────────────────────────────────────────
    ## cols(
    ##   video_id = col_character(),
    ##   trending_date = col_character(),
    ##   title = col_character(),
    ##   channel_title = col_character(),
    ##   category_id = col_double(),
    ##   publish_time = col_time(format = ""),
    ##   views = col_double(),
    ##   likes = col_double(),
    ##   dislikes = col_double(),
    ##   comment_count = col_double(),
    ##   comments_disabled = col_logical(),
    ##   ratings_disabled = col_logical(),
    ##   video_error_or_removed = col_logical()
    ## )

## Presentation

Our presentation slides can be found
[here](presentation/presentation.html). Our pre-recorded video can be
found [here](https://media.ed.ac.uk/media/1+-+INFINITE/1_egvlkmts)

## Data

Mitchell, J 2019, *Trending YouTube Video Statistics*, electronic
dataset, Kaggle, viewed 26 October 2020,
<https://www.kaggle.com/datasnaek/youtube-new?select=CAvideos.csv>.

## References

The link to the data set -
<https://www.kaggle.com/datasnaek/youtube-new?select=CAvideos.csv>
