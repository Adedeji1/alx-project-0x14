# 🎬 MoviesDatabase API

## API Overview
The MoviesDatabase API provides extensive and frequently updated metadata for over **9 million titles** (movies, series, episodes) and **11 million actors and crew members**. It includes trailers, ratings, biographies, awards, images, budgets, and more. The API is designed for developers building media apps, dashboards, search tools, and entertainment platforms that require detailed film and TV data.

---

## API Version
**Version:** single stable version currently available

---

## Available Endpoints

### **Titles**
- **GET /titles** — Fetch multiple titles with optional filters.  
- **GET /titles/{id}** — Retrieve a single title by IMDb ID.  
- **GET /titles/{id}/ratings** — Get rating and vote count.  
- **GET /x/titles-by-ids** — Return multiple titles by providing a list of IDs.  
- **GET /titles/x/upcoming** — List of upcoming titles.  

### **Series & Episodes**
- **GET /titles/series/{id}** — All episodes in a series (light info).  
- **GET /titles/seasons/{id}** — Number of seasons for a series.  
- **GET /titles/series/{id}/{season}** — Episodes for a specific season.  
- **GET /titles/episode/{id}** — Full information for a single episode.  

### **Search**
- **GET /titles/search/keyword/{keyword}** — Search titles by keyword.  
- **GET /titles/search/title/{title}** — Search by title text (supports `exact=`).  
- **GET /titles/search/akas/{aka}** — Search using alternative titles (AKAs).  

### **Actors**
- **GET /actors** — Fetch actors with pagination.  
- **GET /actors/{id}** — Get full actor details by IMDb ID.  

### **Utils**
- **GET /title/utils/titleType** — List all title types.  
- **GET /title/utils/genres** — List all genres.  
- **GET /title/utils/lists** — List predefined categories like Top 250, Most Popular, etc.

---

## Request and Response Format

### **Request Example**
```http
GET /titles?limit=5&info=mini_info