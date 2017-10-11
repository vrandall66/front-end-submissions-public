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

**x points**: Lorem ipsum dolor set amet

## User Interface

**16 points**: The application has many strong pages/interactions, but could use some cleanup to make it a bit more minimal.

* Nice CSS animation with the colors! I would leave the Palette Picker title in place instead of sliding it in from the right, it's a little distracting and I think takes away from the awesomeness of the color animations since it covers them up at the end. It could also be cool to do the transition flipped...having the colors fill in from the top to bottom...might make it look like "dripping paint" or something.

* Little weird to have commas after your drop down menu items for your project names.

* Using the bound boxes for each project is a nice way to keep the layout in tact, but it also makes it look a little busy. One thing you could do is remove the horizontal scroll bars for each project box by using the CSS property `overflow-x: hidden`. It's safe to assume that the width of each palette would be the same and nothing would overflow in that direction.


## Data Persistence with SQL Database

**x points**: Lorem ipsum dolor set amet

## Testing

**x points**: Lorem ipsum dolor set amet

## JavaScript Style

**x points**: Lorem ipsum dolor set amet

## Workflow

**15 points**: Developer(s) make many small, atomic commits that document the evolution of the application but sometimes contain irrelevant changesets and inconsistent commit messages. Developer(s) use git branches and pull requests when applicable to incorporate changes into the application, and are not pushing fresh changes directly to master. Pull requests may contain little or no code review. There may be slight instances where the developer(s) have committed source code that should be .gitignored. There may be some instances of “dead” or commented-out code and debugger statements like console.log that need to be cleaned up.

* [CSS Palette Trash](https://github.com/jasonlucas907/palette-picker/commit/88fb9a99309a17da5d74457502ff6d5cee582c2b) is a really sad commit message, and doesn't give me any insight into what's going on in this commit. Try sticking to these [conventions](https://chris.beams.io/posts/git-commit/) for writing consistent and helpful messages.

* Nice use of issues and branches; pull requests here are kind of useless because you're working individually and nobody is reviewing your code. When you're working solo, I'd suggest using the standard merge/rebase workflow to keep your history clean and free of tons of merge commits.

* Instances of [commented out code](https://github.com/jasonlucas907/palette-picker/commit/5f23210d81549c4442fd52bb2edbf9ad6a2500e9) in this commit, which is also doing more than simply adding a form. This could be broken out into at least 2 separate commits to make the diff easier to read and keep the changesets relevant.


### To get a 3 on this project, you need to score 120 points or higher
### To get a 4 on this project, you need to score 140 points or higher

# Final Score: x / 160
