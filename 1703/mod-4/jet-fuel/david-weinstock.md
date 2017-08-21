# Jet Fuel Submission Form

[Project Spec](http://frontend.turing.io/projects/jet-fuel.html)

# Basics

#### Link to the Github Repository for the Project
[jetfuel](https://github.com/dstock48/jet-fuel)

#### Link to the Deployed Application
[heroku](https://jet-fuel-8888.herokuapp.com/)

#### Link to your annotated server file
[annotated server file](https://github.com/dstock48/jet-fuel/blob/comments/server.js)

## Completion

#### Were you able to complete the base functionality?

Yes.

#### Which extensions, if any, did you complete?

None.

# Code Quality

#### Link to a specific block of your code on Github that you are proud of
[happy code](https://github.com/dstock48/jet-fuel/blob/76cdd8e3dac9f394386742d60196ae1696b50035/public/main.js#L123-L144)

* Why were you proud of this piece of code?

I thought this was a pretty nifty way of dynamically creating div containers with a classname corresponding to the folder name passed into the function. And then using that classname to be dynamically targeted in the next function to add link cards to their corresponding container.

#### Link to a specific block of your code on Github that you feel not great about
[sad code](https://github.com/dstock48/jet-fuel/blob/76cdd8e3dac9f394386742d60196ae1696b50035/public/main.js#L96-L111)

* Why do you feel not awesome about the code? What challenges did you face trying to write/refactor it?

This felt like a very hacky way of getting the fontawesome folder icon to toggle between open/close. I wish there could have been a more simple way to just toggle a single class on and off that would have switched between the open/close icon.

#### Attach a screenshot or paste the output from your terminal of the result of your test-suite running.

```
npm test

> jet-fuel@1.0.0 test /Users/Dave/Documents/Turing/MOD4/projects/jet-fuel
> mocha



Jet Fuel URL Shortener is running on http://localhost:8888
  Client-side Routes
    ✓ should return the static HTML file
    ✓ should redirect from a shortened URL to a long URL (648ms)

  API Routes
    GET /api/v1/folders
Re-seed complete!
      ✓ should return all of the folders
Re-seed complete!
      ✓ should return an error status if you do not hit the correct endpoint
    POST /api/v1/folders
Re-seed complete!
      ✓ should create a new folder
Re-seed complete!
      ✓ should not create a new folder with missing data
Re-seed complete!
      ✓ should not create a folder with a duplicate name
    GET /api/v1/links
Re-seed complete!
      ✓ should return all of the links
Re-seed complete!
      ✓ should return an error status if you do not hit the correct endpoint
    POST /api/v1/links
Re-seed complete!
      ✓ should create a new link
Re-seed complete!
      ✓ should not create a new link with missing data


  11 passing (1s)
```

#### Please feel free to ask any other questions or make any other statements below!

This was a fun project! It was definitely a lot of new concepts to learn in a week, but it really helped demystify what goes on in the back-end.

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
