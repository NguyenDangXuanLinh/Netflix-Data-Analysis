
# Netflix Content Development from 2000 to 2020

_This project is a part of Bootcamp project competitions derived from the Netflix movies and TV shows dataset sourced from Kaggle [Netflix Dataset](https://www.kaggle.com/code/ridwanadejumo/basic-data-visualization-on-the-netflix-dataset)._
<br>
# Netflix's Value Propositions
 - Content Diversity: distribution of movies, TV shows, genres, directors.
 - Temporal Trends: trends over time in content offerings, release years, and production patterns.
 - Audience Insights: viewer preferences, engagement metrics, and user ratings
 - Geographical Patterns: regional variations in content preferences

# Summary of Insights
## Content Diversity
 - From the 2014 to 2018, Netflix's content is increased significantly with the higest spike at 2017 and 2018. This spike then decreased and slowed in 2019 and 2020.
 - Business then have completely dropped in 2021 - investigate whether there is an issue with production, temporary drop related to Covid or a new competitor for this market.
<img width="100%" align="middle" 
    src="images/year_dist_black.png">
<img width="50%" align="middle" 
    src="images/dis_ratios.png">   
<img width="100%" align="middle" 
    src="images/rating_line.png">
## Audience Insights
- The analysis reveals that TV shows with a "TV-MA" rating are the most common on Netflix, followed by "TV-14" rated shows in second place. 
```ruby
data = df.groupby('first_country')[['count']].sum().sort_values(by='count',ascending=False).reset_index()
```
<img width="100%" align="middle" 
    src="images/rating_plot1.png">   
<img width="100%" align="middle" 
    src="images/ages_countries.png">    
```ruby
mlb = MultiLabelBinarizer()
res = pd.DataFrame(mlb.fit_transform(test), columns=mlb.classes_, index=test.index)
corr = res.corr()
```
<img width="100%" align="middle" 
    src="images/tv_heatmap.png">
<img width="100%" align="middle" 
    src="images/movie_heatmap.png">
## Temporal Trends
```ruby
data_sub = df.groupby('type')['month_name_added'].value_counts().unstack().fillna(0).loc[['TV Show','Movie']].cumsum(axis=0).T
```
<img width="100%" align="middle" 
    src="images/month_trend.png">
## Geographical Patterns
```ruby
data_q2q3 = df[['type', 'first_country']].groupby('first_country')['type'].value_counts().unstack().loc[country_order]
data_q2q3['sum'] = data_q2q3.sum(axis=1)
data_q2q3_ratio = (data_q2q3.T / data_q2q3['sum']).T[['Movie', 'TV Show']].sort_values(by='Movie',ascending=False)[::-1]
```
<img width="100%" align="middle" 
    src="images/top10_country.png">   
<img width="100%" align="middle" 
    src="images/dis_ratios_country.png">
# Recommendations & Next Steps
 - Investigate why Production plans exhibit a steep dip in 2021 and expand this analysis to include more years to examine whether this trend is Covid-related or consistent across time. Is there a content preference we can combat this dip?
   
 - The distribution of content genres based on the country of origin, with certain genres being more prevalent in specific regions.Therefore, expand analysis on the country-specific content preferences with localization efforts, and audience targeting ensure the diverse preferences of regional preferences.
   
 - Suggest investigate Temporal Trends for specific country and compare with standalone USA Temporal Trends analysis to discover similarities and differences. Is there any differences in content offerings, release years, and production patterns of the targeted country compared with USA Temporal Trends

# Analysis Techniques
  - 💡 Use MultiLabelBinarizer from sklearn Ml algorithm to tranform `listed_in` into binary variable `genre`.
  - 📈 Calculate correlation coefficient and visualize Netflix's genres in Movie and TV series.
  - 📊 Communicate the insights with visualization, title, subtitiles and personal analysis with Python programming (Matplotlib, Seaborn liberies) advanced techniques.

## 2.3 Dataset Introduction
[The Netflix dataset Information](https://github.com/NguyenDangXuanLinh/Netflix-Data-Analysis/blob/main/Dataset_Information.md)
