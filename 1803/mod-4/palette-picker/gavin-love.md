# Palette Picker Submission Form

[Project Spec](http://frontend.turing.io/projects/palette-picker.html)

# Basics

#### Link to the GitHub Repository for the Project
[palette-picker](https://github.com/gavin-love/PalettePicker)

#### Link to the Deployed Application
[heroku](https://another-palette-picker.herokuapp.com/)

#### Link to your annotated server file
[annotated server file]()

## Completion

#### Were you able to complete the base functionality?
I was not able to set up functionality for deleting projects or testing. I will complete by end of day 8/20. I needed to spend time with
my wife over the weekend, it was our 2 year anniversary. I also had to put a new alternator in her car. 

#### Which extensions, if any, did you complete?

# Code Quality

#### Link to a specific block of your code on GitHub that you are proud of
[happy code]()

const generateColorPalette = e => {
  if (e.which === 32) {

    const randomColor = () => '#' + Math.floor(Math.random() * 16777215).toString(16);

    for (let i = 0; i <= 4; i++) {
      const color = randomColor()

      if (!$(`.palette_${i + 1}`).hasClass('isLocked')) {
        $(`.palette_${i + 1}`).css("background-color", color);
        $(`.palette_${i + 1}`).children('p').text(color);
      }
    }
  }
}

* Why were you proud of this piece of code?
short and clean

#### Link to a specific block of your code on GitHub that you feel not great about
[sad code]()

* Why do you feel not awesome about the code? What challenges did you face trying to write/refactor it?

I wasn't particularlly happy about having all the JavaScript in one file. It would have been nice to be able to import and export files.

#### Attach a screenshot or paste the output from your terminal of the result of your test-suite running.

[test suite]()

#### Link to Design Inspiration

* Show us what you used as design inspiration (another color picker site, a dribbble UI element, a user flow, etc.) and explain what you stole from it

#### Please feel free to ask any other questions or make any other statements below!

Anything else you wanna say!

-----


# Instructor Feedback (Instructor Name)

## Specification Adherence

**x points**: (50 possible points)

## User Interface

**x points**: (20 possible points)

## Testing

**x points**: (20 possible points)

## Commented Server File

**x points**: (10 possible points)

## JavaScript Style

**x points**: (30 possible points)

## Workflow

**x points**: (20 possible points)


### To get a 3 on this project, you need to score 110 points or higher
### To get a 4 on this project, you need to score 130 points or higher

# Final Score: x / 150
