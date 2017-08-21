# Jet Fuel Submission Form

[Project Spec](http://frontend.turing.io/projects/jet-fuel.html)

# Basics

#### Link to the Github Repository for the Project
[jetfuel](https://github.com/buji405/jet-fuel)

#### Link to the Deployed Application
[heroku](https://ciaras-jetfuel.herokuapp.com/)

#### Link to your annotated server file
[annotated server file](https://github.com/buji405/jet-fuel/blob/0a0fa18239f2247b0140f385fb6c11120b26c690/backend/server.js)

## Completion

#### Were you able to complete the base functionality?

If not, explain what is missing and why.

Yes, there is a known bug though with validating the url. 
If I add a invalid link it will append it to the dom as undefined, but if you refresh 
it goes away and never adds to the database. I looked a hundred times at why the catch 
isn't blocking it from appending but can't figure it out. Everything seems to be in place. 

Also I did add a delete method which wasn't required but it only deletes the folders if there is nothing in them. 

#### Which extensions, if any, did you complete?
didn't get that far

# Code Quality

#### Link to a specific block of your code on Github that you are proud of
[happy code]()
$(e.target).parent().find(".drop-down").toggleClass("show") 
$('.info-wrapper').empty()

* Why were you proud of this piece of code?
because it took me forever to target this and get the toggle going. was exciting when it finally worked! 
Also the second line because I had a problem for a long time where everytime I clicked the folder it was 
duplicating all the links, took a long time to figure out what I needed to clean to get it to not duplicate. 

#### Link to a specific block of your code on Github that you feel not great about
[sad code]()
appendInfo(res.origURL, res.description, parentElement, res.shortURL, res.id, res.created_at)

* Why do you feel not awesome about the code? What challenges did you face trying to write/refactor it?
I don't like all the things I'm having to pass through. I think I could have just passed res and parentelement 
but when I tried doing this it was breaking everywhere so I think I just would need more time to figure out all the 
places to change everything. 

#### Attach a screenshot or paste the output from your terminal of the result of your test-suite running.

[test suite]()
<img width="1038" alt="screen shot 2017-08-20 at 10 31 41 pm" src="https://user-images.githubusercontent.com/18603030/29503701-74be8d74-85f7-11e7-867d-6301ae206630.png">

#### Please feel free to ask any other questions or make any other statements below!

Anything else you wanna say!

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


### To get a 3 on this project, you need to score 110 points or higher
### To get a 4 on this project, you need to score 135 points or higher

# Final Score: x / 150
