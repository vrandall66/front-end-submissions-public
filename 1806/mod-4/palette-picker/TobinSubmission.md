# Palette Picker Submission Form

[Project Spec](http://frontend.turing.io/projects/palette-picker.html)

# Basics

#### Link to the GitHub Repository for the Project
[palette-picker](https://github.com/Tobin-jn/bouquet-palette)

#### Link to the Deployed Application
[heroku](https://perfect-palette.herokuapp.com/)

#### Link to your annotated server file
[annotated server file](https://github.com/Tobin-jn/bouquet-palette/blob/annotated/server.js)

## Completion

#### Were you able to complete the base functionality?

Mostly yes-
Current logged issues:
* Users are able to enter duplicate project/palette names
* Site is not responsive
* Some functionality requires a page refresh, everything should function without a refresh
* Locked colors should reset after a palette is saved

#### Link to an image of your wireframe(s)
[wireframes](https://github.com/Tobin-jn/bouquet-palette/blob/master/images/palette-picker-wireframe.png)

#### Which extensions, if any, did you complete?

n/a

# Code Quality

#### Link to a specific block of your code on GitHub that you are proud of
[happy code](https://github.com/Tobin-jn/bouquet-palette/blob/master/public/js/apiCalls.js)

* Why were you proud of this piece of code?

This whole file... it was the first time I wrote fetch calls without considerable struggle! I understand on a deeper level now what promises are doing and how the fetch api is working.

ALSO, I always wanted to experiment with svg's. I took the flower svg icons and figured out how to manipulate colors via javascript. It was fun and I'm really glad I took the time to try that and move past my boring color wheel!

#### Link to a specific block of your code on GitHub that you feel not great about
[sad code](https://github.com/Tobin-jn/bouquet-palette/blob/master/public/js/script.js)
```javascript
$(document).ready(function() {
  if (JSON.parse(localStorage.getItem('currentColors'))) {
    let colors= JSON.parse(localStorage.getItem('currentColors'));;
    currentColors = {...colors};
    updateColors(colors.hex1, colors.hex2, colors.hex3, colors.hex4, colors.hex5)
    localStorage.clear();
  } else {
    generatePalette()
  }
});
```

I ran into an issue with being able to access all functionality with a page reload. When I make a new project, the page has to reload to have access to save a palette to that project. I populate a dropdown with a new project. To get that element created on the DOM, the only way I could get that working was through a reload. Because this element has the project id attached to it as an attribute. That project id is necessary to create a palette, but it comes from the database. I didn't know a way to get it without doing a GET request for that project with the id. Further the palette of colors on the flowers is randomly created after a page reload. So if someone creates a project and then wants to save their current palette, it will be lost. 

So... my "fix" to the palette issue was to temporarily save the palette (before a project is submitted) into local storage and then pull it out of local storage after that necessary page reload. At this point the user has access to the palette POST requests and can save to the project they made.


* Why do you feel not awesome about the code? What challenges did you face trying to write/refactor it?

I feel not awesome about it because I don't think it is the right way to solve this. The spec says everything must be functional without a page reload. 

#### Link to Design Inspiration

* Show us what you used as design inspiration (another color picker site, a dribbble UI element, a user flow, etc.) and explain what you stole from it

I didn't have a specific link. My first intention was to make a color wheel that would spin when you generate a new palette. Upon talking with my wife, she had the idea of a bouquet color picker. So I stole that idea!

I took the svg's from flaticon.com

#### Please feel free to ask any other questions or make any other statements below!

I loved this project! It was just the right amount of challenge with room to have some fun and experiment in the time frame.

-----


# Instructor Feedback (Instructor Name)

## Specification Adherence

**x points**: (50 possible points)

## User Interface

**x points**: (20 possible points)

## Commented Server File

**x points**: (10 possible points)

## JavaScript Style

**x points**: (30 possible points)

## Workflow

**x points**: (20 possible points)


### To get a 3 on this project, you need to score 95 points or higher
### To get a 4 on this project, you need to score 115 points or higher

# Final Score: x / 130
