# 21 Years of Netflix: Data Insights on Global Content Distribution and Demographics

_This project is a part of Bootcamp project competitions derived from the Netflix movies and TV shows dataset sourced from Kaggle [Netflix Dataset](https://www.kaggle.com/code/ridwanadejumo/basic-data-visualization-on-the-netflix-dataset)._
<br>

# 1. Introduction

"Companies rarely die from moving too fast, and they frequently die from moving too slowly." - Reed Hastings Netflix co-founder and then CEO said when the company went all on in streaming service. For a streaming service, Netflix is a data-focused company, using data-informed decision making to improve their service such as Netflix's personalization algorithm can make recommendations to each user. 

But how do they create a good set of content (movies or tv series) to choose from? What data would you like to have if you were designing an asset suite?

In this project, I take two approaches:
- The bottom-up approach, where I let the data naturally surface on distribution, content trends over the years, and genre preferences (Explorative Data Analysis).
- The top-down approach, where I build clusters using the k-means clustering algorithm from prior genre preferences and content watched with Principal Component Analysis (PCA) to handle the curse of dimensionality.

For easy access, here is the links for each analysis:

  Part 1: Explorative Data Analysis on Netflix Global Content Distribution and Demographics

  Part 2: Built content based recommender system to make 10 recommendations
  
<br>

# 2. Structues

The project is seperated into 2 parts:
Part 1: Explorative Data Analysis on Netflix Global Content Distribution and Demographics
Part 2: Built content based recommender system to make 10 recommendations to the user based on the type of show they watched (using Principal Component Analysis (PCA) to handle the curse of dimensionality, and then built clusters using the k-means clustering algorithm).

<br>

# ✨ 2. Explorative Data Analysis 

## 2.1 Report Objectives
<br>

**7770 is the amout of movies and tv series**  Netflix has produced up until 2021. With the extensive library of films and television series, including original productions, Netflix has built a reputation as a content powerhouse, attracting subscribers with its unique offerings. 

Inspired by Netflix, the objectives of this project is to understand the dynamics of Netflix content landscape through the exporative data analysis and advanced visualization leveraging Python programming along with libraries such as NumPy, Pandas, Matplotlib, and Seaborn.

## 3.2 Analysis Techniques
  - 💡 Use MultiLabelBinarizer from sklearn Ml algorithm to tranform `listed_in` into binary variable `genre`.
  - 📈 Calculate correlation coefficient and visualize Netflix's genres in Movie and TV series.
  - 🖥️ Use Netflix's website on rating content, I create `age` column from the original `rating` data.
  - 📊 Communicate the insights with visualization, title, subtitiles and personal analysis with Python programming (Matplotlib, Seaborn liberies) advanced techniques.

<br>

## 3.3 Dataset Introduction

[The Netflix dataset Information](https://github.com/NguyenDangXuanLinh/Netflix-Data-Analysis/blob/main/Dataset_Information.md)


## 3.4 Key Insights



