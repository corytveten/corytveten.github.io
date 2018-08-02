---
layout: post
title:      "CLI Data Gem Project"
date:       2018-08-02 18:14:52 +0000
permalink:  cli_data_gem_project
---


Beginning the CLI Data Gem project with a blank screen was intimidating. But once I watched Avi's walk through video a couple times, i was ready to begin:
[CLI Gem Walkthrough](https://www.youtube.com/watch?v=_lDExWIhYKI)

In my previous lessons, I was short cutting past the psudo-code steps and simply pushing my way through the labs with a trial and error method. Now, all programmers go through the trial and error process, but I think I was too focused on the the back and forth of the TDD and not on why I was doing what I was doing, as part of a bigger picture.

One of the new lessons I learned in this project came from Avi's discussion of his thought process while he was creating a new gem. Previously, i was using the TDD process to find a problem, fix a problem, find a problem, fix a problem. This got me through the labs but since the structure was dictated by the TDD, i did not have a sense of the openness of creating a new program. Avi's narration directly addressed the challenges of building a program from scratch. His initial approach as a programmer is to imagine the user of his program. Where would this person being their interaction with the program? This is where Avi suggests we bein our programming.

From here on, the walkthrough stubs out a structure and hard codes some elemets of the program to get a sense of how we would like it to work. This is where i began to appreciate pseudocode and not simply correcting an error message provided by the TDD program. Simply creating a menu full of hard coded information that would be replaced by scraped data later allowed me to build the structure of my program. Then later, as I encountered error after error with my scraping, I knew that the problems were localized to my scraping methods.

Challenges of scraping:
I used the website boardgamegeek.com to scrape data for my CLI Data Gem. It turns out this website is not especially user friendly for a beginner like me. And, being a beginner, I assumed the fault was completely on my end. 

Initally, I wanted to scrape from [this page](https://boardgamegeek.com/browse/boardgame) and then, to access details about each of  the games, i would scrape from each individual game's page. After some difficultly, I was able to create a new method that took the URL intantiated with each new class of game get details like a description the designer, etc. Unfortunately, the scraping on these details pages proved to be too much. I went over the scraping process with my team lead to get a sense of what was going wrong, and mercifully, he let me know that I was in over my head. He re-directed me to the inital page, which was still full of information to scrape and I was still able to create a gem with an inital menu that led to futher details about each game.
