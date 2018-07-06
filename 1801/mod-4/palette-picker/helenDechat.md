# Palette Picker Submission Form

[Project Spec](http://frontend.turing.io/projects/palette-picker.html)

# Basics

#### Link to the GitHub Repository for the Project
[palette-picker](https://github.com/hdechat/Palette-Picker)

#### Link to the Deployed Application
[heroku](https://helens-janky-colors.herokuapp.com/)

#### Link to your annotated server file
[annotated server file](https://github.com/hdechat/Palette-Picker/blob/commented-server-file/server.js)

## Completion

#### Were you able to complete the base functionality?
Yes
If not, explain what is missing and why.

#### Which extensions, if any, did you complete?

# Code Quality

#### Link to a specific block of your code on GitHub that you are proud of
[happy code](https://github.com/hdechat/Palette-Picker/blob/11891d46ff02625219b5fa9b9e25a4decf21b7c3/public/js/scripts.js#L52-L63)

* Why were you proud of this piece of code?
 I have the most fun with these type of puzzles. I like that it works and it's easy to understand.

#### Link to a specific block of your code on GitHub that you feel not great about
[sad code](https://github.com/hdechat/Palette-Picker/blob/5df5dcb506875d3f674bf98877c205848dd45db5/test/routes.spec.js#L192-L270)

* Why do you feel not awesome about the code? What challenges did you face trying to write/refactor it?
It's commented out sadly. I ran out of time trying to solve the puzzle of testing dynamic id params that are generated with the increments method that keep changing with each seed run. I thought I had a clever solution until I realized that for some reason they were just passing indiscriminantly.

#### Attach a screenshot or paste the output from your terminal of the result of your test-suite running.

[test suite](https://github.com/hdechat/Palette-Picker/blob/master/public/assets/screen-shot-testing-mocha.png)

#### Link to Design Inspiration

* Show us what you used as design inspiration (another color picker site, a dribbble UI element, a user flow, etc.) and explain what you stole from it
https://dribbble.com/shots/3497539-Health-data    
I liked the gradient background, and used that in a different shade. I was happy to find this site to keep it super easy!   
http://www.colorzilla.com/gradient-editor/

#### Please feel free to ask any other questions or make any other statements below!

Anything else you wanna say!  
I'm pretty happy with my functionality. I would have liked to have had more time to redo the UI for adding a saved palette to a saved project. User can save  palettes independently of projects. To save a palette to a project, user must click onto the palette, then onto the project name, and finally onto the save to project button. I didn't have enough time to create more visual indications of what's going on. But I am happy that there is an alert pop up that prevents the user from deleting a palette from the Palettes column if it is included in a project. Needs lots of CSS tlc, but it works :D


-----


# Instructor Feedback (Robbie)

## Specification Adherence

**35 points**: (50 possible points)

- Not seeing the projects and palettes list. I saved a project, refreshed the page, and all of the project were gone. Tough to know if projects are persisting and 
can't tell if I can save a palette to a project

## User Interface

**12 points**: (20 possible points)

- The UI is confusing in that you can save a palette without a project (this wasn't in the project specification), and then there is another button 
to save the palette into a project. So as a user I'm not sure which one is better or what is the recommended workflow. I think the "Save Palette to Project" button 
could be moved to its own visually separated section with the palette and project selection areas so that the button is grouped closely with the selection 
that is needed. It was tough to know what to do without the text guiding me.
- Slight bug in showing the hex values. The hex colors will not show until you click the "Pick Me Some Colors!" button, but clicking on saved-palette colors does 
not trigger the hex codes to show.

## Testing

**10 points**: (20 possible points)

- Ideally, setting [this environment variable](https://github.com/hdechat/Palette-Picker/blob/master/test/routes.spec.js#L1) should be done in your `npm test` script command: something 
like: `"test": "NODE_ENV=test mocha --exit"`
- Good job testing for body properties and values in [this test](https://github.com/hdechat/Palette-Picker/blob/master/test/routes.spec.js#L60-L86) and others
- Why the empty line [here](https://github.com/hdechat/Palette-Picker/blob/master/test/routes.spec.js#L107) and in other tests?
- [These commented out tests](https://github.com/hdechat/Palette-Picker/blob/master/test/routes.spec.js#L167-L270) should be fixed. One reason why these are behaving 
in a strange way is because the IDs are changing every time you run the seed files. Unfortunately, `knex` does not have a good tool for "database cleaning", which means 
something that runs every unit test (`it` block) and resets the ID values so they start incrementing from 1 each test. You can get around this by hard-coding ID values in 
your _test_ seed file, but it's not a best practice. See how you can fix these tests so they are not commented out anymore.

## Commented Server File

**7 points**: (10 possible points)

- What do you mean by ["root" here](https://github.com/hdechat/Palette-Picker/blob/commented-server-file/server.js#L5)?
- For [these lines](https://github.com/hdechat/Palette-Picker/blob/commented-server-file/server.js#L7-L9), be more specific than "user environment". What environment 
variables are being accessed in these lines?
- Good, I like the raw SQL interpretation [here](https://github.com/hdechat/Palette-Picker/blob/commented-server-file/server.js#L18) and other lines
- I would expect [this line](https://github.com/hdechat/Palette-Picker/blob/commented-server-file/server.js#L25) to have more information about what the `projects` variable contains. What do we expect to be passed through into the callback?
- Good explanation [here](https://github.com/hdechat/Palette-Picker/blob/commented-server-file/server.js#L91)

## JavaScript Style

**22 points**: (30 possible points)

- You should not need to explicitly set [this endpoint](https://github.com/hdechat/Palette-Picker/blob/master/server.js#L17) in your server file if you are setting the static asset path 
as you are [here](https://github.com/hdechat/Palette-Picker/blob/master/server.js#L15)
- Good error handling [here](https://github.com/hdechat/Palette-Picker/blob/master/server.js#L28-L30) for the case where the ID does not exist in the DB
- [This endpoint](https://github.com/hdechat/Palette-Picker/blob/master/server.js#L56) should not return a `204` if the project ID does not exist
- Why are [these endpoints](https://github.com/hdechat/Palette-Picker/blob/master/server.js#L98-L120) even created if they're not needed for the spec and other areas 
like UI or testing could be improved?
- Good first and [second migration](https://github.com/hdechat/Palette-Picker/blob/master/db/migrations/20180627141113_add-colors.js) to drop old column and add colors columns - the 
`up` and `down` look good
- In your client-side JS, don't forget to add `catch` to your promise chains to catch errors, handle errors, or at least use the catch for debugging (by console.log-ing)

## Workflow

**15 points**: (20 possible points)

- Would expect to see more granular commits for a project of this size. There were 54 commits when I looked, and this is after Heroku and travisCI setup
- Great job adding a `.gitignore` file in your first commit


### To get a 3 on this project, you need to score 110 points or higher
### To get a 4 on this project, you need to score 130 points or higher

# Final Score: 101 / 150
