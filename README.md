
# Rap Soundtracks and Movie Performance

## Overview

As a huge fan of rap music, I’ve always been fascinated by the energy, emotion, and impact it can have on the individual. Rap is such an influential force that in recent years it has made its way into Hollywood. Some of my favorite tracks that I still listen to today came from movies, like Metro Boomin’s *Self Love*, Pop Money's *Another Dimension* or Post Malone’s *Sunflower* from the most recent Spiderman movies. 

Rap is more than just a genre. It’s a movement, and when it collides with the movie industry, something powerful happens. That got me thinking: are movies with rap soundtracks more successful? Do they perform better in theaters? Do audiences rate them higher?

This project explores that intersection — music and film — by analyzing how movies featuring rap soundtracks stack up against those with other genres. From box office numbers to IMDb and MPAA ratings, I set out to uncover trends in this new era of filmmaking.

---

## Data Collection

The dataset was built using a combination of methods:

- **Web Scraping**: Used BeautifulSoup to extract movie titles, gross earnings, release dates, and distributors from BoxOfficeMojo.com.
- **APIs**: Retrieved additional metadata (IMDb rating, MPAA rating, and genre info) using the OMDb and Last.fm APIs.
- **CSV Files**: Integrated supplementary Spotify data for understanding genre popularity.

To keep the analysis meaningful, I focused on high-performing movies — specifically those that grossed over $100 million. The final data frame consisted of 234 movies released in the last 10 years.

---

## Understanding Rap’s Popularity in Music

Before diving into movies, I wanted to validate the influence of rap in the music world. I analyzed a Spotify dataset of 230,000+ tracks across 23 genres, using Spotify’s built-in popularity score (0–100). Rap ranked as the **second most popular genre** overall.

![Top Music Genres by Popularity](plots/music_popularity.png)

---

## Visualizations and Analysis

### Soundtrack Genre Distribution

I started by visualizing which soundtrack genres were most common across all movies.

- **Top 3**: Classical, Electronic, Instrumental - more traditional film scoring genres.
- **Next Group**: Rap, Pop, Rock — more mainstream music genres.

These results were interesting because they show how popular music genres like rap are breaking into the traditional film score space.

![Soundtrack Genre Distribution](plots/soundtrack_genres.png)

---

### Box Office Averages by Soundtrack Genre

I compared average box office earnings for the top six most common soundtrack genres. Instrumental came out on top at just over $300 million, with rap close behind at around $240 million.

![Box Office Averages](plots/gross_earnings_by_genre.png)

---

### IMDb Ratings by Soundtrack Genre

Next, I looked at average IMDb ratings. Instrumental was again at the top. Rap, however, ranked sixth, with an average score of 6.7. 

![IMDb Ratings by Genre](plots/imdb_rating_by_genre.png)
---

### Regression: Gross Earnings vs IMDb Rating

Despite its lower average IMDb score, rap soundtrack movies show a **positive correlation** between rating and revenue — suggesting that higher-rated rap films tend to perform especially well.

![Revenue vs IMDb Regression](plots/gross_earnings_imdb_ratings_correl.png)

---

### MPAA Ratings Comparison

I compared MPAA ratings for rap and non-rap soundtrack films:

- **Rap Soundtracks**: PG, PG-13, R, then G.
- **Non-Rap Soundtracks**: PG-13, PG, R, then G.

It was surprising to see PG as the most common rating for movies with rap soundtracks; rap usually has a reputation for explicit content.

![MPAA Ratings Comparison](plots/mpaa_ratings.png)

---

### Monthly Release Patterns

I analyzed the number of movie releases by month:

- **Rap Soundtrack Films**: Feburary and summer months.
- **Non-Rap Films**: December and summer months.

This trend indicates that summer is a peak season for both rap and non-rap soundtrack films, while the February spike in rap soundtrack releases may be connected to Black History Month.

![Release Month Distribution](plots/rap_non_rap_seasons.png)

---

### Live Action vs Animated

Movies with rap soundtracks were more likely to be live action (12) than animated (10).

![Live Action vs Animated](plots/animated_vs_live_action.png)

---

### Most Common Movie Genres (for Rap Soundtracks)

The top movie genres among rap soundtrack films were:

1. Action
2. Adventure
3. Comedy

![Movie Genre Breakdown](plots/primary_movie_genre.png)

---

### Trends Over Time

I visualized trends in the six most common soundtrack genres over the last 10 years. Most genres, including rap, saw a decline around 2016–2021, followed by a recent uptick.

![Soundtrack Trends Over Time](plots/genre_year.png)

---

### Which Studios Release Rap Soundtrack Films?

Universal Pictures led the way in releasing rap soundtrack films, accounting for 40% of such releases, followed by Disney at 25% and Sony at 20%. Universal particularly seems to have embraced rap soundtracks as a deliberate strategy.

![Studio Distribution](plots/distributors.png)

---

## Reflection and Next Steps

This project confirmed many of my hunches but also revealed some surprises. I learned:

- Rap is a powerful soundtrack genre linked to strong box office performance.
- Ratings-wise, rap films may underperform, but high-rated ones earn significantly more.
- Release patterns suggest strategic seasonal timing (e.g., summer, Black History Month).
- Universal Pictures has taken the lead amoung common distributors, investing heavily in this trend.

### If I Had More Time...

- Expand the dataset to include movies earning under $100 million.
- Extend the range beyond 10 years for longer-term trend analysis.
- Improve soundtrack genre classification with a more robust API or scraping method.
- Incorporate production budgets, marketing data, or audience soundtrack reviews for deeper insights.

---

## Project Repository Structure

```
project-root/
│
├── data/
│   ├── final_movie_dataset.csv
│   ├── movie_dataset.csv
│   └── spotify_features.csv
│
├── plots/
│   ├── animated_vs_live_action.png
│   ├── distributors.png
│   ├── genre_year.png
│   ├── gross_earnings_by_genre.png
│   ├── gross_earnings_imdb_ratings.png
│   ├── imdb_rating_by_genre.png
│   ├── mpaa_ratings.png
│   ├── music_popularity.png
│   ├── primary_movie_genre.png
│   ├── rap_non_rap_seasons.png
|   └── soundtrack_genres.png
│
├── notebooks/
│   ├── data_collection_cleaning.ipynb
│   └── data_visualizations.ipynb
│
└── README.md
```

---

## Final Thoughts

This was one of the most rewarding and challenging projects I’ve taken on. As both a data analyst and a music fan, digging into this crossover between rap and film has been incredibly satisfying. There's still more to explore, but I hope this analysis helps spotlight the growing cultural and commercial influence of rap in the world of cinema. This is my first major data analysis project, and I hope to take what I've learned and apply it to future projects.
