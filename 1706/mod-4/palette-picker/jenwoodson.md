# Palette Picker Submission Form

[Project Spec](http://frontend.turing.io/projects/palette-picker.html)

# Basics

#### Link to the GitHub Repository for the Project
[palette-picker](https://github.com/jenPlusPlus/palette-picker)

#### Link to the Deployed Application
[heroku](https://jen-woodson-palette-picker.herokuapp.com/)

#### Link to your annotated server file
[annotated server file](https://github.com/jenPlusPlus/palette-picker/compare/annotate-server-file?expand=1#diff-78c12f5adc1848d13b1c6f07055d996e)

## Completion

#### Were you able to complete the base functionality?

I do not have a functionality to make sure all 5 randomly generated colors are unique. I simply forgot about this feature for a while and then ran out of time.

#### Which extensions, if any, did you complete?
none

# Code Quality

#### Link to a specific block of your code on GitHub that you are proud of
[happy code](https://github.com/jenPlusPlus/palette-picker/blob/master/public/js/scripts.js#L119-L125)

* Why were you proud of this piece of code?
This is the first time I successfully added an alert to HTML, rather than using alert();.

#### Link to a specific block of your code on GitHub that you feel not great about
[sad code](https://github.com/jenPlusPlus/palette-picker/blob/master/public/js/scripts.js#L53-L59)

* Why do you feel not awesome about the code? What challenges did you face trying to write/refactor it?
I don't like that I'm repeating the same line with a different number each time. I think I could use a loop to add these lines, but I did not have time to refactor this code.

#### Attach a screenshot or paste the output from your terminal of the result of your test-suite running.

[test suite](<img width="520" alt="screen shot 2017-12-01 at 5 16 10 pm" src="https://user-images.githubusercontent.com/6845268/33503818-8ff2ad2c-d6bb-11e7-999a-613762f6a0bb.png">)

#### Link to Design Inspiration

* Show us what you used as design inspiration (another color picker site, a dribbble UI element, a user flow, etc.) and explain what you stole from it
[design inspiration](https://codepen.io/team/lincolnloop/pen/QwQwza)
I really liked the box shadow on the palette, so I applied it to my destop-size UI. 

#### Please feel free to ask any other questions or make any other statements below!

I thought this project was really fun! I appreciate the simplicity of the backend.

-----


# Instructor Feedback (Brittany)

## Specification Adherence

**50 points**: (50 possible points) No approach was taken that is counter to the spirit of the project and its learning goals. There are no features missing from above that make the application feel incomplete or hard to use. Data persists on refresh using a knex/postgreSQL database.

## User Interface

**15 points**: (20 possible points) User interface is mostly intuitive, though the instructor might need some guidance on interactions. Styling is mostly consistent, but could use some clean up. Application may be missing some relevant feedback that would help guide the user.

* I like the drop-shadows and rounded corners on each color for the palettes, looks like paint chips!

* When there are no palettes or projects to show, it'd be nice to have a message that says 'You haven't created any projects yet!' and maybe some instructions for the user on how to do so.

* Cursor should change to a hand when hovering over save/generate/delete buttons.

* The added border when you hover over a palette within a project is a little bizarre because it jumps the rest of the content around by a pixel or two. You could probably set a completely transparent border around palettes to begin with (`rgba(0,0,0,0)`) and then make it fully opaque on hover if you want to keep that effect.

* Generally for a project revolving around colors like this, I'd keep the body background and text white or black, or something very subtle, as opposed to the pink and teal we currently have. You want the color palettes themselves to really *pop* compared to the rest of the application.

* Nice touch with the slightly opaque backgrounds around the lock icons and HEX values, makes it much easier to view that text no matter what color shows up behind it.

## Testing

**18 points**: (20 possible points) Project has a running test suite that tests every server-side endpoint with many happy and sad path cases.

* Your assertions in [these tests](https://github.com/jenPlusPlus/palette-picker/blob/master/test/routes.spec.js#L87-L174) test are pretty much identical. What you really want to do is have some additional seed data so that you can have palettes that exist under a *different* project, and you can verify that only the palettes that belong to a particular project are returned from `/api/v1/projects/:id/palettes`. Otherwise these tests don't really tell me that endpoint is working accurately -- it could accidentally be returning all palettes for all projects, as that's what your first test and endpoint are doing.

* There's actually no guarantee that your data will come back in a specific order unless you are explicitly sorting it. So assertions like [these](https://github.com/jenPlusPlus/palette-picker/blob/master/test/routes.spec.js#L97-L98), where you're dependent on certain values existing at a particular index of an array often have intermittent failures. It doesn't look like you're sorting your data any where in your server file so I'd be surprised if this was consistently working for you.

* You wouldn't send through an [id](https://github.com/jenPlusPlus/palette-picker/blob/master/test/routes.spec.js#L227) during a POST request naturally, so don't do it in your tests either. Just send through an empty object.

## Commented Server File

**x points**: (10 possible points)

## JavaScript Style

**x points**: (30 possible points)

## Workflow

**x points**: (20 possible points)


### To get a 3 on this project, you need to score 110 points or higher
### To get a 4 on this project, you need to score 130 points or higher

# Final Score: x / 150
