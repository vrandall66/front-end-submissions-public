# Palette Picker Submission Form

[Project Spec](http://frontend.turing.io/projects/palette-picker.html)

# Basics

#### Link to the GitHub Repository for the Project
[palette-picker](https://github.com/ameseee/palette-picker)

#### Link to the Deployed Application
[heroku](https://holt-palette-picker.herokuapp.com/)

#### Link to your annotated server file
[annotated server file](https://github.com/ameseee/palette-picker/blob/annotate-server/server.js)

## Completion

#### Were you able to complete the base functionality?

Yes!

#### Which extensions, if any, did you complete?

None:( not yet.

# Code Quality

#### Link to a specific block of your code on GitHub that you are proud of
[happy code](https://github.com/ameseee/palette-picker/blob/master/public/js/scripts.js#L107-L115)

* Why were you proud of this piece of code?
I liked pulling out the payload body here to keep the fetch function cleaner. 

#### Link to a specific block of your code on GitHub that you feel not great about
[sad code](https://github.com/ameseee/palette-picker/blob/master/public/js/scripts.js#L70-L105)

* Why do you feel not awesome about the code? What challenges did you face trying to write/refactor it?
I feel less than awesome because this is repeating the same thing five times in a row. I refactored other things before tacking this because of the palette_color_# challenge. I still want to refactor it!

#### Attach a screenshot or paste the output from your terminal of the result of your test-suite running.

[test suite]![image](https://user-images.githubusercontent.com/25447342/33492541-8b2a51d2-d67a-11e7-9b8c-e9c885d41453.png)

#### Link to Design Inspiration

[Inspiration](https://dribbble.com/shots/3002953-Famous-Industry-pages)
I liked how much the colors on this popped, and I wanted my Palette Picker to allow the colors the user chose to really stand out and not drown in any of MY design.

#### Please feel free to ask any other questions or make any other statements below!

What is convention for organizing the server.js file - all the gets together, then posts together, etc. or organized by endpoint? Or is this just a preference/team consistency thing?

I'm sure you're planning to include in the feedback, but I'm wondering if I made the right choices for my endpoints? I originally had several more that I starting realizing I didn't need. Looking back I think I maybe should have done a 'POST' directly to /palettes rather than /projects/:id/palettes, but honestly am not 100% sure. 

I have an error on line 43 (TypeError: Cannot read property 'project_name' of undefined). When I append a new project, my theory is that is takes a second because of async, so project is undefined. Somehow it still 'works' though. I feel like I need to understand how I can get the error and console.log to see that project is undefined, but it still 'works'.

-----

# Instructor Feedback (Brittany)

## Specification Adherence

**50 points**: (50 possible points) No approach was taken that is counter to the spirit of the project and its learning goals. There are no features missing from above that make the application feel incomplete or hard to use. Data persists on refresh using a knex/postgreSQL database.

## User Interface

**x points**: (20 possible points)

* Love the design and how you took this in a different direction than the wireframes, nice and simple and clean.

* The boxes with simple explainers on how to use things are great - simple and to-the-point but helpful for the user. What would be SUPER cool is to have these boxes show up as little 'tooltips' on different parts of the application that show you where the save/delete/refresh buttons are. Then you could click out of the tooltips after reading them and clear up some space on the UI for users that already know their way around the app. This would require storing something in localstorage that says "has the user x'ed out of all these helpful tooltips already? if so, don't show them again"

* Would like the cursor to change to the little 'hand' icon when you hover over the lock icons to indicate that I can actually click on them. (Same thing for the palette thumbnails that show up under their respective projects after being saved)

## Testing

**x points**: (20 possible points)

## Commented Server File

**x points**: (10 possible points)

## JavaScript Style

**x points**: (30 possible points)

## Workflow

**x points**: (20 possible points)


### To get a 3 on this project, you need to score 110 points or higher
### To get a 4 on this project, you need to score 130 points or higher

# Final Score: x / 150



### Answers to Your Questions

