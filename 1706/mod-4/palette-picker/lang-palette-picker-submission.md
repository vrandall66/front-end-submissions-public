# Palette Picker Submission Form

[Project Spec](http://frontend.turing.io/projects/palette-picker.html)

# Basics

#### Link to the GitHub Repository for the Project
[palette-picker](https://github.com/francylang/palette-picker)

#### Link to the Deployed Application
[heroku](https://lang-palette-picker.herokuapp.com/)

#### Link to your annotated server file
[annotated server file](https://github.com/francylang/palette-picker/blob/annotated-server/server.js)

## Completion

#### Were you able to complete the base functionality?
Missing:~~Folder names must be unique (you should not be able to create two folders with the same name), annotated server.js file, testing- not fully tested, yet~~
~~I ran out of time.~~

Yes

#### Which extensions, if any, did you complete?
* User can edit the hex code in the aside palette and update to the new color. 

# Code Quality

#### Link to a specific block of your code on GitHub that you are proud of
[happy code](https://github.com/francylang/palette-picker/blob/master/public/js/scripts.js#38-47)
* I like this piece of code because I broke out the logic for the append and fetch palettes function. This eliminated nested fetch calls within the fetch projects function. 

#### Link to a specific block of your code on GitHub that you feel not great about
[sad code](https://github.com/francylang/palette-picker/blob/master/public/js/scripts.js#126-142)

* I would like to see if there is a way to check for duplicates within my main project fetch/post instead of doing two fetch calls to projects. I haven't had success, yet. I am not able to figure out how to get the response and then make the post if there are not duplicates without fetching again. 

#### Attach a screenshot or paste the output from your terminal of the result of your test-suite running.

[test suite](![image](https://user-images.githubusercontent.com/24443103/33521830-6882d1d8-d79a-11e7-8c19-93bc853bef7e.png))

#### Link to Design Inspiration
http://palettab.com/
* I really liked the horizontal color block aside, so I used that to ground my application and build the UI from there. 

#### Please feel free to ask any other questions or make any other statements below!

* I've seen how done is used in testing, but I am not exactly sure where it comes from and why it some times causes my test suite to timeout. 

-----


# Instructor Feedback (Brittany)

## Specification Adherence

**58 points**: (50 possible points) No approach was taken that is counter to the spirit of the project and its learning goals. There are no features missing from above that make the application feel incomplete or hard to use. Data persists on refresh using a knex/postgreSQL database.

* Nice implementation of the extension - but the UI for it is a little funky. Would like some visual indicator that you can edit that hex code value. (Maybe a little 'edit'/'pencil' icon?). Additionally, if I make the HEX value white, I lose the ability to see the HEX value text. Would be good to change that text to a dark color when white is the chosen color.


## User Interface

**x points**: (20 possible points)

* I like the vertical layout of the colors for each palette but on my screen it cuts off after the 4th one and I have to scroll down to see the 5th color. Would be nice to set a `height: 100%` on the containing element here to ensure it's always the height of a user's screen no matter what size their browser is.

* I'm seeing a weird bug where the 5th color stays in place (even when it's not locked). When I click on a pre-existing palette, the 5th color doesn't change.

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
