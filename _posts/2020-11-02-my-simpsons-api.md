---
layout: post
title:  "My Simpsons API"
date:   2nd November 2020
---

Good news everyone! - Wrong show but it’s Simpsons adjacent so I’m using it.  - My Simpsons API is finally complete. What started out as a bit of a joke idea has turned into a fully working API with multiple endpoints to which you can make GET requests.

First things first, you can access the API here: https://simpsons-api-berbakay.herokuapp.com/api

The ‘/api’ endpoint will give you details on all the available endpoints which are as follows:

GET /api<br>
GET /api/random_episode<br>
GET /api/episodes<br>
GET /api/episodes/:episode_id<br>
GET /api/characters<br>
GET /api/characters/:character_id<br>

The API was built using multiple different technologies including JavaScript, Node, Express, Knex, Heroku and PostreSQL.

What started out as a small side project that I wanted to use to return a random Simpsons episode ended up becoming something much bigger mainly thanks to the amazing data available. All of the data was pulled from this GitHub repo: https://github.com/colinxfleming/simpsons_data

The data includes a list of all the major characters in an episode, the season, episode number, description, Disney+ id and a ‘good’ boolean which you can use to filter just the good episodes. I also like the Disney+ id as this allows a front end developer to include a link to Disney+ which the user can click on to take them directly to the episode. I don’t know if Disney allow embedding on a website but that would at least in theory be possible too.

Once I had all the data in a useable JSON object I migrated and seeded all of the tables myself using Knex and SQL. Once that was done I created all of the endpoints using Express and an MVC model to handle the requests and responses to/from the server. I used TDD to make sure the endpoints and queries all work correctly, I ended up with over 60 different tests for just 6 endpoints. If you receive a 500 error from the server let me know, I’ve been as thorough as I can be but I have a nagging feeling I’ve still missed something.

Once I was happy with my tests I then hosted the files on Heroku which allows anyone to access the api. I can’t wait to see if anyone uses it and more importantly what they do with it.

You can see all of the code for the API at my GitHub here: https://github.com/berbakay/simpsons_data Clone and mess about it with it to your heart’s content!


I have also got a front-end in the works. It will be built using React. You can see the GitHub repo here: https://github.com/berbakay/simpsons-front-end

You can clone the repo and run the site locally using ‘npm start’ in your IDE but as I say it’s a work in progress and I’ll work on it more when I have time.

For now I’ve got more exciting projects on the cards, watch this space...