# Palette Picker Submission Form

[Project Spec](http://frontend.turing.io/projects/palette-picker.html)

# Basics

#### Link to the GitHub Repository for the Project
[palette-picker](https://github.com/NikBorn/mod4-Palette-Picker)

#### Link to the Deployed Application
[heroku](https://nikb-palette-picker.herokuapp.com/)

#### Link to your annotated server file
[annotated server file]()
have not filled this out yet!
## Completion

#### Were you able to complete the base functionality?
Yes!


#### Which extensions, if any, did you complete?
none
# Code Quality

#### Link to a specific block of your code on GitHub that you are proud of
[happy code](https://github.com/NikBorn/mod4-Palette-Picker/blob/master/public/js/scripts.js#L113-L120)

Only because I struggled with it for so long for some reason and felt great after getting it to work correctly!

#### Link to a specific block of your code on GitHub that you feel not great about
[sad code](https://github.com/NikBorn/mod4-Palette-Picker/blob/master/public/js/scripts.js#L171-L182)

There is obviously some repittion here, I need to refactor this!

#### Attach a screenshot or paste the output from your terminal of the result of your test-suite running.

```
  Client Routes
    ✓ should return the homepage with text (53ms)
    ✓ should return a 404 for a route that does not exist

  API Routes
    GET /api/v1/projects
Test Seeding Complete!
      ✓ should return all of the projects
Test Seeding Complete!
      ✓ should return a 404 if the path is incorrect
    GET /api/v1/projects/:id/palettes
Test Seeding Complete!
      ✓ should return all palettes for a specific project
Test Seeding Complete!
      ✓ should return a 404 if the path is incorrect
    POST /api/v1/projects
Test Seeding Complete!
      ✓ should be able to add a project to the db
Test Seeding Complete!
      ✓ should not add the project to database if info is missing
    POST /api/v1/projects/:id/palettes
Test Seeding Complete!
      ✓ should be able to add a palette to the database
Test Seeding Complete!
      ✓ should not add a palette to database if it is missing information
    DELETE /api/v1/palettes/:id
Test Seeding Complete!
      ✓ should be able to delete a certain palette
Test Seeding Complete!
      ✓ should return 422 if palette does not exist


  12 passing (440ms)
```

#### Link to Design Inspiration
[inspiration](http://paletton.com/#uid=1000u0kllllaFw0g0qFqFg0w0aF)
* I liked the way everything was very dark EXCEPT for the colors, I felt like with an app like this your eye should only be drawn to the colors.


#### Please feel free to ask any other questions or make any other statements below!

I really learned quite a bit with this project, but I dont' think it will be ready for grading until tomorrow sometime :(

-----


# Instructor Feedback (Brittany)

## Specification Adherence

**50 points**: (50 possible points) No approach was taken that is counter to the spirit of the project and its learning goals. There are no features missing from above that make the application feel incomplete or hard to use. Data persists on refresh using a knex/postgreSQL database.

## User Interface

**13 points**: (20 possible points) User interface is mostly intuitive, though the instructor might need some guidance on interactions. Styling is mostly consistent, but could use some clean up. Application may be missing some relevant feedback that would help guide the user.

* Bug where some HEX values are only saving 5 digits instead of 6, causing the color to not show up

* When I create a new project, I should be able to see it in the drop-down menu immediately. Instead I have to refresh the page.

* Any save/generate/delete buttons should turn the cursor into a hand icon when you hover over them to further indicate that they are clickable.

* Definitely need some more padding/margins in the projects section around the palettes and their names

* I like the creativity of having all the boxes of different colors for displaying a palette, but it's almost a little too jarring to effectively see how the colors would work together. I think it works in the main content area with the big version for generating a new palette, but in the projects sidebar I'd probably simplify it to a single horizontal bar of the colors side-by-side.

## Testing

**18 points**: (20 possible points) Project has a running test suite that tests every server-side endpoint with many happy and sad path cases.

* Testing [all of these assertions](https://github.com/NikBorn/mod4-Palette-Picker/blob/master/test/routes.spec.js#L83-L144) is a little excessive. There's also no guarantee that your data will come back in any particular order, so relying on the index of an array element to assert it's values might intermittently fail. I'd rather you test one element from the array and assert that the array contains a particular object with certain values.

* You wouldn't send through an [id](https://github.com/NikBorn/mod4-Palette-Picker/blob/master/test/routes.spec.js#L166) during a POST request naturally, so don't do it in your tests either. Just assert that the returned response is a 201 with an id property, don't worry about the value.

* Same [here](https://github.com/NikBorn/mod4-Palette-Picker/blob/master/test/routes.spec.js#L182) - just pass through an empty object. You want your tests to mimic real-world environments as closely as possible.

## Commented Server File

**x points**: (10 possible points)

## JavaScript Style

**19 points**: (30 possible points) Application is thoughtfully put together with some duplication and no major bugs. Developer can speak to choices made in the code and knows what every line of code is doing.

* I'd move [this](https://github.com/NikBorn/mod4-Palette-Picker/blob/master/server.js#L26-L28) configuration up closer to the top of the file, where you're doing your other imports.

* [Meh](https://github.com/NikBorn/mod4-Palette-Picker/blob/master/server.js#L30-L31) this isn't doing anything, isn't helping you. Take it out.

* [No .catch](https://github.com/NikBorn/mod4-Palette-Picker/blob/master/server.js#L75) :( [Here](https://github.com/NikBorn/mod4-Palette-Picker/blob/master/server.js#L109) and [here](https://github.com/NikBorn/mod4-Palette-Picker/blob/master/server.js#L120) too.

* You shouldn't have to do this double nesty [database query](https://github.com/NikBorn/mod4-Palette-Picker/blob/master/server.js#L131-L142) to perform your error handling and deletion. You can just try to do the delete right off the bat, and if that deletion doesn't come back successfully, tell the user it failed.

* If you're not using it, [delete it](https://github.com/NikBorn/mod4-Palette-Picker/blob/master/server.js#L148-L154)

* [Whats this](https://github.com/NikBorn/mod4-Palette-Picker/blob/master/js/scripts.js)

* Having an object named [color](https://github.com/NikBorn/mod4-Palette-Picker/blob/master/public/js/scripts.js#L25-L26) contain a property name that's also called color is really confusing

* [KeWl SpElLiNg, BrO](https://github.com/NikBorn/mod4-Palette-Picker/blob/master/public/js/scripts.js#L52)

* Rather than getting nest with these [fetches](https://github.com/NikBorn/mod4-Palette-Picker/blob/master/public/js/scripts.js#L47-L60) I'd break the palettes fetch out into it's own function.

* You don't want to be [appending to the DOM](https://github.com/NikBorn/mod4-Palette-Picker/blob/master/public/js/scripts.js#L105-L126) on each iteration of a for loop. DOM manipulations are expensive. Instead, you'd want to use Document Fragments to build up all the HTML you want to append, and then add it to the DOM all at once at the end of the loop.

* You can simplify [this](https://github.com/NikBorn/mod4-Palette-Picker/blob/master/public/js/scripts.js#L171-L175) by just setting the value equal to the opposite of itself. e.g. `foo = !foo`


## Workflow

**x points**: (20 possible points)


### To get a 3 on this project, you need to score 110 points or higher
### To get a 4 on this project, you need to score 130 points or higher

# Final Score: x / 150