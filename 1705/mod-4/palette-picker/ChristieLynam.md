# Palette Picker Submission Form

[Project Spec](http://frontend.turing.io/projects/palette-picker.html)

# Basics

#### Link to the GitHub Repository for the Project
[palette-picker](https://github.com/christielynam/palette-picker)

#### Link to the Deployed Application
[heroku](https://palette-picker-cl.herokuapp.com/)

#### Link to your annotated server file
[annotated server file](https://github.com/christielynam/palette-picker/blob/server-comments/server.js)


## Completion

#### Were you able to complete the base functionality?

If not, explain what is missing and why.

Yes, with the exception of 1 minor bug. When i click the delete icon, I originally get a 500 error (/api/v1/palettes/undefined). When I refresh the page and click it again, it removes the palette from the database correctly.

#### Which extensions, if any, did you complete?

Ability to modify color in the generator

# Code Quality

#### Link to a specific block of your code on GitHub that you are proud of
[happy code](https://github.com/christielynam/palette-picker/blob/master/public/js/scripts.js#L20-L32)

* Why were you proud of this piece of code?

I was proud of making a nested fetch call for each project to append that projects palettes on page load. 

#### Link to a specific block of your code on GitHub that you feel not great about
[sad code](https://github.com/christielynam/palette-picker/blob/master/public/js/scripts.js#L44-L59)
[more sad code](https://github.com/christielynam/palette-picker/blob/master/public/js/scripts.js#L102-L116)

* Why do you feel not awesome about the code? What challenges did you face trying to write/refactor it?

I feel like I should probably be able to write both append palette functions with one function, but have just not had the time to do a major refactor.

#### Attach a screenshot or paste the output from your terminal of the result of your test-suite running.

<img width="763" alt="screen shot 2017-10-06 at 10 54 46 pm" src="https://user-images.githubusercontent.com/20754511/31304860-7f119a20-aae9-11e7-841a-32b3c3b3ae24.png">

#### Please feel free to ask any other questions or make any other statements below!

-----


# Instructor Feedback (Brittany)

## Specification Adherence

**60 points**: No approach was taken that is counter to the spirit of the project and its learning goals. There are no features missing from above that make the application feel incomplete or hard to use.

* Looks like the delete bug has been fixed and is working appropriately now, no points off for that.

* Great job getting an extension in there! I know the spec wasn't explicit about this, but it would be nice if you could edit the color and have the option to re-save the palette.

## User Interface

**11 points**: The application shows effort in the interface. The evaluator has some difficulty using the application when reviewing the features in the user stories.

* The form flow for saving a new palette is slightly confusing. I know your solution closely mimics the wireframes, but wireframes are simply a guide, not something to be implemented and followed exactly to spec. Think about this flow from a user perspective, does it make sense to you? I initially tried to create a new palette and save it to a new project right away, but it seems this is a two-step process. After I create a new project, I'd immediately want to click 'save palette' and save it to that newly generated project, but instead it defaults to whatever is selected in the drop down on the left. I'd add more titles and descriptions of what you expect the user flow to be here to avoid confusion.

* I'd add a note under the project headers that says something like 'There are no palettes saved for this project' if there are no palettes present. The alignment makes it a little difficult to visually see the heirarchy, especially if there are no palettes present. I'd consider either left-aligning the content or at least bumping the palette names onto their own line. (Since palette names can vary in length, it makes that entire line really wonky if you have a long name)

* I don't take points off for style that I simply don't like, but one thing I would suggest is making your background, buttons and fonts a little more subtle and minimal, so that the palette colors actually stand out and become the prominent visual attraction on the page. It's difficult to see if a color palette is actually appealing when there are other competing colors and words on the page.

## Data Persistence with SQL Database

**20 points**: The application persists data in a SQL database with correct relationships between folders and URLs.

## Testing

**15 points**: Project has a running test suite that tests every server-side endpoint, but some assertions are commented out or failing

* [This 404 test](https://github.com/christielynam/palette-picker/blob/master/test/routes.spec.js#L68-L75) is redundant. You only need to do one 404 test for an endpoint that doesn't exist, doesn't matter if it is prefixed with `api/v1` or not. [This](https://github.com/christielynam/palette-picker/blob/master/test/routes.spec.js#L165-L174) is also the same exact 404 test. Remove these duplicates.

* Assuming [this](https://github.com/christielynam/palette-picker/blob/master/test/routes.spec.js#L112) is commented out because it's failing, curious why

* [This](https://github.com/christielynam/palette-picker/blob/master/test/routes.spec.js#L129-L160) is nice and thorough, but really difficult to read and doesn't offer you a ton of additional integrity or insight about the success of the request. I'd pick one of the objects, make an actual javascript object to represent it, and check if the array contains it or not.

## Commented Server File

**8 points**: Each line of the server file (on a separate branch) is commented and explains the code using mostly precise, correct terminology and specificity

* Getting ahead of yourself a little [here](https://github.com/christielynam/palette-picker/blob/server-comments/server.js#L3), all path does as a library is give you access to helper methods for navigating your directories.

* [This](https://github.com/christielynam/palette-picker/blob/server-comments/server.js#L9) is more about accessing the correct database in the correct environment, rather than the application itself. It gives you an instance of the database you want to connect to.

* Proper terminology [here](https://github.com/christielynam/palette-picker/blob/server-comments/server.js#L26) is **assigning** the body of the request to a variable. Not setting.

## JavaScript Style

**17 points**: Application is thoughtfully put together with minor duplication, no major bugs. Developer can speak to choices made in the code and knows what every line of code is doing.

* The ordering of your API routes is kind of bizarre, generally you want to order your requests by ALL the methods you can call on a particular table. e.g. GET all projects, POST new project, GET single project by id, PUT/PATCH single project by id, DELETE single project by id (then the same for palettes)

* Better error handling [here](https://github.com/christielynam/palette-picker/blob/master/server.js#L103) would be to give back an error message that tells the user what ID they actually tried to grab. Maybe they fat-fingered the number and it wasn't obvious to them.

* Very nice, clean, organized and consistently-styled code. It looks pretty and is easy to read.

* Love the way you made [this](https://github.com/christielynam/palette-picker/blob/master/public/js/scripts.js#L10-L18) dynamic by looping through numbers and using corresponding class names, but could you do a similar thing [here](https://github.com/christielynam/palette-picker/blob/master/public/js/scripts.js#L105-L110) to reduce some of this repeat code?

* Fetch requests are not depending on the DOM and therefore do not need to wait for document.ready. Kick off [this](https://github.com/christielynam/palette-picker/blob/master/public/js/scripts.js#L147) request right away so that you can get your data ASAP.

* Appending in a [loop](https://github.com/christielynam/palette-picker/blob/master/public/js/scripts.js#L25) like [this](https://github.com/christielynam/palette-picker/blob/master/public/js/scripts.js#L45) is really slow and doing too many unecessary DOM Manipulations. You'd want to use a DocumentFragment in a scenario like this to build up a large chunk of HTML within your JavaScript first, then append it to the DOM all at once at the end of the loop.

* Using es6 shorthand [here](https://github.com/christielynam/palette-picker/blob/master/public/js/scripts.js#L96) would really shorten up this line and make it easier to read

## Workflow

**15 points**: Developer(s) make many small, atomic commits that document the evolution of the application but sometimes contain irrelevant changesets and inconsistent commit messages. Developer(s) use git branches and pull requests when applicable to incorporate changes into the application, and are not pushing fresh changes directly to master. Pull requests may contain little or no code review. There may be slight instances where the developer(s) have committed source code that should be .gitignored. There may be some instances of “dead” or commented-out code and debugger statements like console.log that need to be cleaned up.

* Some instances of [commented](https://github.com/christielynam/palette-picker/commit/c64452e04203af1078e10c2ba9e10a9a748cf081#diff-78c12f5adc1848d13b1c6f07055d996eR5). [out](https://github.com/christielynam/palette-picker/commit/d95a368363b9a6f554389acffa582debf8930a29#diff-22cbc1db13fa2c410616712446566a7cR51). [code](https://github.com/christielynam/palette-picker/commit/d95a368363b9a6f554389acffa582debf8930a29#diff-22cbc1db13fa2c410616712446566a7cL54) and [console.logs](https://github.com/christielynam/palette-picker/commit/d95a368363b9a6f554389acffa582debf8930a29#diff-22cbc1db13fa2c410616712446566a7cR63) You can use `git stash` to hide changes that you don't want to commit yet and pop them back on when you want them back with `git stash pop`. 

* Nice, consistent formatting of your commit messages but I'd recommend capitalizing the first letter of each commit message. This makes them even more consistent with the auto-generated Merge Commits, and is the most common practice on development teams.

* Good use of branches, pull requests are kind of irrelevant in this scenario because you are working individually and don't have anyone reviewing your code. You can use the typical merge or rebase workflow for getting your changes into master when you're working solo. This keeps your history clean and free of excessive merge commits, without having to push changes directly to master.

* This [commit](https://github.com/christielynam/palette-picker/commit/d95a368363b9a6f554389acffa582debf8930a29#diff-22cbc1db13fa2c410616712446566a7cR63) probably does a little too much - if the problem was that you forgot a leading slash in your api endpoint, that should be the only single-line change in this commit. Front-end changesets are irrelevant and should be put into a subsequent commit, or the commit message should reflect that all of these changes are being made.


### To get a 3 on this project, you need to score 120 points or higher
### To get a 4 on this project, you need to score 140 points or higher

# Final Score: 146 / 160
