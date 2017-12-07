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

* [Wahh](https://github.com/jenPlusPlus/palette-picker/blob/master/server.js#L28), [wahhh](https://github.com/jenPlusPlus/palette-picker/blob/master/public/js/scripts.js#L101)

* [Yep](https://github.com/jenPlusPlus/palette-picker/blob/master/server.js#L40), but it doesn't hurt to have. Also [yes](https://github.com/jenPlusPlus/palette-picker/blob/master/server.js#L74)

* I'd just return the entire palette object [here](https://github.com/jenPlusPlus/palette-picker/blob/master/server.js#L142-L148) by not specifying that second argument with an array of column names. If you need that many things back from the newly created object, you might as well just get everything.

* Instead of swapping out an img [src](https://github.com/jenPlusPlus/palette-picker/blob/master/public/js/scripts.js#L27-L34) here, you could rework your css so that those images are actually a background image. That would allow you to just toggle the class for whether or not you want the locked or unlocked background.

* [This](https://github.com/jenPlusPlus/palette-picker/blob/master/public/js/scripts.js#L51-L79) is a little unruly. It's still clean and readable, but maybe you do write a loop to dynamically generate those palette-color divs? Instead of having all that repeat code.

* I know you're doing some event delegation [here](https://github.com/jenPlusPlus/palette-picker/blob/master/public/js/scripts.js#L86-L92) but this is a little tricky to read with this array of variables.

* Could you not just add `unique` to the project name column in your database schema to avoid having to do this whole [check](https://github.com/jenPlusPlus/palette-picker/blob/master/public/js/scripts.js#L144-L178)?

* ES6 shorthand would be really nice [here](https://github.com/jenPlusPlus/palette-picker/blob/master/public/js/scripts.js#L222-L226)

* You should do the deleting from page [within a .then](https://github.com/jenPlusPlus/palette-picker/blob/master/public/js/scripts.js#L239-L264) of your fetch request that deletes from the server. If anything goes wrong with that delete request, you'd be deleting an element from the page that still exists in your dataset.

* Fetch requests arent dependent on the [DOM](https://github.com/jenPlusPlus/palette-picker/blob/master/public/js/scripts.js#L285) so this function shouldn't be waiting for the whole window to load before you kick it off. Get that data ASAP.

## Workflow

**15 points**: (20 possible points)

* [This](https://github.com/jenPlusPlus/palette-picker/blob/master/.DS_Store) should be in your .gitignore file.

* Caught committing [node_modules](https://github.com/jenPlusPlus/palette-picker/commit/db503c248b059ea0542aa5795405ae361521d83f) =P

* Do cleanup like [removing console logs](https://github.com/jenPlusPlus/palette-picker/commit/b4814199fd2b1eca17a25cc56c12dea6233c48f4) in a completely separate commit to avoid cluttering up the diffs of your changesets.

* You don't have to file PRs on a project when you're working by yourself. You should still be using branches, but PRs are for code review.


### To get a 3 on this project, you need to score 110 points or higher
### To get a 4 on this project, you need to score 130 points or higher

# Final Score: x / 150
