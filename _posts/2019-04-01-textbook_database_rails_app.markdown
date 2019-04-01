---
layout: post
title:      "Textbook Database Rails App"
date:       2019-04-01 10:23:46 +0000
permalink:  textbook_database_rails_app
---


For my Ruby on Rails portfolio project, I created an application that allows users to access information about course listings and textbooks at secondary learning institutions. The imagined audience of the site is a curriculum researcher. Basic information like course descriptions and credit hours are usually available on the web, but course materials like textbooks and other information from the syllabus is harder to come by. This application would allow university administrators and faculty to lookup and add information about the specific textbooks attached to a course.

The models for the program include User, Textbook, School, and Course. Users will need to create an account to both add and access the information, as I am imagining this not as a public site, but something used by one education system. So my User model does not have associations as it might if i were building a site for students to enter info about a course they attended. Instead, the associations are located among School, Course, and Textbook. With the school having many courses and the course and textbooks both having many through, since a course will have multiple texts and a textbook may be used in multiple courses. I have also added a comments attribute that will allow the user to make a comment on the use of a textbook within a course (e.g., “Required Text”).

Working through this project, i found myself relying on the require params.inspect command for debugging. I often would encounter issued with instantiating new objects of a class through the forms that I had created. Inserting the require params.inspect command into the code allowed me to recognize whether the form was providing the required information to the controller to create the object. I could quickly discover that my object was not instantiating because I was missing a course id. Raise Params directed me to problems quickly and allowed me to debug in a focused, informed way.
