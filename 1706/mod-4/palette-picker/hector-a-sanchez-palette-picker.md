# Palette Picker Submission Form

Basics

Link to the GitHub Repository for the Project

https://github.com/hsanchez7934/hs-palette-picker

Link to the Deployed Application

https://hs-palette-picker-12-1-17.herokuapp.com/

Link to your annotated server file

https://github.com/hsanchez7934/hs-palette-picker/tree/hs-annotated

Completion

Were you able to complete the base functionality?

Yes.

Which extensions, if any, did you complete?
none

Code Quality

Link to a specific block of your code on GitHub that you are proud of
https://github.com/hsanchez7934/hs-palette-picker/blob/master/public/js/index.js

Why were you proud of this piece of code?

Honestly, I'm kind of proud of everything that I wrote here, I know there can be
some refactoring, but after not having written jquery for a few months now, I feel proud
of the functionality I was able to implement with jquery.

happy code

Link to a specific block of your code on GitHub that you feel not great about
https://github.com/hsanchez7934/hs-palette-picker/blob/master/public/js/index.js

Why do you feel not awesome about the code? What challenges did you face trying to write/refactor it?

On line 164, function onSavePaletteClick, this function handles a lot of logic and is very long.
I know that with some refactoring I can clean it up and make it easier to read.
sad code

Attach a screenshot or paste the output from your terminal of the result of your test-suite running.
test suite
Palette Picker is running on 3000.
  Client Routes

    ✓ should return the homepage with text (54ms)
    ✓ should return 404 error for nonexistent route
 
 API Routes
Seeding test complete!
    ✓ should fetch projects
Seeding test complete!
    ✓ should fetch color palette from targeted project
Seeding test complete!
    ✓ should be able to post project to database (50ms)
Seeding test complete!
    ✓ should return 422 is project is missing name
 Seeding test complete!
    ✓ should post palette to project
Seeding test complete!
    ✓ should return 422 if missing a required property
Seeding test complete!
    ✓ should destroy palette
Seeding test complete!
    ✓ should destroy project if project
      has no associated palettes
Seeding test complete!
    ✓ should not destroy project
      if it has associated palettes
11 passing (775ms)

Link to Design Inspiration

Show us what you used as design inspiration (another color picker site, a dribbble UI element, a user flow, etc.) and explain what you stole from it

I really like the design of the wireframe that was including in the palette picker spec, I spent a lot of time reviewing the lessons
on express and knex and I know I didn't devote too much time to UI research.  My UI is modeled after the wireframe that
is included in the palette picker, I felt that it was really easy to read and I really like it. 

Please feel free to ask any other questions or make any other statements below!
Anything else you wanna say!

# Instructor Feedback (Robbie)

## Specification Adherence

**50 points:** (50 possible points)

* Everything looks good to match the spec.

## User Interface

**15 points:** (20 possible points)

* Good use of space for the color palette
* The form for making new palettes and projects in a bit confusing (if I didn't write the project, I might not know what to do first for saving a palette and project)

## Testing

**13 points:** (20 possible points)

* Great happy path tests
* The indentation [here](https://github.com/hsanchez7934/hs-palette-picker/blob/master/test/routes.spec.js#L62) and in other places in this file is a bit unconventional when it comes to JS style guides. Would normally see the `.send` and `.then` on separate lines.
* [Here](https://github.com/hsanchez7934/hs-palette-picker/blob/master/test/routes.spec.js#L88) and other tests, you're forgetting to return the promise, which is probaly why you need to use `done()`
* Should test for the error response [here](https://github.com/hsanchez7934/hs-palette-picker/blob/master/test/routes.spec.js#L107) too, not just the status code
* For [this case](https://github.com/hsanchez7934/hs-palette-picker/blob/master/test/routes.spec.js#L167), the server should response with a more helpful message - something to tell the user that they can't delete the project for a specific reason

## Commented Server File

**7 points:** (10 possible points)

* Good comment coverage in the file. For some lines, like [this](https://github.com/hsanchez7934/hs-palette-picker/blob/hs-annotated/server.js#L3) need more specificity (why are we including body-parser/what is it used for?). We're mainly looking for the _purpose_ you want to write each line of code.

## JavaScript Style

**20 points:** (30 possible points)

* Nice job [adding a migration](https://github.com/hsanchez7934/hs-palette-picker/tree/master/db/migrations) instead of just editing your initial migration
* Make sure you remove [this library](https://github.com/hsanchez7934/hs-palette-picker/blob/master/server.js#L6) if you're not using it
* [This functionality](https://github.com/hsanchez7934/hs-palette-picker/blob/master/server.js#L50-L61) for checking params is used elsewhere - see if you can extract this to a separate function or piece of middleware
* You shouldn't need an explicit return [here](https://github.com/hsanchez7934/hs-palette-picker/blob/master/server.js#L41) and other places. You usually only need the explicit `return` if you are within an if/else conditional 
* I don't see the purpose of [this Project class](https://github.com/hsanchez7934/hs-palette-picker/blob/master/public/js/index.js#L24-L26). When you create a new instance of the project, you are holding the name from the input in the new instance, but you can just use a variable in this case.
* What is the purpose of [this `return`](https://github.com/hsanchez7934/hs-palette-picker/blob/master/public/js/index.js#L58)?
* One thing to note with using `fetch` is that it will not error on 404 - in order to hit the `.catch` on a 404, you can check for `response.ok` [demonstrated in the MDN docs here](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API/Using_Fetch#Checking_that_the_fetch_was_successful)

## Workflow

**12 points:** (20 possible points)

* Be sure to add `.gitignore` early on in your project and include `.DS_Store` files
* Would expect smaller, more atomic commits

### To get a 3 on this project, you need to score 110 points or higher

### To get a 4 on this project, you need to score 130 points or higher

# Final Score: 117 / 150
