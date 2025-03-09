# 🎬 Flask Movie Ranking App
This project is a Flask-based Movie Ranking Application that allows users to:<br>
✅ Add movies to their favorite movie list 🎥<br>
✅ Rate and review each movie ⭐<br>
✅ Edit and delete movie entries 📝❌<br>
✅ Fetch movie details from TMDb API 📡<br>
✅ Store data in a SQLite database 💾

## Features
✅ 1. Add Movie<br>
- Users can add a movie by entering its title.
- The app will fetch the movie details (image, description, release date) from The Movie Database (TMDb API).
- Users can select the movie from a list of options fetched from TMDb API.

✅ 2. Rate and Review Movie<br>
- After adding the movie, users can rate it (out of 10) and leave a review.
- Movies are ranked based on their rating (highest to lowest).

✅ 3. Edit Movie Details<br>
- Users can update the rating and review of a movie.
- The app uses Flask-WTF Forms for form validation.

✅ 4. Delete Movie<br>
- Users can delete a movie from the list with a single click.

✅ 5. Dynamic Movie Ranking<br>
- Every time a new movie is added or reviewed, the ranking is updated dynamically based on the movie rating.

## 💻 Tech Stack
| Technology   | Purpose   |
|------------|------------|
| Flask | Python web framework for building the web app |
| Flask-WTF | Handles forms and form validation |
| SQLAlchemy | ORM (Object Relational Mapping) for database interactions |
| Bootstrap-Flask | Provides Bootstrap styling for clean UI |
| TMDb API | Fetches movie data (title, description, image, release date) |
| SQLite | Lightweight database for storing movie details |

## 📂 Project Structure
```
/flask_movie_ranking
│── /static
│   ├── css
│   │   ├── styles.css       # Custom CSS Styling
│── /templates
│   ├── base.html            # Base Template for all pages
│   ├── index.html           # Home Page (All Movies)
│   ├── add.html             # Add a new movie
│   ├── edit.html            # Edit Movie Rating and Review
│   ├── select.html          # Select Movie from API Response
│── movies.db                # SQLite Database
│── main.py                  # Flask App
│── requirements.txt         # List of Dependencies
```

## 💾 Database (movies.db)
The application uses a SQLite database to store movie information.<br>
### Table: Movie
| Column   | Type   | Description |
|------------|------------|------------|
| id | Integer (Primary) | Unique ID for each movie |
| title | String (250) | Movie title |
| year | Integer | Release year |
| description | String (500) | Movie description |
| rating | Float | User-given rating (out of 10) |
| ranking | Integer | Movie rank based on rating |
| review | String (250) | User review |
| img_url | String (250) | Poster image URL |

## 🔗 API Integration (TMDb API)
The app uses The Movie Database (TMDb) API to fetch movie details.<br>
✅ API Endpoints:<br>
- Search Movie: https://api.themoviedb.org/3/search/movie
- Get Movie Details: https://api.themoviedb.org/3/movie/{id}
You can obtain your own API key from TMDb API.



