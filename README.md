# Neo4j-Movie-Recommendation
# 🎬 Neo4j Movie Recommendation Graph

This project is a graph-based movie recommendation system using **Neo4j** and a subset of the [MovieLens 100K Dataset](https://grouplens.org/datasets/movielens/100k/). It demonstrates how user-movie-genre relationships can be modeled and queried using a graph database.

---

## Project Overview

The graph database simulates a simplified movie recommendation engine by capturing interactions between:

- **Users** (with attributes like age, gender, and occupation)
- **Movies** (with metadata such as title and release year)
- **Genres** (such as Comedy, Drama, Romance, etc.)

The system allows you to:
- Analyze user behavior
- Identify top-rated movies by genre
- Recommend films based on common user preferences
- Practice Cypher query writing and graph analysis

---

## Graph Schema

### **Node Types**
| Label  | Properties |
|--------|------------|
| `User` | `user_id`, `age`, `gender`, `occupation` |
| `Movie` | `movie_id`, `title`, `year` |
| `Genre` | `name` |

### **Relationship Types**
| Relationship | From → To | Properties |
|--------------|-----------|------------|
| `[:RATED]` | `User` → `Movie` | `rating`, `timestamp` |
| `[:BELONGS_TO]` | `Movie` → `Genre` | _(no properties)_ |

---

## Dataset

The dataset is sourced from the [MovieLens 100K dataset](https://grouplens.org/datasets/movielens/100k/), provided by GroupLens Research.  
We used a **subset of**:
- 50 users
- 30–50 movies
- Genre flags from the metadata
- 1000+ ratings



