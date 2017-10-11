# Palette Picker Submission Form

[Project Spec](http://frontend.turing.io/projects/palette-picker.html)

# Basics

#### Link to the GitHub Repository for the Project
[palette-picker](https://github.com/jackmallahan/palette-picker)

#### Link to the Deployed Application
[heroku](https://jacks-palette-picker.herokuapp.com/)

#### Link to your annotated server file
[annotated server file](https://github.com/jackmallahan/palette-picker/tree/comments)

## Completion

#### Were you able to complete the base functionality?

I was able to complete all functionality. I would like to write an endpoint to delete projects, and plan on doing that. I for some reason am having a hard time with my DELETE test and couldn't figure it out.

#### Which extensions, if any, did you complete?

I did not complete any extensions

# Code Quality

#### Link to a specific block of your code on GitHub that you are proud of
[happy code](https://github.com/jackmallahan/palette-picker/blob/c1992b1ec7b959182abcf8008fd92e248db2a9ce/public/js/scripts.js#L29-L43)

* Why were you proud of this piece of code?
I just thought this was a fun piece of code. The front end stuff like this is what I really enjoy writing. Making my title have random colors for each letter is a completely superfluous function, but it is fun.

#### Link to a specific block of your code on GitHub that you feel not great about
[sad code](https://github.com/jackmallahan/palette-picker/blob/51bf12b00c2741c11d9bc5d3f7837253ba85b62e/test/routes.spec.js#L226-L235)

* Why do you feel not awesome about the code? What challenges did you face trying to write/refactor it?

I don't like this code because I have no idea why it doesn't work. I asked a couple of classmates and they had theirs very similarly. I don't know why it doesn't work.

#### Attach a screenshot or paste the output from your terminal of the result of your test-suite running.

<img width="560" alt="screen shot 2017-10-08 at 11 39 25 pm" src="https://user-images.githubusercontent.com/25092178/31326288-0c684884-ac83-11e7-9b9d-05db0f119edc.png">

#### Please feel free to ask any other questions or make any other statements below!

I made some good progress and wrote some code that I am definitely proud of. I really enjoyed writing the front end code for this and had fun with that. I think this was a good introduction to writing with Express and I definitely need to hone my skills in this area. Plus I got to name this file jacks-pp and that makes me laugh.

-----


# Instructor Feedback (Brittany)

## Specification Adherence

**x points**: Lorem ipsum dolor set amet

## User Interface

**15 points**: The application has many strong pages/interactions, but a few holes in lesser-used functionality.

* Cool spacebar keyboard shortcut, but it's common practice to also include a button. What if my spacebar doesn't work? :(

* I like that the lock and hex codes only show up on hover, but the coloring can be really difficult to see depending on the color that shows up for the palette. One common way to get around this is by adding a small background color to wrap that lock and hex color, that's somewhat opaque. (e.g. a white background at 70% opacity, with a black lock and black text, or vice versa.)

* Would be nice to have a 'No palettes in this project' message when you add a new project before it has any palettes. Otherwise it takes up a lot of weird and awkward whitespace.

## Data Persistence with SQL Database

**20 points**: The application persists data in a SQL database with correct relationships between folders and URLs.

## Testing

**x points**: Lorem ipsum dolor set amet

## JavaScript Style

**x points**: Lorem ipsum dolor set amet

* [This](https://github.com/jackmallahan/palette-picker/blob/master/db/seeds/test.js) is some really intense indentation...you'll probably want to switch to 2 or 4-space indentation rather than these massive tabs. Not common to see code that looks like this in the real world. Generally you want to keep each line length to max 80 characters (that's a common linter rule to put in place), and you're tabbing enthusiam pushes your code super far to that limit.

## Workflow

**16 points**:  Developer(s) make many small, atomic commits that document the evolution of the application but sometimes contain irrelevant changesets and inconsistent commit messages. Developer(s) use git branches and pull requests when applicable to incorporate changes into the application, and are not pushing fresh changes directly to master. Pull requests may contain little or no code review. There may be slight instances where the developer(s) have committed source code that should be .gitignored. There may be some instances of “dead” or commented-out code and debugger statements like console.log that need to be cleaned up.

* First things first, I know naming is hard, but try to do better than `jacks-pp`. +1 point for making me laugh.

* .DS_Store [files](https://github.com/jackmallahan/palette-picker/blob/master/.DS_Store) should be .gitignored. People will make fun of you if you commit them ;) You can edit your [global git config](https://help.github.com/articles/ignoring-files/#create-a-global-gitignore) to always ignore .DS_Store files 

* Commit messages like [this](https://github.com/jackmallahan/palette-picker/commit/049cb43702981055921e74ace12fe8758eebb1f2) aren't super helpful. We know you wrote some code, no need to tell us in the commit message. I'd rewrite it like "Prepend projects on page load". It's also doing a little too much in the changesets - you did a lot more than just write a function here, you wrote HTML and CSS along with it. This could be broken out into 3 separate commits so the diffs are easier to read.


### To get a 3 on this project, you need to score 120 points or higher
### To get a 4 on this project, you need to score 140 points or higher

# Final Score: x / 160
