What is the most popular video on Youtube, factoring in the number of views, comments, and likes
================
INFINITE

## Summary

Write-up of your project and findings go here. Think of this as the text
of your presentation. The length should be roughly 5 minutes when read
out loud. Although pacing varies, a 5-minute speech is roughly 750
words. To use the word count addin, select the text you want to count
the words of (probably this is the Summary section of this document, go
to Addins, and select the `Word count` addin). This addin counts words
using two different algorithms, but the results should be similar and as
long as you’re in the ballpark of 750 words, you’re good\! The addin
will ignore code chunks and only count the words in prose.

You can also load your data here and present any analysis results /
plots, but I strongly urge you to keep that to a minimum (maybe only the
most important graphic, if you have one you can choose). And make sure
to hide your code with `echo = FALSE` unless the point you are trying to
make is about the code itself. Your results with proper output and
graphics go in your presentation, this space is for a brief summary of
your project.

    ## ── Attaching packages ────────────────────────────────── tidyverse 1.3.0 ──
    ## ✓ ggplot2 3.3.2     ✓ purrr   0.3.4
    ## ✓ tibble  3.0.4     ✓ dplyr   1.0.2
    ## ✓ tidyr   1.1.2     ✓ stringr 1.4.0
    ## ✓ readr   1.4.0     ✓ forcats 0.5.0
    ## ── Conflicts ───────────────────────────────────── tidyverse_conflicts() ──
    ## x dplyr::filter() masks stats::filter()
    ## x dplyr::lag()    masks stats::lag()
    ## here() starts at /cloud/project
 
    ## ── Column specification ───────────────────────────────────────────────────
    ## cols(
    ##  video_id = col_character(),
    ##  trending_date = col_character(),
    ##  title = col_character(),
    ##  channel_title = col_character(),
    ##  category_id = col_double(),
    ##  publish_time = col_datetime(format = ""),
    ##  tags = col_character(),
    ##  views = col_double(),
    ##  likes = col_double(),
    ##  dislikes = col_double(),
    ##  comment_count = col_double(),
    ##  thumbnail_link = col_character(),
    ##  comments_disabled = col_logical(),
    ##  ratings_disabled = col_logical(),
    ##  video_error_or_removed = col_logical()
    ## )

## Presentation

Our presentation can be found [here](presentation/presentation.html).

## Data

Include a citation for your data here. See
<https://github.com/ids-s1-20/project-infinite.git> for guidance
on proper citation for datasets. If you got your data off the web, make
sure to note the retrieval date.

## References

List any references here. You should, at a minimum, list your data
source.
