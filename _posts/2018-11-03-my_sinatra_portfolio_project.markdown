---
layout: post
title:      "My Sinatra Portfolio Project"
date:       2018-11-03 18:03:03 +0000
permalink:  my_sinatra_portfolio_project
---


For my Sinatra Portfolio project, I created a board game database app. This app keeps a database of board game titles, years of publication, and designers. A user must register and sign in to add games to the database.

Using the MVC framework, I created two classes for my models - one for users and one for games. I kept these classes simple, the user class has many games and the games belong to users. The game class inherits name, year, and designer methods from the database through ActiveRecord. I thought about adding a designer class that would have many games and games would belong to designers, but in order to focus on the basics of routing and the controllers, I kept the models as simple as possible.

Moving on to the controllers, I set up an ApplicationContoller class which inherits its methods from Sinatra. From there I created two new controller classes - one to handle signing up and logging in and the other to handle CRUD for games in the database.

Finally, within my views folder, I created a default layout and index page. From there, I created two folders, dividing the views between user and games again. The user view files create web pages to sign up, login, and show an individual users game collection. While the games files create web pages to add new games, edit existing entries, get a list of all games added to the site, and view details on any one game.

