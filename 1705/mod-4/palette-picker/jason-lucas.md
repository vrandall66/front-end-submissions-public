# Palette Picker Submission Form

[Project Spec](http://frontend.turing.io/projects/palette-picker.html)

# Basics

#### Link to the GitHub Repository for the Project
[palette-picker](https://github.com/jasonlucas907/palette-picker)

#### Link to the Deployed Application
[heroku](https://jasonpalette.herokuapp.com/)

#### Link to your annotated server file
[annotated server file](https://github.com/jasonlucas907/palette-picker/blob/serverNotes/server.js)

## Completion

#### Were you able to complete the base functionality?

I was able to complete the base functionality.

#### Which extensions, if any, did you complete?

The user is able to manually change the color codes of the main palette.

# Code Quality

#### Link to a specific block of your code on GitHub that you are proud of
[happy code]()

* Why were you proud of this piece of code?

#### Link to a specific block of your code on GitHub that you feel not great about
[sad code](https://github.com/jasonlucas907/palette-picker/blob/master/public/js/scripts.js)

* Why do you feel not awesome about the code? What challenges did you face trying to write/refactor it?

My script file has alot of long if/else statements and repetitious functionality that I need to refactor.

#### Attach a screenshot or paste the output from your terminal of the result of your test-suite running.

Anything else you wanna say!

-----


# Instructor Feedback (Brittany)

## Specification Adherence

**50 points**: No approach was taken that is counter to the spirit of the project and its learning goals. There are no features missing from above that make the application feel incomplete or hard to use.

## User Interface

**16 points**: The application has many strong pages/interactions, but could use some cleanup to make it a bit more minimal.

* Nice CSS animation with the colors! I would leave the Palette Picker title in place instead of sliding it in from the right, it's a little distracting and I think takes away from the awesomeness of the color animations since it covers them up at the end. It could also be cool to do the transition flipped...having the colors fill in from the top to bottom...might make it look like "dripping paint" or something.

* Little weird to have commas after your drop down menu items for your project names.

* Using the bound boxes for each project is a nice way to keep the layout in tact, but it also makes it look a little busy. One thing you could do is remove the horizontal scroll bars for each project box by using the CSS property `overflow-x: hidden`. It's safe to assume that the width of each palette would be the same and nothing would overflow in that direction.


## Data Persistence with SQL Database

**20 points**: The application persists data in a SQL database with correct relationships between folders and URLs.

## Testing

**7 points**: Project has sporadic testing of some server-side endpoints. Missing some happy and sad path test cases.

* [This assertion](https://github.com/jasonlucas907/palette-picker/blob/master/test/roots.spec.js#L60) isn't super helpful if all you're checking is the property name. I'd rather you make a javascript object that represents a project in the database and check that it exists in the array.

* [This 404 test](https://github.com/jasonlucas907/palette-picker/blob/master/test/roots.spec.js#L66-L72) is redundant. You only need to do one 404 test for an endpoint that doesn't exist, doesn't matter if it is prefixed with `api/v1` or not.

* The description of this [test](https://github.com/jasonlucas907/palette-picker/blob/master/test/roots.spec.js#L99-L105) doesn't match the assertion you're making


## Commented Server File

**5 points**: Most lines of the server file (on a separate branch) are commented, but the explanation is sometimes lacking in demonstrating true understanding

## JavaScript Style

**12 points**: Your application has a significant amount of duplication and major room for refactoring and improvements.

* A common convention for organizing your [imports](https://github.com/jasonlucas907/palette-picker/blob/master/server.js#L1-L9) is to include any built-in libraries first, line break, third-party libraries second, line break, code that **you** wrote third, line break. So these imports could be reorganized like so:

```js
const path = require("path");

const express = require("express");
const app = express();
const bodyParser = require('body-parser');
const cors = require("express-cors");

const environment = process.env.NODE_ENV || "development";
const configuration = require("./knexfile")[environment];
const database = require("knex")(configuration);
```

* [This](https://github.com/jasonlucas907/palette-picker/blob/master/server.js#L13-L22) is a fine and dandy way to setup cors, butttttt you shouldn't need it on this project. Not sure what kind of problem you might've been running into that prompted you to add this code but it should be able to be taken out.

* Weird spacing [here](https://github.com/jasonlucas907/palette-picker/blob/master/server.js#L93-L98) make that a little hard to read. I'd tighten that up to a single line.

* If you're just returning a 204, you don't need to do a [.json()](https://github.com/jasonlucas907/palette-picker/blob/master/server.js#L134) too

* Copy-paste jobs are very clear when you don't change the names of the tables in the [comments](https://github.com/jasonlucas907/palette-picker/blob/master/db/seeds/test/testSeed.js#L4-L5) ;)

* The ordering of your API routes is kind of bizarre, generally you want to order your requests by ALL the methods you can call on a particular table. e.g. GET all projects, POST new project, GET single project by id, PUT/PATCH single project by id, DELETE single project by id (then the same for palettes)

* Lots of weird line breaks [here](https://github.com/jasonlucas907/palette-picker/blob/master/server.js#L93-L98)

* You're returning the entire object for your post request [here](https://github.com/jasonlucas907/palette-picker/blob/master/server.js#L98) but only the id [here](https://github.com/jasonlucas907/palette-picker/blob/master/server.js#L121). I don't care what you choose to do, but be consistent.

* I'd lose these [line breaks](https://github.com/jasonlucas907/palette-picker/blob/master/public/js/fetch.js#L7) before your .catches. Keep the catches close to the code they're actually catching.

* Eehhh, lots of [global variables here](https://github.com/jasonlucas907/palette-picker/blob/master/public/js/scripts.js#L1-L8), I'd wrap all your code in an IIFE if this is the way you want to handle these values. You want to avoid polluting the window object with your variables.

* Lots of [duplicate code here](https://github.com/jasonlucas907/palette-picker/blob/master/public/js/scripts.js#L12-L68) and [here](https://github.com/jasonlucas907/palette-picker/blob/master/public/js/scripts.js#L81-L115) and [here](https://github.com/jasonlucas907/palette-picker/blob/master/public/js/scripts.js#L118-L169) and [here](https://github.com/jasonlucas907/palette-picker/blob/master/public/js/scripts.js#L364-L411). Major room for improvement and refactoring to make your code more dynamic.

* These [conditionals](https://github.com/jasonlucas907/palette-picker/blob/master/public/js/scripts.js#L98-L100) are really trippy and difficult to read.

* Appending in a [loop](https://github.com/jasonlucas907/palette-picker/blob/master/public/js/scripts.js#L179-L194) is really slow and doing too many unecessary DOM Manipulations. You'd want to use a DocumentFragment in a scenario like this to build up a large chunk of HTML within your JavaScript first, then append it to the DOM all at once at the end of the loop.

* Not sure why you need these [setTimeouts](https://github.com/jasonlucas907/palette-picker/blob/master/public/js/scripts.js#L221-L222) but they are almost always a sure sign of a code smell.

* You shouldn't have 2 [document.ready handlers](https://github.com/jasonlucas907/palette-picker/blob/master/public/js/scripts.js#L406-L417)

* Fetch requests are not dependent on the DOM and therefore do not need to wait for document.ready. Kick off [this](https://github.com/jasonlucas907/palette-picker/blob/master/public/js/scripts.js#L416) request right away so that you can get your data ASAP.

## Workflow

**15 points**: Developer(s) make many small, atomic commits that document the evolution of the application but sometimes contain irrelevant changesets and inconsistent commit messages. Developer(s) use git branches and pull requests when applicable to incorporate changes into the application, and are not pushing fresh changes directly to master. Pull requests may contain little or no code review. There may be slight instances where the developer(s) have committed source code that should be .gitignored. There may be some instances of “dead” or commented-out code and debugger statements like console.log that need to be cleaned up.

* [CSS Palette Trash](https://github.com/jasonlucas907/palette-picker/commit/88fb9a99309a17da5d74457502ff6d5cee582c2b) is a really sad commit message, and doesn't give me any insight into what's going on in this commit. Try sticking to these [conventions](https://chris.beams.io/posts/git-commit/) for writing consistent and helpful messages.

* Nice use of issues and branches; pull requests here are kind of useless because you're working individually and nobody is reviewing your code. When you're working solo, I'd suggest using the standard merge/rebase workflow to keep your history clean and free of tons of merge commits.

* Instances of [commented out code](https://github.com/jasonlucas907/palette-picker/commit/5f23210d81549c4442fd52bb2edbf9ad6a2500e9) in this commit, which is also doing more than simply adding a form. This could be broken out into at least 2 separate commits to make the diff easier to read and keep the changesets relevant.


### To get a 3 on this project, you need to score 120 points or higher
### To get a 4 on this project, you need to score 140 points or higher

# Final Score: 125 / 160
