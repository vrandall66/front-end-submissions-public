# Palette Picker Submission Form

[Project Spec](http://frontend.turing.io/projects/palette-picker.html)

# Basics

#### Link to the GitHub Repository for the Project
[palette-picker](https://github.com/johnmboudreaux/palette-picker)

#### Link to the Deployed Application
[heroku](https://jm-palette-picker.herokuapp.com/)

#### Link to your annotated server file
[annotated server file](https://github.com/johnmboudreaux/palette-picker/blob/server-comments/server.js)

## Completion

#### Were you able to complete the base functionality?

I was able to get all base functionality complete.

#### Which extensions, if any, did you complete?

I didnt get to any of the suggested extensions, but I did put in functionality to delete projects.

# Code Quality

#### Link to a specific block of your code on GitHub that you are proud of
[happy code](https://github.com/johnmboudreaux/palette-picker/blob/c84bcd40d2bd24bd5e7d4bb282643a45fbc10bb7/public/js/scripts.js#L107-L160)


I really like when it all comes together and displays on the dom.Its always satisfying feeling.

#### Link to a specific block of your code on GitHub that you feel not great about
[sad code](https://github.com/johnmboudreaux/palette-picker/blob/c84bcd40d2bd24bd5e7d4bb282643a45fbc10bb7/public/js/scripts.js#L134-L160)

I know some of this code I wrote that I'm proud of, but I do really like the functionality of it. It could be written cleaner and not look so bulky.

#### Testing Suite


![screen shot 2017-12-02 at 9 26 25 pm](https://user-images.githubusercontent.com/20631355/33522355-ce610f30-d7a7-11e7-9a4e-df69494a9cb0.png)


#### Link to Design Inspiration

I did come across some palette transition stuff that I liked and did include in this project I also reflected on Louisa's
mod1 lesson on less is more and drew from that how i wanted to design it.

#### Please feel free to ask any other questions or make any other statements below!

Anything else you wanna say!

nope

-----


# Instructor Feedback (Robbie)

## Specification Adherence

**50 points**: (50 possible points)

* Spec adherence looks good!

## User Interface

**15 points**: (20 possible points)

* I like the color transitions after new palette generations - would like the transition to be a little faster to see the palette and generate new palettes quicker
* The forms are clear, but the width are very long for the amount of text expected to be contain in the dropdowns or text boxes

## Testing

**12 points**: (20 possible points)

* Since you're using promises in the test, [like this one](https://github.com/johnmboudreaux/palette-picker/blob/master/test/routes.spec.js#L56), you shouldn't need to call `done()`, but you do want to return the promise (`return chai(...)`).
* [This part of your test](https://github.com/johnmboudreaux/palette-picker/blob/master/test/routes.spec.js#L184-L192) can be overkill depending on the dev team you're working on. Some will want the check by making a request, and some will want to assume that unless you get any errors, the DB has done it's thing correctly. Just keep in mind not to nest too many requests or else the test can be difficult to read.
* [This](https://github.com/johnmboudreaux/palette-picker/blob/master/test/routes.spec.js#L226) should not have a status of 201 since it is not creating a new record
* Want to see a sad path around POST requests where there is missing information (params) in the body
* Good job with the happy paths

## Commented Server File

**7 points**: (10 possible points)

* Comments look good
* Want to see a little more clarity around some lines [like this](https://github.com/johnmboudreaux/palette-picker/blob/server-comments/server.js#L14), how does this line enable you to configure the knex environment?
* Not sure what you mean [here](https://github.com/johnmboudreaux/palette-picker/blob/server-comments/server.js#L47)

## JavaScript Style

**22 points**: (30 possible points)

* Should not need to explicitly return a response [here](https://github.com/johnmboudreaux/palette-picker/blob/master/server.js#L30) and in other places in your route handlers - a time where you do need to use an explicit return is if the response is within an if/else conditional
* [This chunk of code](https://github.com/johnmboudreaux/palette-picker/blob/master/server.js#L121-L127) is a good candidate for pulling out into its own function or middleware since it is used in other route handlers with the difference being the expected parameters
* [For this situation](https://github.com/johnmboudreaux/palette-picker/blob/master/server.js#L166) where the record does not exist in the database, you would return a 404 response instead of a 422 because the resource does not exist
* What out for leaving in `console.log` or [console.error](https://github.com/johnmboudreaux/palette-picker/blob/master/server.js#L183) if you have an error response in place
(looking at [this version](https://github.com/johnmboudreaux/palette-picker/blob/ebbdd12ea4d4e72e28605965ec91b6406b32878a/public/js/scripts.js) of your public JS file)
* One thing to note with using `fetch` is that it will not error on 404 - in order to hit the `.catch` on a 404, you can check for `response.ok` [demonstrated in the MDN docs here](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API/Using_Fetch#Checking_that_the_fetch_was_successful)
* Be sure you have a `catch()` on everything [promise based](https://github.com/johnmboudreaux/palette-picker/blob/ebbdd12ea4d4e72e28605965ec91b6406b32878a/public/js/scripts.js#L86), including fetch calls
* I'm sure you know [this function](https://github.com/johnmboudreaux/palette-picker/blob/ebbdd12ea4d4e72e28605965ec91b6406b32878a/public/js/scripts.js#L126-L152) could use some refactoring and separation of responsibility

## Workflow

**16 points**: (20 possible points)

* Want to see smaller, more atomic commits for similar units of functionality/features
* Good job adding `.gitignore` file early with node modules - there is a [good file](https://github.com/github/gitignore/blob/master/Node.gitignore) I typically use for Node projects

### To get a 3 on this project, you need to score 110 points or higher
### To get a 4 on this project, you need to score 130 points or higher

# Final Score: 122 / 150

