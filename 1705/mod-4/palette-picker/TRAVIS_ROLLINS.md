# Palette Picker Submission Form

[Project Spec](http://frontend.turing.io/projects/palette-picker.html)

# Basics

#### Link to the GitHub Repository for the Project
[palette-picker](https://github.com/Kalikoze/Palette-Picker)

#### Link to the Deployed Application
[heroku](https://tr-palette-picker.herokuapp.com/)

#### Link to your annotated server file
[annotated server file](https://github.com/Kalikoze/Palette-Picker/blob/tr-comments/server.js)

## Completion

#### Were you able to complete the base functionality?

Yes.

If not, explain what is missing and why.

#### Which extensions, if any, did you complete?

N/A

# Code Quality

#### Link to a specific block of your code on GitHub that you are proud of
[happy code](https://github.com/Kalikoze/Palette-Picker/blob/master/public/js/scripts.js#L120-L128)

* Why were you proud of this piece of code?

I was pretty excited about this function partially because it's the first time I've used the data attribute.  It was pretty awesome to be able to store the hex value within the data attribute of the HTML element and then save it for later.  I was also excited to be able to not only get the value of each color, but also assign the color to the colors on the main page all within the same loop.  

#### Link to a specific block of your code on GitHub that you feel not great about
[sad code](https://github.com/Kalikoze/Palette-Picker/blob/master/public/js/scripts.js#L81-L99)

* Why do you feel not awesome about the code? What challenges did you face trying to write/refactor it?

I think it was just more frustrating to me about having to send each color in an array as separate values, since knex does not take arrays easily.  I feel like this could get messy especially if you had more than 5 values.  What if you had 20 hex values or some other kind of data?  Would you have to literally store each one as a string?  I'm just curious how I could go about this better next time.  Thank you!!!

#### Attach a screenshot or paste the output from your terminal of the result of your test-suite running.

[test suite](https://slack-files.com/T029P2S9M-F7EKRJLLA-5007c74145)

#### Please feel free to ask any other questions or make any other statements below!

This was a pretty fun project.  I was nervous about doing the backend in the beginning, but I have a better understanding of it now after this project.   I know I've still got plenty to learn, and am excited to get your comments back so I can do better next time.  Cheers! 

-----


# Instructor Feedback (Robbie)

## Specification Adherence

**50 points**: (50 possible points)

- Looks like all the features are there (no extensions)

## User Interface

**13 points**: (20 possible points)

- I like the transition to change colors, but it takes too long - I want to flip through palettes quickly and see the results
- A form on the very top of the page is not an obvious place for user interaction...especially if it's above the name of the site
- I like the organization of the projects on the left, but they are tough to differentiate between project containers because the style and colors are so similar, little to divide each project

## Data Persistence with SQL Database

**20 points**: (20 possible points)

- Schema looks good with one-to-many relationship using primary/foreign key

## Testing

**15 points**: (20 possible points)

- Good job with the before and beforeEach blocks
- For [this test](https://github.com/Kalikoze/Palette-Picker/blob/master/test/routes.spec.js#L63), you should be looking for an ID integer value that doesn't exist, not a string, for a record that doesn't exists in the DB
- Same as above [here](https://github.com/Kalikoze/Palette-Picker/blob/master/test/routes.spec.js#L100) - also the title doesn't match the test
- Good sad path test [here](https://github.com/Kalikoze/Palette-Picker/blob/master/test/routes.spec.js#L129)
- Good test, but [this](https://github.com/Kalikoze/Palette-Picker/blob/master/test/routes.spec.js#L211) should respond with a 404

## Commented Server File

**7 points**: (10 possible points)

- Good overall, looking for more technically accurate explanations in some places, though. For instance, [this part](https://github.com/Kalikoze/Palette-Picker/blob/tr-comments/server.js#L9) about environments - very vague just to say you are setting it up

## JavaScript Style

**15 points**: (20 possible points)

- If you're sending a JSON object in the response, [like this one](https://github.com/Kalikoze/Palette-Picker/blob/master/server.js#L32), use the `.json` method instead of the `.send` method
- Need to test for the case where the ID of the [item to delete](https://github.com/Kalikoze/Palette-Picker/blob/master/server.js#L56) might not exist in the DB
- Great job using DATA attributes in your HTML, but the `${paletteId}` also belongs in a data attribute

## Workflow

**17 points**: (20 possible points)

- Need some smaller, more atomic commits, but good job adding .gitignore right off the bat


### To get a 3 on this project, you need to score 120 points or higher
### To get a 4 on this project, you need to score 140 points or higher

# Final Score: 137 / 160
