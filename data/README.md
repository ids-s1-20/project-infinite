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

This data analysis has been a success and it has been fun to research about something that we use everyday. The dataset we used was 'USvideos', it gives us indepth information about videos on Youtube such as number of likes, views, dislikes, comment_count. The data was collected from as early as 2008 to 2018 with 10000 rows but we had cut the data frame into half because the large dataset resulted in errors loading the dataset onto R. 

Our research question was "What makes a Youtube video popular?" We wanted to understand what exactly makes a Youtube video popular, is it the most amount of likes, comments or views? You may say it would be ofcourse the number of views but popular videos such as 'Baby' by Justin Bieber which has a total of 11 million dislikes and a like to dislike ratio of 15:11. The absurd amount of dislikes disqualifies a video being in the top 10 most popular videos. So to investigate our research question, we came out with three additional questions, what is the most viewed video, during what time of day do Youtubers post, effects of clickbait on views and lastly a statistical questin which asks "How many likes will a video with 1 trillion views get?"

To visualize our findings, we first had to combine the duplicate rows together so we get a total value for each duplicate. Afterwards, we went ahead and visualized the most popular Youtube videos by views. We used the group_by function to group together both title and views to help us visualize the videos by descending order. Next, we wanted to figure out is there any benefit to posting at certain times of day. We first set a certain time frame to a time of day and {INSERT INFO ABOUT THE FINDINGS}. We then wanted to get a better understanding on clickbait in Yotube videos. To get a better understanding, we filtered the top videos with an exclamation mark or question mark and using the string package. We then selected views, likes, dislikes and comment_count because we wanted to see if clickbait would cause viewers to dislike the video because of misleading titles. Lastly, we wanted to estimate how many likes a video would receive it were to reach 1 trillion views. We did so by finding the least squares regression learned in week 8. After finding the equation, we also checked the R^2 score to check if the regression is an appropirate fit for our data. 

Our findings were somewhat suprising. We found that 3/5 of the top 5 Youtube videos were music videos, 1 of them was a trailer to the movie "The Avengers"" and the last one was a Youtube Rewind of the most memorable videos on Youtube. Next, we found the most frequent time for uploading Youtube videos and they were during the {INSERT TIME} it was suprising because that was when people {EITHER WAS WORKING OR AT HOME}. The idea of clickbait was one of particular interest to us because we wanted to know if it really impacts the view count and if it was worth it for them to deceive viewers to gain extra viewers at the cost of dislikes. Our research shows that by simply putting a question or exclamation mark in the title, they were determined to receive more views but at the same time, they received more dislikes compared to a title without clickbait.  

