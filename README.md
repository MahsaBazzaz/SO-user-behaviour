# SO-user-behaviour
In this project:
1. I obtained the StackOverflow questions and answers for a given tag within a given time period
2. I extracted for each post 5 key metrics
3. I generated a CSV file with one line per post, where each line contains an identifier for a post and the values for the 5 chosen metrics
4. I generated plots to understand the differences in the distribution of the 5 metrics between the posts of the two tags

# Metrics
I extracted 5 key metrics for each question:
- If the question has an accepted answer, a metric to determine how likely it is that someone will get the correct answer to the question. 
- the score of the question: the number of upvotes - the number of downvotes, a metric to examine the quality of the post.
- the question comments count: a metric to examine how active are the posts of the tag
- the answer count: a measure of how diverse the answers are to the tag's questions.
- owner reputation: a metric to examine the level of expertise of the users asking questions about the tag

# Assumptions and Limitations
- Since users can get banned from StackOverflow if they do intensive post retrieval, I was only able to retrieve a small number of posts. Clearly, this amount of data isn't an accurate representation of users' behavior.
 Due to the time limit, I did not implement any crawlers to fetch StackOverflow posts and instead, I used the stack exchange API (https://api.stackexchange.com/docs) to fetch the posts. Because of this, I was limited to the methods available there.

# Analyses 

## plot no.1
I compared the number of questions with accepted answers to questions without accepted answers in this plot. In the plots, it can be seen that questions with WordPress tags are more likely to be answered correctly than those with Drupal tags.

## plot no.2
Using this plot, I compared the scores of the posts of the two tags. The plot shows that the WordPress tagged questions have a much higher score than the Drupal tagged questions.

## plot no.3
I plotted the reputations of users who asked questions in those tags. Users are rewarded with reputation points when they post helpful questions and answers, so it can serve as a gauge for determining how expert they are. As can be seen from the plots, the reputations of users are pretty similar between tags.

## plot no.4
I compared the average number of answers to each tag on this plot. This metric is used to determine how diverse the answers to a question are within each tag. According to the plot, WordPress questions have significantly different answers than Drupal questions.

## plot no.5
For this plot, I compared the average number of comments of each post in order to examine the activity of the posts associated with the tag. Drupal questions receive more comments on average than WordPress questions.

# Conclusions
- The analysis shows that although Drupal questions have more comments, they have fewer accepted answers than WordPress questions. Perhaps the reason is that the questions asked are not appropriate (plot 2), which is probably due to Drupal's level of complexity.
- The user reputations appeared to be the same in these plots, but I think this may be due to the small size of the dataset, so I think we should analyze this again with a larger sample size.
WordPress questions have higher veracity of possible answers. I am not familiar with either WordPress or Drupal, but I believe the nature of the problems in each technology is responsible for this difference.
