# Palette Picker Submission Form

[Project Spec](http://frontend.turing.io/projects/palette-picker.html)

# Basics

#### Link to the GitHub Repository for the Project
[palette-picker](https://github.com/JorgeEdPerezGa/palette-picker)

#### Link to the Deployed Application
[heroku](https://pallete-picker.herokuapp.com/)

#### Link to your annotated server file
[annotated server file](https://github.com/JorgeEdPerezGa/palette-picker/blob/master/server.js)

## Completion

#### Were you able to complete the base functionality?
Everything works, but I need to hard refresh the page for new projects to show.

#### Which extensions, if any, did you complete?

# Code Quality

#### Link to a specific block of your code on GitHub that you are proud of
[happy code](https://github.com/JorgeEdPerezGa/palette-picker/blob/master/public/scripts.js)

* Why were you proud of this piece of code?
I have loved being able to post to my own back end.

#### Link to a specific block of your code on GitHub that you feel not great about
[sad code](https://github.com/JorgeEdPerezGa/palette-picker/blob/master/public/scripts.js)

* Why do you feel not awesome about the code? What challenges did you face trying to write/refactor it?

line 179, I confused myself with the relationship between projects and palettes.

#### Attach a screenshot or paste the output from your terminal of the result of your test-suite running.

[test suite](http://g.recordit.co/7me5ZgdiEe.gif)

#### Link to Design Inspiration

* Show us what you used as design inspiration (another color picker site, a dribbble UI element, a user flow, etc.) and explain what you stole from it

[inspiration](https://color.adobe.com/)

#### Please feel free to ask any other questions or make any other statements below!

I would like to do more with the UI.

-----


# Instructor Feedback (Robbie)

## Specification Adherence

**40 points**: (50 possible points)

- Bug: When you add a new project, all of the palettes on the UI double and appear twice unless you refresh
- Bug: You are able to add non-unique project names ("Test" and "Test" is possible)
- When you select the colors in the saved palettes, the hex values change to rgb
- Project was handed in a late state (-5)

## User Interface

**17 points**: (20 possible points)

- Overall, very pleasant interface - I like the dark background behind the palette, makes the colors easier to view
- For the lock icon, it is always in a "locked" position, but then it is the background that changes. I would expect the lock to look "unlocked" when you are not locking a color

## Testing

**17 points**: (20 possible points)

- Great test suite overall - you're testing for prperties and values of pretty much everything
- Missing a sad path for deleting a palette (think about trying to delete a palette that does not exist in the database, an `:id` that does not exist) - you have the functionality for it [here](https://github.com/JorgeEdPerezGa/palette-picker/blob/master/server.js#L124)

## Commented Server File

**7 points**: (10 possible points)

- This should be on a separate branch
- Watch out for [typos](https://github.com/JorgeEdPerezGa/palette-picker/blob/master/server.js#L1)
- The [environment](https://github.com/JorgeEdPerezGa/palette-picker/blob/master/server.js#L26) is not just for development
- Careful with the verbs on the [route handlers](https://github.com/JorgeEdPerezGa/palette-picker/blob/master/server.js#L40) - you're saying the route handler "makes" a request, but actually the route handler "takes" a request and performs some logic accordingly
- Great job, especially since English is not your first language

## JavaScript Style

**23 points**: (30 possible points)

- It would be great to be able to [pull this out](https://github.com/JorgeEdPerezGa/palette-picker/blob/master/server.js#L95-L103) into its own piece of middleware. That way, you could reuse this functionality for other endpoints that need to check parameters.
- Can add a [uniqueness check to columns](https://github.com/JorgeEdPerezGa/palette-picker/blob/master/db/migrations/20180314205051_initial.js#L5) since this is required in the spec, http://knexjs.org/#Schema-unique
- [This line](https://github.com/JorgeEdPerezGa/palette-picker/blob/master/server.js#L21) is not necessary - you are not using url-encoded data from forms in this application

## Workflow

**17 points**: (20 possible points)

- Good job not having `node_modules` in your repository, but I do see a `.DS_Store` file committed to master. You should add this file to your `.gitignore`


### To get a 3 on this project, you need to score 110 points or higher
### To get a 4 on this project, you need to score 130 points or higher

# Final Score: 116 / 150
