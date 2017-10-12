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


### To get a 3 on this project, you need to score 120 points or higher
### To get a 4 on this project, you need to score 140 points or higher

# Final Score: x / 160
