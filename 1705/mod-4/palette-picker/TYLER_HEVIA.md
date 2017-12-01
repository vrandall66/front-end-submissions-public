# Palette Picker Submission Form

[Project Spec](http://frontend.turing.io/projects/palette-picker.html)

# Basics

#### Link to the GitHub Repository for the Project
[palette-picker](https://github.com/tylerjhevia/palette-picker)

#### Link to the Deployed Application
[heroku](https://palette-picker-th.herokuapp.com/)

#### Link to your annotated server file
[annotated server file](https://github.com/tylerjhevia/palette-picker/blob/server-comments/server.js)

## Completion

#### Were you able to complete the base functionality?

Yes, I finished it over the weekend.

#### Which extensions, if any, did you complete?

# Code Quality

#### Link to a specific block of your code on GitHub that you are proud of
[happy code](https://github.com/tylerjhevia/palette-picker/blob/master/server.js) lines 112-122

```app.delete("/api/v1/palettes/delete/:id", (request, response) => {
  database("palettes")
    .where("id", request.params.id)
    .delete()
    .then(palette => {
      palette
        ? response.sendStatus(204)
        : response.status(422).send({ error: "Could not find palette" });
    })
    .catch(error => response.status(500).json({ error }));
});
```

There's not anything special about this delete endpoint but it took me a long time to figure out that I needed to check if my response had a length before I sent a 204 or 422 status, so I was happy when it finally worked.

#### Link to a specific block of your code on GitHub that you feel not great about
[sad code](https://github.com/tylerjhevia/palette-picker/blob/master/public/js/script.js) lines 5-19
```const swatchOne = $(".one");
const swatchTwo = $(".two");
const swatchThree = $(".three");
const swatchFour = $(".four");
const swatchFive = $(".five");

const labelOne = $(".label-one");
const labelTwo = $(".label-two");
const labelThree = $(".label-three");
const labelFour = $(".label-four");
const labelFive = $(".label-five");

const swatches = [swatchOne, swatchTwo, swatchThree, swatchFour, swatchFive];
const labels = [labelOne, labelTwo, labelThree, labelFour, labelFive];
```

I created variables for each swatch and label and inserted them into arrays. I did this because I wanted to map through each swatch and label and I couldn't get it to work using something like $('.swatch') to select all swatches.


#### Attach a screenshot or paste the output from your terminal of the result of your test-suite running.

[test suite](https://imgur.com/a/ycRrK)

#### Please feel free to ask any other questions or make any other statements below!

I didn't finish testing or styling, and I didn't get a chance to do much refactoring. I'm going to finish that this weekend.

-----


# Instructor Feedback (Robbie)

## Specification Adherence

**35 points**: (50 possible points)

- No persistence of data because the API request has been hard-coded to [localhost](https://github.com/tylerjhevia/palette-picker/blob/master/public/js/script.js#L63) instead of a relative path

## User Interface

**12 points**: (20 possible points)

- Would be nice to arrive at the page with a palette already generated
- Not obvious at all that a palette color is locked
- Page is jumping around when hovering over a palette color because of the added border
- Form text needs room on the left side so it doesn't bump up against the left side of the input box
- Form layout and flow is not obvious for the user (the text there makes it seem like you need to create a new project every time)
- Great to have the placeholder text of `This project has no saved palettes!`

## Data Persistence with SQL Database

**20 points**: (20 possible points)

- Schema looks good with one-to-many relationship using primary/foreign key

## Testing

**15 points**: (20 possible points)

- You have [this before block](https://github.com/tylerjhevia/palette-picker/blob/master/test/routes.spec.js#L11-L19) at the top level of the test file, and then you have one at a lower level when you make your API calls - you only need one at the level of your API calls
- Good job with the before and beforeEach blocks at the API level
- Good sad path test [here](https://github.com/tylerjhevia/palette-picker/blob/master/test/routes.spec.js#L107)
- Should test for the actual value [here](https://github.com/tylerjhevia/palette-picker/blob/master/test/routes.spec.js#L173) if you can

## Commented Server File

**5 points**: (10 possible points)

- Some vague comment lines, [like this one](https://github.com/tylerjhevia/palette-picker/blob/server-comments/server.js#L15), and missing some code comments 

## JavaScript Style

**13 points**: (20 possible points)

- You should not need [CORS](https://github.com/tylerjhevia/palette-picker/blob/master/server.js#L13-L22) for this project because you are requesting everything on the front-end from your own server, which is the same origin
- Before you [insert or change any data in a database](https://github.com/tylerjhevia/palette-picker/blob/master/server.js#L79-L88), you should be performing some kind of validation on the data coming in to be sure that it's exactly what you need
- [Multi-line ternaries](https://github.com/tylerjhevia/palette-picker/blob/master/server.js#L105-L107) look ok at first, but at that point, just use an if/else statement for clarity and readability for other developers and future you - [this](https://github.com/tylerjhevia/palette-picker/blob/master/public/js/script.js#L164-L176) cannot be a ternary, no way
- Good job using DATA attributes in your HTML to store data about a resource, but the same should go for [palette names as classes](https://github.com/tylerjhevia/palette-picker/blob/master/public/js/script.js#L101) - this should go in a data attribute
- Make sure you have a `.catch()` for every client-side [fetch call](https://github.com/tylerjhevia/palette-picker/blob/master/public/js/script.js#L136) - and every promise for that matter

## Workflow

**17 points**: (20 possible points)

- Would like to see a little more smaller, more atomic commits, but good job adding .gitignore right off the bat

### To get a 3 on this project, you need to score 120 points or higher
### To get a 4 on this project, you need to score 140 points or higher

Waiting for data persistence on production.

# Final Score: x / 160
