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

**18 points**: (20 possible points) User interface is intuitive and the instructor can easily use it on their own without guidance. Styling is consistent and call-to-action elements are obvious. The application provides the user with relevant feedback based on interactions.

* Love the design and how you took this in a different direction than the wireframes, nice and simple and clean.

* The boxes with simple explainers on how to use things are great - simple and to-the-point but helpful for the user. What would be SUPER cool is to have these boxes show up as little 'tooltips' on different parts of the application that show you where the save/delete/refresh buttons are. Then you could click out of the tooltips after reading them and clear up some space on the UI for users that already know their way around the app. This would require storing something in localstorage that says "has the user x'ed out of all these helpful tooltips already? if so, don't show them again"

* Would like the cursor to change to the little 'hand' icon when you hover over the lock icons to indicate that I can actually click on them. (Same thing for the palette thumbnails that show up under their respective projects after being saved)

## Testing

**17 points**: (20 possible points) Project has a running test suite that tests most server-side endpoints but is missing/skipping a test or two.

* Would be good to assert against an [error message here too](https://github.com/ameseee/palette-picker/blob/master/test/routes.spec.js#L158), not just the status code

* It block text [here](https://github.com/ameseee/palette-picker/blob/master/test/routes.spec.js#L167) doesn't match up with what you're actually trying to assert in this test. Not sure at a quick glance why this would fail in CI and not locally, but happy to debug in-person with you if you'd like.

* These look [like](https://github.com/ameseee/palette-picker/blob/master/test/routes.spec.js#L193-L203) identical [tests](https://github.com/ameseee/palette-picker/blob/master/test/routes.spec.js#L151-L162) asserting against adding a project to the database. One of these should be trying to add a palette to the database.

## Commented Server File

**10 points**: (10 possible points) Each line of the server file (on a separate branch) is commented and explains the code using precise, correct terminology and specificity

## JavaScript Style

**23 points**: (30 possible points) Application is thoughtfully put together with some duplication and no major bugs. Developer can speak to choices made in the code and knows what every line of code is doing.

* Is this [conditional](https://github.com/ameseee/palette-picker/blob/master/server.js#L44-L48) necessary? If there is no length to the array, wouldn't it return an empty array anyway?

* Server-side code is beautiful, I'm rarely in the scenario where I can't find things to bitch about. Good job.

* [Fetch requests](https://github.com/ameseee/palette-picker/blob/master/public/js/scripts.js#L3) aren't dependent on the DOM, and therefore don't need to be in `document.ready()` kick off that request ASAP!

* You don't want to be [appending to the DOM](https://github.com/ameseee/palette-picker/blob/master/public/js/scripts.js#L31) on each iteration of a for loop. DOM manipulations are expensive. Instead, you'd want to use Document Fragments to build up all the HTML you want to append, and then add it to the DOM all at once at the end of the loop.

* [This](https://github.com/ameseee/palette-picker/blob/master/public/js/scripts.js#L76-L106) is a little unruly. It's still clean and readable, but maybe you do write a loop to dynamically generate those palette-color divs? Instead of having all that repeat code.

* [postPayload](https://github.com/ameseee/palette-picker/blob/master/public/js/scripts.js#L110) is a really generic, uninformative name for a function. Instead of using the verb POST, you want to use something that's a little more semantic, like save or create. This is also a little misleading because you're not actually POSTing anything in this function, you're just creating the configuration for doing the post. I do like that you're reusing the function for palettes and projects though. 

* You want to make sure you're not removing something from the DOM before it's actually deleted from the [database](https://github.com/ameseee/palette-picker/blob/master/public/js/scripts.js#L186-L195). If anything went wrong with that delete request you would have removed an element that actually still existed in your dataset. Do the DOM removal in the `.then()` of the delete request.

* Could you not just add `unique` to the project name column in your database schema to avoid having to do this whole [check](https://github.com/ameseee/palette-picker/blob/master/public/js/scripts.js#L212-L226)?

## Workflow

**18 points**: (20 possible points)

* You don't have to file PRs on a project when you're working by yourself. You should still be using branches, but PRs are for code review.

* Nice, consistent and informative git commit messages 

* Glad you did cleanup and linting fixes in their own commits, but there's a lot of them. Try using a git hook to prevent this in the future ;)


### To get a 3 on this project, you need to score 110 points or higher
### To get a 4 on this project, you need to score 130 points or higher

# Final Score: 136 / 150



### Answers to Your Questions

What is convention for organizing the server.js file - all the gets together, then posts together, etc. or organized by endpoint? Or is this just a preference/team consistency thing? -- **Will go over in class**

I'm sure you're planning to include in the feedback, but I'm wondering if I made the right choices for my endpoints? I originally had several more that I starting realizing I didn't need. Looking back I think I maybe should have done a 'POST' directly to /palettes rather than /projects/:id/palettes, but honestly am not 100% sure.  -- **You'll see both of these URL structures in the real world, but I prefer `/projects/:id/palettes` because it more clearly demonstrates that there is a one-to-many reltionship between the two tables. It also means the user doesn't have to pass through a project ID along with the palette data.**

I have an error on line 43 (TypeError: Cannot read property 'project_name' of undefined). When I append a new project, my theory is that is takes a second because of async, so project is undefined. Somehow it still 'works' though. I feel like I need to understand how I can get the error and console.log to see that project is undefined, but it still 'works'. -- **Can't quite tell, it looks fine at first glance but I'm happy to debug this in person together**