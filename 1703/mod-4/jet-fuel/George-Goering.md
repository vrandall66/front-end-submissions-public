# Jet Fuel Submission Form

[Project Spec](http://frontend.turing.io/projects/jet-fuel.html)

[Project Spec](http://frontend.turing.io/projects/jet-fuel.html)

# Basics

#### Link to the Github Repository for the Project
[jetfuel](https://github.com/Ggoering/Jet-Fuel)

#### Link to the Deployed Application
[heroku](https://gg-jet-fuel-winning.herokuapp.com/)

#### Link to the annotated server file
[annotated server file 1](https://github.com/Ggoering/Jet-Fuel/blob/master/server.js)
[annotated server file 2](https://github.com/Ggoering/Jet-Fuel/blob/master/routes.js)
[annotated server file 3](https://github.com/Ggoering/Jet-Fuel/blob/master/controller.js)

## Completion

#### Were you able to complete the base functionality?

Everything except CSS animation

I built the drop downs and box displays using a display: none toggle.  Apparently you can't do CSS transitions with that CSS property.  Had my 1 yr wedding anniversary so spent a lot of this weekend doing non-coding things and couldn't learn a new way to implement & refactor in time for submission.

#### Which extensions, if any, did you complete?

None

# Code Quality

#### Link to a specific block of your code on Github that you are proud of
[happy code](https://github.com/Ggoering/Jet-Fuel/blob/master/public/scripts.js#L7-L9)

* Cool UX I copied from bit.ly and I have no idea why I needed to do the setTimeout to have access to the pasted element (without the setTimeout event.target.value and the val() of the input field were undefined or empty string) but it was my idea to try it and it worked.

#### Link to a specific block of your code on Github that you feel not great about
[sad code](https://github.com/Ggoering/Jet-Fuel/blob/master/public/scripts.js#L52-L75)

* I am having to clear the input fields before applying the for loop because I don't know how to append without duplicating what was there already & still reuse this same function everywhere possible. It wouldn't be so bad but it makes it so that the expanded folder tabs have to be reopened which is bad UX.  I'd probably hunt around for a better jQuery method than .append in order to refactor.

* In general all my event listeners are a little sad because I didn't get to implement button disables, key code refusals, and displaying of error messages to the user if they didn't submit something properly.

#### Attach a screenshot or paste the output from your terminal of the result of your test-suite running.

[test suite]()

Jet Fuel is running on 3000.
  Client Route
    ✓ is a single page app (43ms)
    ✓ should return a 404 for a route that does not exist

  API routes
    GET /api/v1/link
      ✓ Should return a list of all the links
    POST /api/v1/link
      ✓ should add a new link
    PUT /api/v1/link/:id
      ✓ should update a link with folder and description
    GET /api/v1/folder
      ✓ should list all the folders
    POST /api/v1/folder
      ✓ should add a new folder


  7 passing (356ms)


#### Please feel free to ask any other questions or make any other statements below!

Anything else you wanna say!

-----


# Instructor Feedback (Instructor Name)

## Specification Adherence

**x points**: Lorem ipsum dolor set amet

## User Interface

**x points**: Lorem ipsum dolor set amet

## Data Persistence with SQL Database

**x points**: Lorem ipsum dolor set amet

## Testing

**x points**: Lorem ipsum dolor set amet

## JavaScript Style

**x points**: Lorem ipsum dolor set amet

## Workflow

**x points**: Lorem ipsum dolor set amet


### To get a 3 on this project, you need to score 110 points or higher
### To get a 4 on this project, you need to score 135 points or higher

# Final Score: x / 150
