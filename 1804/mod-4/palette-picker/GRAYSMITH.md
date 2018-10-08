# Palette Picker Submission Form

[Project Spec](http://frontend.turing.io/projects/palette-picker.html)

# Basics

#### Link to the GitHub Repository for the Project

[palette-picker](https://github.com/GraySmith00/palette-picker)

#### Link to the Deployed Application

[heroku](https://gs-palettepicker.herokuapp.com/)

#### Link to your annotated server file

[annotated server file](https://github.com/GraySmith00/palette-picker/blob/b5fc04a57adf6ae83faf2aba66b143b61c6033cb/server.js)
[annotated projects routes file](https://github.com/GraySmith00/palette-picker/blob/b5fc04a57adf6ae83faf2aba66b143b61c6033cb/routes/projects.js)

## Completion

#### Were you able to complete the base functionality?

Yes, I think I was able to complete the base functionality

#### Link to an image of your wireframe(s)

[wireframes](https://i.imgur.com/qT2g20Q.png)

#### Which extensions, if any, did you complete?

Unfortunately I didn't have time to finish any of the extentions.

# Code Quality

#### Link to a specific block of your code on GitHub that you are proud of

[happy code](https://github.com/GraySmith00/palette-picker/blob/52d5a4e6ef0691c3c001c0f6c67893dd856116ec/routes/projects.js#L16-L41)

- Why were you proud of this piece of code?
  I was proud of this code because it allows you to save a project to the database, but also provides some data validation and sends back the appropriate feedback to the front end if the user is trying to submit a project without a name or submit a project name that already exists.

#### Link to a specific block of your code on GitHub that you feel not great about

[sad code](https://github.com/GraySmith00/palette-picker/blob/52d5a4e6ef0691c3c001c0f6c67893dd856116ec/public/js/index.js#L1-L7)

- Why do you feel not awesome about the code? What challenges did you face trying to write/refactor it?

I really liked the idea of having one source of truth for the main palette and making each color an object with a locked value and a hexValue. I think in the long run it makes my code my more succinct and easy to understand. I didn't like how I had to keep it as a global variable though. I wasn't sure how else to access this data from so many other methods.

#### Link to Design Inspiration

- Show us what you used as design inspiration (another color picker site, a dribbble UI element, a user flow, etc.) and explain what you stole from it

[file tree](https://dribbble.com/shots/1996199-Assets-List-View)

I really wanted my application to have an easy to use file tree that is intuitive and everyone would know how to use immediately. It's not perfect yet I'm still working out a few things.

#### Please feel free to ask any other questions or make any other statements below!

I hope its ok that I used BlingJS. I was very excited to use it. I think its a really cool library that is super lightweight (only about 30 lines of code). It basically lets you use the $ and .on from jQuery but everything else is in vanilla JavaScript.

---

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
