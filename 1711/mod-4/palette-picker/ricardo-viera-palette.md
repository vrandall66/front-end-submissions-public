# Palette Picker Submission Form

[Project Spec](http://frontend.turing.io/projects/palette-picker.html)

# Basics

#### Link to the GitHub Repository for the Project
[palette-picker](https://github.com/rvwatch/palette-picker)

#### Link to the Deployed Application
[heroku](https://palettesofpickers.herokuapp.com/)

#### Link to your annotated server file
[annotated server file](https://github.com/rvwatch/palette-picker/blob/master/server.js)

## Completion

#### Were you able to complete the base functionality?

If not, explain what is missing and why.
My tests are not running. I'm not sure why yet, but I suspect I messed something up with my environment variables. 

#### Which extensions, if any, did you complete?

# Code Quality

#### Link to a specific block of your code on GitHub that you are proud of
[happy code](https://github.com/rvwatch/palette-picker/blob/f2ca77394273f1f9b781a97bc8e2b3fa7f5a444c/db/migrations/20180607110919_initial.js#L19)      
snippet `table.foreign('project_id').references('projects.id').onDelete('CASCADE');`
* Why were you proud of this piece of code?  
because the issue it solved stopped me dead in my tracks... I thought I'd have to rebuild my entire DB from scratch. This code was a huge relief to find. 

#### Link to a specific block of your code on GitHub that you feel not great about
[sad code](https://github.com/rvwatch/palette-picker/blob/f2ca77394273f1f9b781a97bc8e2b3fa7f5a444c/public/js/scripts.js#L9-L26)       

* Why do you feel not awesome about the code? What challenges did you face trying to write/refactor it?  
I tried for a while to figure out a way to convert rgb to hexidecimal. In the end I had to copy/paste this solution and it stands out like a sore thumb in my code.
Everything else I wrote might be ugly, but at least I wrote it. This was a necessary evil for now. Until I become regexPERT! Maybe... 

#### Attach a screenshot or paste the output from your terminal of the result of your test-suite running.

Test results: 

`API tests      

    ✓ should GET all the projects   
    ✓ should GET all the palettes   
    ✓ should POST a new project to the database    
    ✓ should THROW a 422 if no params are sent     
    ✓ should POST a new palette to the database    
    ✓ should THROW a 422 if no params are sent     
    ✓ should DELETE a project from the DB      
    ✓ should not DELETE a project if ID does not exist      
    ✓ should DELETE a palette from the DB       
    ✓ should not DELETE a palette if ID does not exist   
    
  10 passing (1s)`

[test suite](https://github.com/rvwatch/palette-picker/blob/master/test/routes.spec.js)

#### Link to Design Inspiration

[inspiration](https://dribbble.com/shots/1616186-IMDB-Concept-Hero)

* I liked the subtle gradient and use of darker colors and muted whites for the tabs. 
I also used the slightly transparent borders on the buttons. 

#### Please feel free to ask any other questions or make any other statements below!

Anything else you wanna say!

Obviously a huge thanks for letting me return to this project and the time extension. I ended up getting really into this 
project once I started to pull it apart. It's one of my favorite "default" projects and I'll be featuring it on my portfolio
in the short term. 

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
