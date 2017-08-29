# Jet Fuel Submission Form

[Project Spec](http://frontend.turing.io/projects/jet-fuel.html)

# Basics

#### Link to the Github Repository for the Project
[jetfuel](https://github.com/danielbucket/JetFuel)

#### Link to the Deployed Application
[heroku](https://jetgas.herokuapp.com/)

#### Link to your annotated server file
[annotated server file]()

## Completion

#### Were you able to complete the base functionality?

If not, explain what is missing and why.
* Didn't get the sorting done. Short on time.
* URL validation. Short on time.
* Date display. Short on time.
* Testing using seeding. Short on time.

#### Which extensions, if any, did you complete?

# Code Quality

  * I'd be proud of my code if I felt like I was able to really put time and care into making something significant. As it is, all my code was written rushed and haphazard.

* Why do you feel not awesome about the code? What challenges did you face trying to write/refactor it?
* Time is the number one challenge. When you spend 3/7 days trying to remember how to write jQuery and another 2 days troubleshooting, you're left with 2 days of actual code writing.

#### Attach a screenshot or paste the output from your terminal of the result of your test-suite running.

`
Server is running on 3300
  Client Routes
    ✓ should return status(200) (44ms)
    ✓ sad panda path

  GET/api/v1/folders
    ✓ should return

  GET/api/v1/shortURL
    ✓ should return these values:


  4 passing (100ms)

danielbucket:jetfuel/ (master) $
`

#### Please feel free to ask any other questions or make any other statements below!

Anything else you wanna say!

-----


# Instructor Feedback (Robbie)

## Specification Adherence

**50 points**: Lorem ipsum dolor set amet

## User Interface

**20 points**: Lorem ipsum dolor set amet

## Data Persistence with SQL Database

**20 points**: Lorem ipsum dolor set amet

## Testing

**20 points**: Lorem ipsum dolor set amet

## Commented Server File

**10 points**: Lorem ipsum dolor set amet

## JavaScript Style

**20 points**: Lorem ipsum dolor set amet

## Workflow

**20 points**: Lorem ipsum dolor set amet


### To get a 3 on this project, you need to score 120 points or higher
### To get a 4 on this project, you need to score 140 points or higher

# Final Score: x / 160


**Need to fix before eval can be completed**

* Production is not working - one big reason for this is that your `baseRoute` is defined on your client side using `localhost`, which is not the URL of your heroku app, which is why you're getting a 404 response for POST to `/folders` in the console
  * Instead of using an absolute path with `localhost:3000`, use relative paths in your fetch calls. For instance, instead of the absolute path to `localhost:3000/api/v1/folders`, just use the relative path `/api/v1/folders`

* You need to have s separate branch where you have commented lines explaining your sever file (as described in the project spec)