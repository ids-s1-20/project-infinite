# data

Data Dimensions:
4998 observations
13 variables

## USvideos

- `video_id`: Unique ID of each video
- `trending_date`: date of the video that it was listed on 'Youtube Trending List'
- `title`: Titles of videos
- `channel_title`: Titles of channels
- `category_id`: Category of video
- `publish_time`: Time that videos are published by authors in US timezone
- `views`: number of views 
- `likes`: How many viewers like this video
- `dislikes`: How many viewers dislike this video
- `comment_count`: How many comments this video receive
- `comments_disabled`: videos that authors do not allow viewers to leave comment
- `ratings_disabled`: videos that authors do not allow viewrs to rate
- `video_error_or_removed`: videos that have error happened or are removed

# Write-up

This data analysis has been a success and it has been fun to research about something that we use everyday. The dataset we used was 'USvideos', it gives us indepth information about videos on Youtube such as number of likes, views, dislikes, comment_count. The data was collected from as early as 2008 to 2018 with 10000 rows but we had cut the data frame into half because the large dataset resulted in errors loading the dataset onto R. Our research question was "What makes a Youtube video popular?" We wanted to understand what exactly makes a Youtube video popular, is it the most amount of likes, comments or views? You may say it would be ofcourse the number of views but popular videos such as 'Baby' by Justin Bieber which has a total of 11 million dislikes and a like to dislike ratio of 15:11. The absurd amount of dislikes disqualifies a video being in the top 10 most popular videos. So to investigate our research question, we came out with three additional questions, what is the most viewed video, during what time of day do Youtubers post, effects of clickbait on views and lastly a statistical questin which asks "How many likes will a video with 1 trillion views get?"

