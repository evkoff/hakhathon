# Hackathon Project
# AI-Powered Movie Recommendation System

## Project Overview

AI-inspired recommendation system is a Python-based application that simulates how modern streaming platforms recommend movies to users based on their preferences and viewing history.

The project demonstrates core concepts of Python programming, Object-Oriented Programming (OOP), data analysis, statistics, and basic recommendation system logic inspired by real-world AI applications.

---

# Problem It Solves

Streaming platforms contain thousands of movies, making it difficult for users to discover content that matches their interests.

This project solves that problem by:

* analyzing user preferences,
* tracking movie ratings,
* identifying similar users,
* and generating personalized movie recommendations.

---

# Main Features

## User Simulation

* Generates fake users using the Faker library
* Stores:

  * user names,
  * ages,
  * preferred genres,
  * watch history,
  * personal movie ratings

---

## Movie Dataset

* Stores movie information including data from IMDB fetched via OMDB API https://www.omdbapi.com/:

  * title,
  * genre,
  * director,
  * year,
  * average rating ('movie rating' - needed for ranking recommendations, popular movies)



---

## Recommendation Engine

The system recommends movies based on:

* favorite genres,
> Since a user likes "Sci-Fi" and "Action" genres, the system will look for movies of these genres, exclude already watched movies and sort the remaining ones by rating
* previously watched movies,
> “Since you liked Interstellar, you may also enjoy Inception.” 
* user ratings (needed for personalized recommendations, Pearson correlation, similarity between users),
> Since a user rate Sci-Fi movies with high ratings and Romance - with low ratings, then the system will increase priority of Sci-Fi movies
* similarity between users (Pearson correlation)
> We compare ratings of different users and make a conclusion about similarity of users based on taste (John and Anna have similar tastes, then if Anna liked Blade Runner and а John hasn't watched it — the system will recommend it to John -> 'users similar to you liked 'Blade Runner')



---

## Statistical Analysis

Uses SciPy statistical methods:

* Pearson correlation to compare user preferences
* K-means clustering to group similar users
Users from the same cluster tend to have similar genre preferences.
The system can use cluster information to recommend movies highly rated by users with similar tastes.

---

## Data Visualization

Visualizes user behavior with:

* pie charts of watched genres,
* line plots of movie ratings over time,
* bar charts of recommended genres,
* cluster distribution charts after K-Means clustering

---

## JSON and File Handling

* Saves generated users and movie data into JSON files
* Loads data from files for future analysis

---

# Technologies Used

* Python
* OOP (Classes and Objects)
* JSON
* Faker
* Requests
* Pandas
* NumPy
* Matplotlib
* Seaborn
* SciPy

---

# How to Run the Project

## 1. Install Required Libraries

Run the following command:

```bash
pip install faker pandas numpy matplotlib seaborn scipy requests
```

---

## 2. Download the Project Files

Clone the repository or download the project folder.

---

## 3. Run the Python Script

Run:

```bash
python main.py
```

or open the notebook in Google Colab/Jupyter Notebook.

---

# Expected Output

The program will:

* generate fake users,
* create movie datasets,
* simulate watch history,
* generate recommendations,
* visualize user insights,
* and save data into JSON files.
