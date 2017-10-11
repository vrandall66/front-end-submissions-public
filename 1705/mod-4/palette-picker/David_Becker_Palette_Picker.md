# Palette Picker Submission Form

[Project Spec](http://frontend.turing.io/projects/palette-picker.html)

# Basics

#### Link to the GitHub Repository for the Project
[palette-picker](https://github.com/davidbecker6081/PalettePicker)

#### Link to the Deployed Application
[heroku](https://david-palette-picker.herokuapp.com/)

#### Link to your annotated server file
[annotated server file](https://github.com/davidbecker6081/PalettePicker/blob/add-comments-server/server.js)

## Completion

#### Were you able to complete the base functionality?

I've completed all of the base functionality although there were a few UI changes I wanted to make. Mostly to do with notifying the user of various actions such as creating a new project, displaying a project with no palettes, and creating a new palette.

#### Which extensions, if any, did you complete?

None

# Code Quality

#### Link to a specific block of your code on GitHub that you are proud of
[happy code](https://github.com/davidbecker6081/PalettePicker/blob/master/public/js/scripts.js#L196-L214)

* Why were you proud of this piece of code?

I feel like this piece of code is a combination of so many things I've learned in the past 3 modules. It includes selecting jquery elements by parent container and then child. It includes a fetch call to an API endpoint that I built, consuming promises, a for in loop (which is pretty new to me), using bracket notation, and a little bit of functional javascript where one function is returning a value that another function then uses (running inside out).

#### Link to a specific block of your code on GitHub that you feel not great about
[sad code](https://github.com/davidbecker6081/PalettePicker/blob/master/public/js/scripts.js#L122-L141)

* Why do you feel not awesome about the code? What challenges did you face trying to write/refactor it?

Most of the reason I feel sad about this code is because I think that there is great bit of refactoring to be done here. It actually is a pretty cool piece of code based on what it's doing, but it's doing wayyy too much for one function. This needs to be split out into multiple smaller functions and I need to find a way to get rid of the nested if/else statements. 

#### Attach a screenshot or paste the output from your terminal of the result of your test-suite running.

[test suite](https://i.imgur.com/qE65GR6.png)

I have a few tests skipped because of this error, which I haven't figure out YET

[error](https://i.imgur.com/whpibuK.png)

#### Please feel free to ask any other questions or make any other statements below!

Anything else you wanna say!

It's been hard for me to understand all of the connection between database and the server.js file. But now at the end of the project, I feel like my grasp is on the incline. I made some choices that may not seem like efficient ones, completely for the sake of getting practice doing the things we're learning. For instance I chose to make a fetch call to get a specific palette to display on the main display when you clicked on it. This gave me the opportunity to do a couple of things again, one being making a fetch call to the API endpoint, two being writing another endpoint handler, and three being writing a test for this endpoint handler. It would have been a lot easier to store the color values in the DOM elements and just grab them straight from there, but I wanted the practice doing it the other way. 

[example of this](https://github.com/davidbecker6081/PalettePicker/blob/master/public/js/scripts.js#L196-L214)

-----


# Instructor Feedback (Brittany)

## Specification Adherence

**50 points**: No approach was taken that is counter to the spirit of the project and its learning goals. There are no features missing from above that make the application feel incomplete or hard to use.

## User Interface

**10 points**: The application shows effort in the interface, but the evaluator has some difficulty using the application when reviewing the features in the user stories. Particularly lacking in user feedback after interactions.

* Love the subtle fade transition you implemented when generating a new palette, hate the giant dark drop-shadow border around the palette and form fields. The same subtlety you applied to the fade transition, apply to those drop shadows. They are a bit harsh.

* If I try to save a new palette but don't have any projects available to save it to, I don't get any error handling or message about what went wrong :( 

* Really difficult to tell that I've created a new project when I hit 'Save' because it appears in a drop-down and nowhere else on the UI.

* Don't let Jack make PP jokes on your app. 

* When I select a project that has no palettes, it would be nice to see a message that says 'This project has no palettes'. Otherwise it looks like a bug or something is missing when I select a project and nothing appears. 

## Data Persistence with SQL Database

**20 points**: The application persists data in a SQL database with correct relationships between folders and URLs.

## Testing

**x points**: Lorem ipsum dolor set amet

## JavaScript Style

**x points**: Lorem ipsum dolor set amet

* [This](https://github.com/davidbecker6081/PalettePicker/blob/master/db/migrations/20171003162939_initial.js#L5) is a weird column name. You either want to use snake_case or camelCase, not a combination of the two. I'd rename this to `projectName` or `project_name`

* Don't forget to always have a `.catch` for every [.then](https://github.com/davidbecker6081/PalettePicker/blob/master/db/seeds/test/test.js#L55)

## Workflow

**15 points**: Developer(s) make many small, atomic commits that document the evolution of the application but sometimes contain irrelevant changesets and inconsistent commit messages. Developer(s) use git branches and pull requests when applicable to incorporate changes into the application, and are not pushing fresh changes directly to master. Pull requests may contain little or no code review. There may be slight instances where the developer(s) have committed source code that should be .gitignored. There may be some instances of “dead” or commented-out code and debugger statements like console.log that need to be cleaned up.

* Some of your commit messages are really useful and [informative](https://github.com/davidbecker6081/PalettePicker/commit/afe3dfbef854a3af3cb005555e582487028ecc85) and others are...kinda [useless](https://github.com/davidbecker6081/PalettePicker/commit/0a4f2d8692a160976cd7fdc1bc77b1fb8b844f67). Even when you get frustrated or you're throwing shit at the wall, try to be consistent with your commit messages.

* Even though the commit message [here](https://github.com/davidbecker6081/PalettePicker/commit/afe3dfbef854a3af3cb005555e582487028ecc85) is nice, the commit itself is doing way too much work and includes lots of instances of commented out code. You can use `git stash` to hide changes that you don't want to commit yet and pop them back on when you want them back with `git stash pop`.

* Nice use of issues and branches; pull requests here are kind of useless because you're working individually and nobody is reviewing your code. When you're working solo, I'd suggest using the standard merge/rebase workflow to keep your history clean and free of tons of merge commits.



### To get a 3 on this project, you need to score 120 points or higher
### To get a 4 on this project, you need to score 140 points or higher

# Final Score: x / 160
