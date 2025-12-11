# Comparative Analysis of Audience Sentiment for Two Films with Different Box Office Performances
## 1.Introduction
### 1.1 Background
The film industry often presents stark contrasts in audience reception and commercial
success, a divergence vividly illustrated by the box office performance of the animated sequel
Inside Out 2 (2024) and the live-action adaptation Snow White (2025).  

Inside Out 2, released on June 14, 2024, became an undisputed blockbuster. Its tremendous
success was founded upon a powerful combination of factors, such as exploring Riley's
developmental stage of puberty and the exciting integration of new emotions alongside the
beloved original cast. This enthusiasm fueled a historic theatrical run, resulting in a domestic
box office gross of approximately $652.98 million.  

In stark contrast, Snow White (2025) experienced a substantially different outcome.
Following its pre-release trailer and subsequent release, the film encountered a significant
wave of negative public discourse and sustained controversy. This backlash, which centered
on elements of character interpretation, narrative changes, and perceived production quality,
likely contributed to its poor commercial showing. The film concluded its domestic theatrical
run after 77 days with a gross revenue of approximately $87.20 million.  
<img width="1090" height="626" alt="box office" src="https://github.com/user-attachments/assets/dc121f74-4d03-40da-96f0-7819213d7010" />


In view of these two disparate box office performances, the precise difference in audience
reaction and its correlation with commercial performances warrants close examination
### 1.2 Question of Interest
(1) What were the temporal trends in daily audience sentiment and comment volume for
each film?  
(2) What correlations exist between audience sentiment, comment volume and
subsequent daily box office revenue for each film?  
(3) What were the dominant emotional polarities and thematic subjects of audience
discourse for Inside Out 2 and Snow White (2025)?

## 2.Methodology
### 2.1 Data Source
Focusing on two films, Inside Out 2 (2024) and Snow White (2025), we collected daily box
office data from Box Office Mojo using web-scraping techniques. And obtained audience
comments from the YouTube data API, sourced specifically from the discussion threads
under each film’s official trailer.
### 2.2 Research Subject
<img width="957" height="378" alt="subject" src="https://github.com/user-attachments/assets/0411de57-7ff2-40dc-8c98-2c95e5f92a48" />

### 2.3 Analysis Technique
(1) Sentiment Analysis  
After cleaning the raw comments data, a natural language processing (VADER) model was
applied to assign a numerical sentiment score to each comment, ranging from -1.0 to +1.0.
The daily average sentiment was calculated by averaging the scores of all comments posted
each day. Alongside the comment volume, use time-series plot to track audience emotional
trends over time.  

(2) Correlation Analysis  
Separately define daily comment volume and daily average sentiment score as the predictors,
next-day box office revenue was defined as outcome. Pearson correlation coefficient was
used to qualify the relationship between variables, and a scatter plot with regression line was
used for visualization.  

(3) Word Frequency and Topic Modelling  
For word frequency, the cleaned tokens were tallied to determine the frequency of each
unique word. The top 30 most frequent words were then visualized using two horizontal bar
charts. For topic modeling, Latent Dirichlet Allocation (LDA) was used to identify
underlying topics within the text corpus by grouping words that frequently co-occur.
