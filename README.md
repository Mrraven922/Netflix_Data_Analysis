# Netflix_Data_Analysis

# 🎯 Project Objective 

This project performs exploratory data analysis and sentiment analysis on Netflix content using Python libraries. It aims to extract key insights about:

Content types and ratings distribution


Most frequent directors and actors


Content trends over time


Viewer sentiment trends (via content descriptions)


# 🧰 Tech Stack
Tool	Purpose

Python	Data analysis and scripting

Pandas	Data manipulation

Plotly	Interactive data visualization

TextBlob	Sentiment analysis

Google Colab	Cloud-based IDE

GitHub CLI (gh)	Pushing to GitHub repo


# 📂 Dataset
📁 Source: Netflix public dataset (netflix_titles.csv)


📊 Size: 14,958 rows × 12 columns


# 📌 Attributes:


title, director, cast, country, release_year


rating, duration, listed_in, description


# 📈 Key Features

🔍 Content Rating Distribution

Created a pie chart of rating frequencies.


Insights:


Majority of content is rated TV-MA and TV-14.


# 🎬 Top 5 Directors

Missing values filled with 'Director not specified'.


Split multiple director entries, grouped and sorted.


Top 5 directors:


Raúl Campos, Jan Suter, Marcus Raboy, Jay Karas, Rajiv Chilaka


# 🎭 Top 5 Actors

Split multi-actor fields, cleaned nulls.


Most featured actors displayed in horizontal bar chart.


# 📅 Yearly Sentiment Trend

Used TextBlob to analyze polarity from description.

Classified as:

🔵 Positive

🔴 Negative

🟡 Neutral

Generated stacked bar chart of yearly sentiment from 2006 onward.

# 📊 Visualizations
🥧 Pie Chart: Distribution of content ratings


📊 Bar Chart: Top 5 actors


📊 Bar Chart: Yearly sentiment distribution


All charts are interactive using Plotly.


# 🧪 Code Highlights

python
Copy
Edit
# Group by and count ratings

df.groupby(['rating']).size().reset_index(name='counts')


# Sentiment analysis on description

testimonial = TextBlob(d)

sentiment = 'Positive' if testimonial.sentiment.polarity > 0 else 'Negative' if testimonial.sentiment.polarity < 0 else 'Neutral'
# 💡 Insights & Learnings

High proportion of Netflix content is rated for mature audiences (TV-MA, TV-14).


A few directors and actors dominate Netflix production.


Sentiment of content descriptions leans positive, indicating engaging/hopeful narratives.


# 🚀 Next Steps / Recommendations

Perform genre-level sentiment breakdown.

Integrate viewer ratings or reviews for deeper sentiment modeling.

Use NLP tools like spaCy or BERT for better sentiment granularity.

Add a time series forecast to predict future content trends.

