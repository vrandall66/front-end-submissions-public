# Palette Picker Submission Form

[Project Spec](http://frontend.turing.io/projects/palette-picker.html)

# Basics

#### Link to the GitHub Repository for the Project
[palette-picker](https://github.com/bbp5280/palette-picker)

#### Link to the Deployed Application
[heroku](https://palette-picker-bp.herokuapp.com/)

#### Link to your annotated server file
[annotated server file](https://github.com/bbp5280/palette-picker/blob/server-comments/server.js)

## Completion

#### Were you able to complete the base functionality?

The missing items are
  - Testing
  - Design research implementation 
  
 In the end I ran out of time. I struggled with some functionality which caused a time crunch I did not overcome.
 I will be finishing these over the weekend. 
  
#### Which extensions, if any, did you complete?

# Code Quality

#### Link to a specific block of your code on GitHub that you are proud of
[happy code](https://github.com/bbp5280/palette-picker/blob/8afb0d04e9251a92b13430bc329846ad5c64e6a6/public/js/scripts.js#L27-L45)

I like this fetch function to retrieve and build projects and palettes as it is mostly broken down into easy single functionality functions. 

#### Link to a specific block of your code on GitHub that you feel not great about
[sad code](https://github.com/bbp5280/palette-picker/blob/8afb0d04e9251a92b13430bc329846ad5c64e6a6/public/js/scripts.js#L127-L146)

This is mostly a duplicate function. I am serving back the wrong data in the response to use the original. I know how to refactor this but did not get there. 

#### Attach a screenshot or paste the output from your terminal of the result of your test-suite running.

<img width="953" alt="screen shot 2018-01-09 at 5 26 21 pm" src="https://user-images.githubusercontent.com/26842728/34750098-5bcf8c52-f562-11e7-8c4a-335fceaac889.png">

#### Link to Design Inspiration

I intended to impliment this style for my inputs and design buttons to match I did not get this done yet.
  https://dribbble.com/shots/1747015-Sky-Labels

#### Please feel free to ask any other questions or make any other statements below!


-----


# Instructor Feedback (Robbie)

## Specification Adherence

**50 points**: (50 possible points)

* Looks like everything is in place, nice job

## User Interface

**12 points**: (20 possible points)

* Took me a while to find the New Palette button in the top left corner
* Ideally, forms are styled and text larger, but I'm sure it was a time issue
* I can't create an identical project name, which is great, but nothing happens if I try to do so - give the user some indication of what happened

## Testing

**0 points**: (20 possible points)

* No API testing...

## Commented Server File

**7 points**: (10 possible points)

* Want a little more information [here](https://github.com/bbp5280/palette-picker/blob/server-comments/server.js#L14) about the purpose of body parser - you always need a good reason to bring in external packages
* "connect" [database](https://github.com/bbp5280/palette-picker/blob/server-comments/server.js#L27)?
* [Here](https://github.com/bbp5280/palette-picker/blob/server-comments/server.js#L58), the request body is being assigned to the project variable, sounds like you just have it reversed
* Overall, good comments

## JavaScript Style

**22 points**: (30 possible points)

* You do not need an explicit `return` [here](https://github.com/bbp5280/palette-picker/blob/master/server.js#L18), but you would need to use it explicitly if you are sending a response within an if/else statement
* [This](https://github.com/bbp5280/palette-picker/blob/master/server.js#L39-L41) is a good portion of code where you could refactor into its own function or middleware since you're doing the same thing in another POST request route handler - the only difference is the params that are expected
* One thing to note with using `fetch` is that it will not error on 404 - in order to hit the `.catch` on a 404, you can check for `response.ok` [demonstrated in the MDN docs here](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API/Using_Fetch#Checking_that_the_fetch_was_successful)
* [This](https://github.com/bbp5280/palette-picker/blob/master/server.js#L79) should be a 404 response because the resource is not found - the request structure is OK
* Good job having `catch()` on all of your client-side fetch calls
* Consider moving [this](https://github.com/bbp5280/palette-picker/blob/master/public/js/scripts.js#L65-L81) to an HTML template
* Careful with your [indentation](https://github.com/bbp5280/palette-picker/blob/master/public/js/scripts.js#L57-L58)

## Workflow

**15 points**: (20 possible points)

* Need to add you `.gitignore` right away so you don't end up with `.DS_STORE` files in [your projects](https://github.com/bbp5280/palette-picker)
* Need some smaller, more atomic commits


### To get a 3 on this project, you need to score 110 points or higher
### To get a 4 on this project, you need to score 130 points or higher

# Final Score: x / 150
