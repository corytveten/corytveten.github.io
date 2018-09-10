---
layout: post
title:      "Re-Loading a Lab "
date:       2018-09-10 13:59:30 +0000
permalink:  re-loading_a_lab
---



Visiting a lab again has been helpful with knocking some of the cobwebs off when I haven't engaged with a subject in a while. It's also helpful to come back to earlier subjects once I have developed a broader perspective on how Ruby works and improved my programmatic thinking in general.

Early on, I was uncomofortabel with GitHub and forking/cloning labs, so I was reliant on the Learn IDE button. Once a lab had been completed, I thought I was unable to 'reset' the lab and use the tests to run through the lesson again. This blog post will help any beginners who have relied on the "Open IDE" button and want to know how to re-open a lab through GitHub.

First open the Learn IDE application. This will bring you to the temporary folder. 

Next, go to the GitHub site and search for the lab by title (e.g. ruby-object-initialize-lab). The first search result should be the Learn.co students account. Click on that result.

On the right side of the screen you will find a large green button that reads "Clone or download."  Click this button and you will get a dropdown that gives you the option to clone with SSH or HTTPS. Click the SSH option. Then copy the SSH key.

Back to the terminal in your IDE application. On the command line type  "git clone" followed by the coped SSH key. Remember to use cmd+shift+v on mac, or ctrl+shift+v on pc to paste. For example:
git clone git@github.com:learn-co-students/ruby-object-initialize-lab-v-000.git

From here, type "cd" followed by the name of the lab:
cd ruby-object-initialize-lab-v-000

Next, type "bundle install".

Now, type "learn". You will see that you are no longer passing your tests and you can run through the lab again.



