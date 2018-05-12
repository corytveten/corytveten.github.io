---
layout: post
title:      "Puts, Print, and Return Values"
date:       2018-05-12 13:24:20 +0000
permalink:  puts_print_and_return_values
---


Puts vs Print

Both of these commands will display the output of Ruby programming. Print will print out the results of the coding onto a single line. Puts (which is an abbreviation of “output” and “string”) will do the same with the additional step of moving the cursor to the next line down.

Return Values vs Puts and Print

Both Puts and Print will display the output of Ruby programming, but they also produce a return value of “nil.” When puts “Hello World” is entered, the following results:

Hello World
=> nil

Puts and print can be thought of as commands that produce an immediate, superficial result. The results they produce are end points. But methods that produce a return value can be stored and used in later methods and functions. Of course, in Ruby, the print and puts command are actually producing a return value of “nil,” which is important to recognize, but outside of the scope of what I am addressing here.
It is useful to recognize these differences early on when working with Ruby. Puts and print display immediate results while return values provide information that can be stored and continued to be operated upon.

