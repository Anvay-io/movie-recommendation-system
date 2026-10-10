# 🎬 CineMatch — Movie Recommendation System

<p align="center">
  **Discover your next favorite movie with Machine Learning.**
  
  A content-based movie recommendation engine that helps you discover films similar to the ones you love.
</p>

<p align="center">
  🚀 **Live Demo:** (https://1movie-recommendation-system.streamlit.app/)
 <br>
   💻 **GitHub:** https://github.com/Anvay-io/movie-recommendation-system
</p>

---

## 🍿 About CineMatch

Ever spent more time choosing a movie than actually watching one?

**CineMatch** makes movie discovery smarter by using machine learning to analyze movie metadata and recommend films with similar characteristics.

Using content-based filtering, the system compares information such as genres, keywords, cast, and descriptions to generate relevant recommendations.

Whether you're looking for something similar to your favorite thriller or searching for your next sci-fi adventure, CineMatch helps narrow down your choices.

## ✨ Features

- 🎯 **Smart Recommendations** — Discover movies similar to your selected title.
- 🧠 **Machine Learning Engine** — Uses text vectorization and cosine similarity.
- 🎭 **Metadata-Based Matching** — Analyzes genres, keywords, cast, and overviews.
- 🎬 **TMDB API Integration** — Retrieves movie information from The Movie Database.
- ⚡ **FastAPI Backend** — Serves recommendation functionality through API endpoints.
- 📊 **Similarity-Based Ranking** — Ranks movies according to their metadata similarity.
- 🔐 **Secure Configuration** — Supports environment variables for API credentials.

## ⚙️ How It Works

1. **Data Collection:** Load movie metadata and retrieve relevant information through TMDB API integration.
2. **Data Preprocessing:** Clean and prepare movie descriptions, genres, cast, and keywords.
3. **Feature Engineering:** Combine selected metadata into a unified text feature.
4. **Text Vectorization:** Convert text into numerical vectors using `CountVectorizer`.
5. **Similarity Calculation:** Apply cosine similarity to compare movie representations.
6. **Recommendation Generation:** Return movies with the highest similarity to the selected title.
7. **API Delivery:** Make recommendation functionality accessible through FastAPI.

## 🏗️ System Architecture

```text
       Movie Dataset + TMDB API
                  |
                  v
          Data Preprocessing
                  |
                  v
           Feature Engineering
                  |
                  v
             CountVectorizer
                  |
                  v
          Cosine Similarity
                  |
                  v
        Recommendation Engine
                  |
                  v
                FastAPI
                  |
                  v
          User / Frontend Client
```

## 🧠 Machine Learning Approach

| Component | Technique |
|---|---|
| Recommendation type | Content-Based Filtering |
| Feature extraction | Text preprocessing and feature engineering |
| Vectorization | CountVectorizer |
| Similarity metric | Cosine Similarity |
| Backend framework | FastAPI |
| Movie metadata | TMDB API and dataset |

### Cosine Similarity

CineMatch compares numerical representations of movie metadata using cosine similarity.

\[
\operatorname{Similarity}(A,B)=
\frac{A\cdot B}{\|A\|\|B\|}
\]

A higher similarity score indicates a closer match between the selected movie and a candidate movie based on the features used.

### Why Content-Based Filtering?

- Doesn't require user ratings or viewing history.
- Recommends movies based on their content.
- Helps users discover similar films.
- Provides a straightforward and interpretable recommendation process.

## 🛠️ Tech Stack

- **Python** — Core programming language
- **Pandas & NumPy** — Data processing and numerical operations
- **Scikit-learn** — Machine learning utilities
- **CountVectorizer** — Text feature extraction
- **Cosine Similarity** — Movie similarity computation
- **FastAPI** — REST API development
- **Uvicorn** — ASGI server
- **TMDB API** — Movie information
- **python-dotenv** — Environment configuration

## 🚀 Getting Started

### Prerequisites

- Python 3.10 or newer recommended
- pip
- TMDB API key, if required by your implementation

### 1. Clone the repository

```bash
git clone YOUR_GITHUB_REPOSITORY_URL
cd movie-recommendation-system
```

### 2. Create and activate a virtual environment

**Windows**

```bash
python -m venv .venv
.venv\Scripts\activate
```

**macOS / Linux**

```bash
python3 -m venv .venv
source .venv/bin/activate
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Configure environment variables

Create a `.env` file and add the credentials required by your application.

```env
TMDB_API_KEY=your_tmdb_api_key
```

Use the variable names expected by your code, and never commit private credentials to GitHub.

### 5. Run the application

If your FastAPI instance is named `app` in `main.py`, run:

```bash
python -m uvicorn main:app --reload
```

Access the API documentation at:

`http://127.0.0.1:8000/docs`

## 🔐 Security & Reliability

- Keep API keys and credentials in environment variables.
- Exclude `.env` from version control.
- Validate incoming API requests.
- Handle unavailable movies and API failures gracefully.
- Protect sensitive operations and avoid exposing internal errors.
- Verify deployed services and database connectivity where applicable.

## 🔮 Future Enhancements

- 🖼️ Movie posters, trailers, and ratings
- 🌐 Interactive movie discovery interface
- 🎭 Genre, language, and year filters
- ❤️ Watchlists and personalized preferences
- 🤝 Hybrid recommendations using collaborative filtering
- ⚡ Optimized similarity search for larger datasets
- ☁️ Improved deployment monitoring and automated testing

## 🎯 What This Project Demonstrates

- Practical application of machine learning
- Text preprocessing and feature engineering
- Content-based recommendation algorithms
- Vectorization and similarity computation
- REST API development with FastAPI
- Third-party API integration
- Application deployment and environment configuration

## 📄 Data & Attribution

Movie information may be sourced through TMDB integration. Follow TMDB's applicable API terms, attribution requirements, and branding guidelines. This project is not endorsed or certified by TMDB.

---

<p align="center">
  **🎬 Don't just watch movies. Discover your next favorite.**
</p>
