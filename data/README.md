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

  This data analysis has been a success and it has been fun to research something that we use every day. The dataset we used was 'USvideos', which gives us in-depth information about videos on Youtube such as the number of likes, views, dislikes, comment_count. The data was collected from as early as 2008 to 2018 with 10000 rows but we had cut the data frame into half because the large dataset resulted in errors loading the dataset onto R. 
  
  Our research question was "What makes a Youtube video popular?" We wanted to understand what exactly makes a Youtube video popular, is it the most amount of likes, comments, or views? You may say it would be of course the number of views but popular videos such as 'Baby' by Justin Bieber which has a total of 11 million dislikes and a like to dislike ratio of 15:11. The absurd amount of dislikes disqualifies a video from being in the top 10 most popular videos. So to investigate our research question, we came out with three additional questions, what is the most viewed video, during what time of day do Youtubers post, effects of clickbait on views, and lastly a statistical question which asks "How many likes will a video with 7.8 billion views get?"

  To visualize our findings, we first had to combine the duplicate rows so we get a total value for each duplicate. Afterwards, we went ahead and visualized the most popular Youtube videos by views. We used the group_by function to group both title and views to help us visualize the videos by descending order. Next, we wanted to figure out is there any benefit to posting at certain times of the day. We first set a certain time frame to a time of day and ranked them by descending order to view the the time which had the most amounts of posts. We then wanted to get a better understanding of clickbait in Youtube videos. To get a better understanding, we filtered the top videos with an exclamation mark or question mark and using the string package. We then selected views, likes, dislikes, and comment_count because we wanted to see if clickbait would cause viewers to dislike the video because of misleading titles. Lastly, we wanted to estimate how many likes a video would receive it were to reach 1 trillion views. We did so by finding the least-squares regression learned in week 8. After finding the equation, we also checked the R^2 score to check if the regression is an appropriate fit for our data. 

  Our findings were somewhat surprising. We found that 3/5 of the top 5 Youtube videos were music videos, 1 of them was a trailer to the movie "The Avengers" and the last one was a Youtube Rewind of the most memorable videos on Youtube. Next, we found the most frequent time for uploading Youtube videos and they were during the afternoon it was surprising because that was when people were working. We thought that it would be posted during the evening becasue that was when people had leisure time to browse Youtube. And it was no suprise that the least popular time was during the morning because that is people are sleeping or communiting to work or school. The idea of clickbait was one of particular interest to us because we wanted to know if it impacts the view count and if it was worth it for them to deceive viewers to gain extra viewers at the cost of dislikes. Our research shows that simply adding suspense titles will attract more likes compared to just writing the title with capital letters and question and exclamation marks. The suspenseful titles came at a cost nonetheless, they received more dislikes compared to the titles without any cliffhangers. And we could also imply that the larger comment count for the suspenseful titles could be a result of the viewers trying to express their complaints against the deception. If the Youtuber was posting for revenue, we would advise them to refrain from using such titles because it results in lost subscribers and lower views in the future. An appropriate title that accurately reflects the videos will be more beneficial revenue-wise in the long term. Finally, we finished the data analysis with a least-squares regression and finding the R^2. We concluded the equation of the regression line to be y = 4355 + (3/100)x, this implies that with 0 views a video would receive 4355 likes but this is somewhat common because Youtube sometimes has glitches within their system that causes such numbers to appear. We calculated the R^2 to have a value of 0.8 which was a solid number and that was enough to make statistical inferences on the data. Therefore, we applied the regression line to predicted the number of likes for the most popular video of 2017. "Échame La Culpa" would receive if it were to reach 2 billion views. While the difference in the predicted likes and actual likes in the video was off by approximately 53 million, we can infer a few things. Some people rewatch the video plenty of times which doesn't let them relike the video and they also may be unable to create a google account which disables the ability for them to like the video. We also used the regression line to predict the number of likes a video would receive if the whole human population watched one specific video. We approximated that it would receive 233 million likes, but we may never know how many likes that video would get because of government censorship and lack of wifi in some places of the world. 
  
  
  This was an interesting and fun project to research with our knowledge gained throughout this course. Not only did we learn more about how certain aspects affect Youtube, we got to know different people. 

