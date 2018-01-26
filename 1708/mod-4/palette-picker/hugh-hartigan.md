# Palette Picker Submission Form

[Project Spec](http://frontend.turing.io/projects/palette-picker.html)

# Basics

#### Link to the GitHub Repository for the Project
[palette-picker](https://github.com/HartiganHM/palette-picker)

#### Link to the Deployed Application
[heroku](https://palettepicker.herokuapp.com/)

#### Link to your annotated server file
[annotated server file](https://github.com/HartiganHM/palette-picker/blob/master/server.js)

## Completion

#### Were you able to complete the base functionality?

Yes

If not, explain what is missing and why.

#### Which extensions, if any, did you complete?

None

# Code Quality

#### Link to a specific block of your code on GitHub that you are proud of
[happy code](https://github.com/HartiganHM/palette-picker/blob/9c31aace7dd7de47d8996d8b69655efe1ca99330/public/js/scripts.js#L329-L357)

* Why were you proud of this piece of code?

The hurdle to get this section to work correctly was one of my greatest because of several bugs that showed up (ie duplicating existing palettes, overwriting background colors, etc.). I had to figure out a unique class to apply to each color and palette group in order to target unique palettes and their respective colors. I initially used a combination of the palette name and project name, but this lead to errors with spaces or non-alphanumeric characters. I implemented a regex screen on all inputs, but, through user testing, found that people wanted to use spaces or special characters. I then refactored the application of the classes to use the unique `pallete.id` applied to each palette through the backend database.

#### Link to a specific block of your code on GitHub that you feel not great about
[sad code](https://github.com/HartiganHM/palette-picker/blob/9c31aace7dd7de47d8996d8b69655efe1ca99330/public/js/scripts.js#L90-L124)

* Why do you feel not awesome about the code? What challenges did you face trying to write/refactor it?

This section of code uses a few global variables that deference different data points for the projects and palettes to be used elsewhere in the application. This was the first and foremost refactor I wanted to tackle but was unable to do it quickly without breaking large portions of functionality in the application.

#### Attach a screenshot or paste the output from your terminal of the result of your test-suite running.

[test suite](https://i.imgur.com/H07Wvld.png)

#### Link to Design Inspiration

* Show us what you used as design inspiration (another color picker site, a dribbble UI element, a user flow, etc.) and explain what you stole from it

My primary inspiration for overall layout was from the website Coolors, as I use it consistently with every project I've made at Turing. Additionally, I wanted to make something only using flat color shapes with no hard lines, similar to Japanese paintings. Inspiration 2 and 3 gave me an idea for how I wanted to set-up the overall layout and color scheme, which only used shapes to define different bodies of an image, instead of using hard lines to provide division between objects. The simple clarity of these designs is fun, but engaging, which is something I wanted to incorporate into my project. Inspiration 4 and 5 inspired me to keep things simple, but have interactive movement created by the use of basic shapes. Ultimately, I wanted all of my elements to lead into one another through some sort of simple, organic shapes (ie tubes, circles, etc.). My thought was to make Palette Picker a machine that used simple buttons and pipes to build each palette.

* [Inspiration 1: Coolors](https://coolors.co/495867-577399-bdd5ea-f7f7ff-fe5f55)
* [Inspiration 2: Girl with Bike](https://dribbble.com/shots/3888881-Girl-With-Her-Bike)
* [Inspiration 3: Ketchup Bottles](https://dribbble.com/shots/4131216-Ketchup)
* [Inspiration 4: Playground Gif](https://dribbble.com/shots/3947591-Playground)
* [Inspiration 5: Shapes Gif](https://dribbble.com/shots/3867318-Shapes)

#### Please feel free to ask any other questions or make any other statements below!

Though I am happy with the overall functionality of my project and the architecture of my backend, I didn't get to implement nearly as many of my design inspirations as I would have liked. My goal is to continue working on this to really paint the picture I envisioned at the onset of this project. However, I am incredibly happy with how quickly I was able to setup the backend database, though this can be somewhat attributed to my prior experience with Node.js. Additionally, though the testing was difficult at first, I think setting up the new environments was eye-opening in terms of how modular you can make the design process of any application.

Anything else you wanna say!

One comment I do want to make is that I wish we had more lessons grouped together at the start of the week with more work time later in the week. I was stalled with the backend at a certain point, waiting to see how more of the endpoint setup and testing should actually be implemented in my project.

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
