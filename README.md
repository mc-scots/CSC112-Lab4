# Designing Big Things

## Introduction
Back in the more innocent days of Lab 2, you helped write a very
complex shapes program.  Each of you had a fork of the lab, from which
you added one shape.  I then took on the simple task of merging your
pull requests together.  In the end, what was produced was very good,
and very lengthy!  It is well over 2000 lines long!

So then, how do we cope with something of that size and complexity?
We need some way to design all the ins and outs of the system, and
that is what this lab is about.  You are going to retroactively design
the full program in Lab2, and then you are going to make modifications
to that design.  This will be followed by an extra credit opportunity
in which you can implement your changes to improve your grade on
program 1.

## Step One: Merge Upstream Changes into Lab 2
We will begin this journey in your lab2 folder.  Go ahead and go
there, and then visit https://help.github.com/articles/syncing-a-fork/
to learn how to sync your fork with the upstream changes.  Once you
have a working program that can draw all the shapes, go ahead and
commit and push all changes brought in by this merge.

## Step Two: Diagram What is There
For this step, you will need a UML editor.  Just like a text editor,
UML modeler preference is highly personal.  I would recommend you try
several.  Note that this work will need to be done either on your own
computer (if you need to install anything), or on the lab computers.
Our server does not have a web based UML modeler installed.  Some
suggestions of good/easy to use modelers are:

* Umbrello
* Argo UML
* UML Pad

If you do a google search for these terms, you should find them quite
easily.  They are all open source, and they are all relatively simple
to use.  Learning how to use your tool is your responsibility!  We're
only going to do use case and class diagrams, so it shouldn't be that
hard to get it working.  Just fiddle with it for a few minutes and
you'll learn where everything is.

Now that you have a UML tool, go ahead and draw a use case diagram for
the shapes program.  Next, model all the classes in a class diagram.
You shouldn't have to look at any files other than the header files to
do this!

## Step Three: Changes
Imagine that you've just shown your boss the shapes program.  They
love it!  Unfortunately, the users are finding it difficult to use.
In fact, they all wish it had a few more features.  After a lot of
back and forth, they have come up with the following list of changes
to make to the program.

1. Display a menu at the bottom listing the shapes and their letters.
Something like this:

     (P)oint  (L)ine  (R)ectangle  (Q)uadrangle  (T)riangle (H)exagon
     (C)ircle (S)ierpinski
     
2. Have the ability to select colors for the shapes.  The color
selections should be the 7 terminal colors.  Use the number keys to
set the colors. (0 for normal 1-7 according to the terminal color
codes). Each shape should retain its color.  For instance, I should be
able to make a red rectangle, a blue circle, and a green rectangle in
the same canvas.

3. Have the cursor change colors to show what the current drawing
color is.

4. Display a status line at the top of the screen while entering
points for a shape.  For instance, if we are drawing a rectangle, this
line should say:
     Rectangle:  1/2 points
The count will update with each new point.  Once the shape is
complete, it will disappear.

5. Preview the shapes as they are being entered.  For instance, if I
am drawing a line, after the first point, draw a line from the
starting point to where the cursor currently is at.  As the cursor
moves, the line is cleared and redrawn to the new position.  This
preview will mean different things in different shapes, but the bottom
line is we should see as much of the shape as we can with each cursor
movement.


Now, some of those changes are rather simple.  Some of them will not
affect the design in the slightest.  Others, however, will have far
reaching effects on the object design.  If you were to launch into the
code and try to make these things happen, you would quite likely make
a real mess of things!  Instead, what we want to do is modify the
shapes system design so that it can accommodate these behaviors.

Remembering everything you have ever learned about OOP (provided you
payed attention during lecture, that is), figure out which of the
feature changes require design modification.  Modify the design in
your UML diagrams.  Be sure to add additional use cases as needed, but
most of this is going to take place on the class diagram.

Once you have modified the classes to meet the new demands, put your
UML diagrams in your Lab4 folder, add it to git, and commit and push
your changes.  Don't worry about exporting them to images, I have all
the UML tools known to man on my laptop.  If you find one I don't know
about, however, I may have to get you to send me a link to it.  

Here endeth Lab 4.


## Extra Credit: Implementing the Changes
Ok, so some of you did not do so well on Program 1.  Some of you are
overachievers for whom a grade of 100 is not enough.  Rarer, is that
you could be someone who realizes that trying to work with other
people's code would be edifying. If you fall into any of these
categories, now's your chance to improve your score! 

Implement the 5 changes outlined above.  Be sure to follow your design
from the lab.  Don't do your work in the lab2 folder!  Remember those
are public repositories and other students could steal your work for
their gain! Copy all the code (Makefile, *.cpp, and *.h) files from
lab2 into your lab4 folder and add them all to the git repository. Do
your work in the lab4 folder.

Each of the 5 changes are worth different numbers of points.  I won't
tell you what they are because that would give away which are easy and
which are hard.  The bottom line is, the more you do, the more points
get added to program 1.  If you complete all 5, you will get an
additional 100 points.