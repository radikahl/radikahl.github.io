---
layout: post
title: Visualizing my Instagram Activity
excerpt_separator: <!--more-->
permalink: /2016/07/26/vizualizing-my-instagram-acitivty.html
---
I have posted [116 photos and videos](https://www.instagram.com/radikahl/) to Instagram till writing this post. Not tremendously much but still enough to potentially see some interesting patterns or trends in my Instagram usage. I am using Python pandas in a Jupyter notebook with matplotlib to visualise the data. You can get the [code on Github](https://github.com/radikahl/data-visualization/blob/master/Instagram%20Data%20Visualization.ipynb).

I am using the parts of the Instagram API that doesn’t require authentication. I’d have liked to use the endpoints that provide a more rich dataset (e.g. geo coordinates, detailed info about every like etc.). However, Instagram’s new API terms make it difficult - if not impossible - to gain full access to the API endpoints with authentication for projects like this. They require an app review if one wants to pull info for more than 20 posts.

So… let’s see how my Instagram usage has been since I joined the network. That is a bit funny. In May 2012 I posted two photos. Then I stayed quite for 3 years.

![Monthly overview](https://dl.dropboxusercontent.com/u/4255155/blog/instagram/instagram_posts_month.png)

<!--more-->

Looking at the posting activity I can correlate this to times when I was traveling. In particular, road trip and trips to the country side seem to get me excited for sharing the beauty I see. Probably because I am a city boy. For instance, in May 2015 I was on a road trip through Ireland with a couple of friends. In August I spend a long weekend with my girlfriend on the beautiful island Bornholm. The low in February 2016 is probably because I “only” went to Barcelona and Edinburgh for short weekend getaways. 

![Day of week overview](https://dl.dropboxusercontent.com/u/4255155/blog/instagram/instagram_posts_weekday.png)

I am clearly most active on Saturdays. Followed by Sunday and Monday. I think this can be contributed to the many weekend trips I do. What about the time of day?

![time of day overview](https://dl.dropboxusercontent.com/u/4255155/blog/instagram/instagram_posts_hour.png)

Late breakfast, lunch and evening seems to be my preferred times of posting. Let’s see if there is a preference of certain times at different days?

![heatmap](https://dl.dropboxusercontent.com/u/4255155/blog/instagram/instagram_post_heatmap.png)

Easy to recognise the patterns of the previous two charts (e.g. 10 am being the most active time of day). Probably not too surprising that the most of early morning/late night posting happened on a weekend day. But what’s up Mondays? It’s the day I return home from weekend getaways with late flights.

![Hashtags](https://dl.dropboxusercontent.com/u/4255155/blog/instagram/instagram_most_common_hashtags.png)

My favoured hashtags are travel related. Not that anyone would be surprised when reading the paragraphs above ;)
Is the location data providing a similar picture?

![world map](https://dl.dropboxusercontent.com/u/4255155/blog/instagram/instagram_post_geomap.png)

Yes, it is!

![Average Engagement](https://dl.dropboxusercontent.com/u/4255155/blog/instagram/instagram_average_engagement_month.png)

When talking about Instagram how can I not talk about likes?! Looking at the chart I do see a trend that my photos and videos gain on average more and more likes and comments. 


You can visualise your one Instagram activity. [Head to my Github repository](https://github.com/radikahl/data-visualization/blob/master/Instagram%20Data%20Visualization.ipynb) and use the IPython notebook to generate graphs based on your data. You might want to get yourself an API key for Goole Maps to ensure that Google is providing geo coordinates when ever it can. Without proper API key it’s sometimes drops some coordinates.