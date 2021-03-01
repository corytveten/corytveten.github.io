---
layout: post
title:      "Textbook Database App for JS/Rails SPA Project"
date:       2021-03-01 02:52:11 +0000
permalink:  textbook_database_app_for_js_rails_spa_project
---


Description of the Project
I created a textbook database app. In my current position, I research course materials for schools across the country for articulation agreements and transfer credit. Databases of school catalogs are available online, but it is difficult to get specific information about courses beyond the course description. The title alone of a textbook can provide useful evidence of the level and content of a course, and having quick access to this information would be valuable to people working in my field. I imagine the user of this app to be an academic administrator or counselor who would like to keep track of information they have accrued in past research (e.g., textbooks). This app could be expanded to keep records like transferability of courses between two different schools.

The app is structured around three Ruby classes: School, Course, and Textbook. A user can add a new instance of any of these three classes, but only a school can be introduced completely new, without a foreign key. Courses must be attached to a school and textbooks must be attached to a course.

The styling of the app is minimal and not user friendly at the moment, but for the purpose of the parameters of the project, I wanted the DOM manipulation in the app to demonstrate a little sophistication, so I set up a toggle function for the display of courses and textbooks. The user can click on a school name to see that school’s courses that have been added to the database and a form for adding new courses. From there, the user can click on a course title to find the course’s textbooks and a textbook form. Opening and closing elements of the DOM as you are using them also helps with the readability of the page.

Challenges
As stated above, I wanted to show a little sophistication in the app through DOM manipulation and this proved to be my biggest challenge. In order to toggle the course info, I needed to restructure the nodes multiple times. I knew I wanted the parent node to include the school name and a data-id property for the school. I added an event listener to the parent node class that would expand out and show the hidden child nodes with course info. I wanted the user to be able to click anywhere on the entire node to collapse and hide the display, but that would not allow the user to expand the course. So I added a span for the school name that I could attach the event listener to.

There was also some trial and error with setting up the toggle function. Once I placed the “let showCouse = false” flag within the function, everything started falling into place much quicker. 

One other stumbling block: not calling the toggle function upon the creation of new instances of a school or course was causing all of my information to be hidden (the default setting in css), until i refreshed the page. It seems obvious now, as I patched in a new school, the school name was appearing, but I could not toggle the add-course form on and off. I thought the problem was with attaching the course form to the school instance, but of course, the form was there, just hidden. The toggle function needed to be called.

