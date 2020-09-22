# Movie Night
## This project was a group final project for 301. After 301 ended, I decided to take this project up a notch by including user authentication and ability for users to search the API for any movie, not just the ones provided on our recommendations list. I also added the ability for users to sort movies based off genre. 

**Original Group:Riva Davidowski, Darius Pasilaban, Krystian Francuz-Harris, Mike Wohl.**

**Contributions after Sept. 4th were done by Riva Davidowski**

### TOOLS USED:
* Node.js
* The Movie Database(TMDb)for access to the API
* Heroku for deploying the final app
* Express
* Bcrypt for user authentication

### GETTING STARTED
* Run npm i to install all dependencies ( I cloned this project down to my repo)
* Set up all packages in server.js
* Create a .env with PORT, DB_URL,and API_KEY (more to come on this one as I use bcrypt)
* Set up all global vars and configs
* Set up the server and tell it to first listen for requests:
```
client.connect()
  .then(() => {
    app.listen(PORT, () => console.log(`listening on ${PORT}`));
  });
  ```
* create test route to make sure server is listening on correct port
* run Nodemon in terminal to start server
* create Schema.sql and create schema for movies using DROP TABLE
* run psql and create database and movies table:
  * CREATE DATABASE _database name_
  * connect to database with \c __database name__
  * #ID SERIAL PRIMARY KEY,
    (enter all data to match movie constructor)
  Run SQL files by conecting them to database psql -d _database name_ -f schema.sql
* create a separate instance of app on Heroku since app was cloned down to repo

# What is Movie Night?

**Problem Domain:** There are too many movies to watch and so many choices across various streaming services. 
#### How do you choose? 

Movie Night makes it easy for a user to pick a movie from a recommendation list based of ratings. The user can choose which movies to watch based of this list and add them to a watchlist.The project used a public API to get movie data and the user can choose which movies to watch based of this list. They can then add movies to the watchlist and delete movies from the watchlist. This involved setting up a server, using various SQL commands, creating GET and POST routes and storing data in a database. This app will save you time and make it easy to choose a movie on any given night.

---

## Wireframes

### Recommendation/Login page

<img src=images/WF1.png>


### Details page

<img src=images/WF2.png>


### Watch List page

<img src=images/WF3.png>


### About Us page

<img src=images/WF4.png>

---

### User Stories

*As a user, I want to be able to create a username to access the Movie Night app.*

Feature Tasks:
User can create a username to access recommended movie list and create personalized watchlist
Username will be featured at top of each page as a reminder that the user is logged in.

Acceptance Tasks:
User’s username will be correctly set as database parameter
Correct username will be displayed at the top of the page
Correct User watchlist is generated once logged in



*As a user, I want to be able to search for movies and get movie details.*

Feature Tasks:
User will be able to scroll horizontally through a list of movies generated by OMDB API
User can click on a movie poster to be taken to a page that displays movie details

Acceptance Tasks:
Once user is logged in, API is used to generate list of movies based on overall rating
User will be able to scroll horizontally through the list of movies
User will be able to click on a movie poster and be directed to a movie detail page. 



*As a user, I want to be able to save movies to my personal watchlist.*

Feature Tasks:
User will be able to click on ‘add to watchlist’ button to add movie to watchlist from the recommended movie list or movie detail page. 

Acceptance Tasks:
Once user clicks on ‘add to watchlist’, correct movie will be added to user’s watchlist.
User’s watchlist persists. 



*As a user, I want to be able to view my watchlist on a separate page.*

Feature Tasks:
User will be able to click ‘My Watchlist’ to see all of their saved movies.

Acceptance Tasks:
Once user clicks ‘My Watchlist’, their saved movies are displayed. 



*As a user, I want to be able to sort/edit my watchlist.*

Feature Tasks:

User will be able to sort saved movies by genre.
User will be able to remove saved movies from watchlist.
Once user adds a movie to watchlist, this movie will appear first in line.

Acceptance Tasks:
Once user sorts by genre, saved movies are sorted by correct genre.
Once user clicks ‘remove from watchlist’ correct movie is removed from the watchlist



---

### Domain Modelling

<img src="images/Domain Modelling.png">

---

### Entity Relationship Diagram 

<img src="images/Entity Relationship Diagram.png">
