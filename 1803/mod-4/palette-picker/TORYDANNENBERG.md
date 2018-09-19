# Palette Picker Submission Form
 [Project Spec](http://frontend.turing.io/projects/palette-picker.html)
 # Basics
 #### Link to the GitHub Repository for the Project
[palette-picker](https://github.com/tdberg21/palette-picker)
 #### Link to the Deployed Application
[heroku](https://palette-picker-td.herokuapp.com/)
 #### Link to your annotated server file
[annotated server file](https://github.com/tdberg21/palette-picker/blob/server-comments/server.js)
 ## Completion
 #### Were you able to complete the base functionality?
 Yes.
 #### Which extensions, if any, did you complete?
 None.
 # Code Quality
 #### Link to a specific block of your code on GitHub that you are proud of
happy code- scripts lines 134-139:
```const fetchSavedProjects = async () => {
  const url = '/api/v1/projects/';
  const response = await fetch(url);
  const results = await response.json();
  return results;
};```
 I think it shows the growth of my comfort with coding throughout Turing. In mod1 my functions were usually much longer and handled multiple tasks but I was much more successful in writing DRY SRP functions. 
 #### Link to a specific block of your code on GitHub that you feel not great about
sad code- scripts lines 75-79:
```<div class="mini-color-boxes mini-color-box1" style="background-color: ${colors[0]}" title="${colors[0]}"></div>
      <div class="mini-color-boxes mini-color-box2" style="background-color: ${colors[1]}" title="${colors[1]}"></div>
      <div class="mini-color-boxes mini-color-box3" style="background-color: ${colors[2]}" title="${colors[2]}"></div>
      <div class="mini-color-boxes mini-color-box4" style="background-color: ${colors[3]}" title="${colors[3]}"></div>
      <div class="mini-color-boxes mini-color-box5" style="background-color: ${colors[4]}" title="${colors[4]}"></div>```
      
It is very repetitive and just looks ugly. I am sure it could be refactored using an array prototype but I did not have enough time.
 #### Attach a screenshot or paste the output from your terminal of the result of your test-suite running.
 test suite:
``` Palette Picker is running on 3000.
  Client Routes
    ✓ should return the homepage
    ✓ should not return the homepage if the wrong url is entered
   API Routes
    GET /api/v1/projects
Seeding complete!
      ✓ should return the all the projects
    GET /api/v1/palettes
Seeding complete!
      ✓ should return the all the palettes
    GET /api/v1/projects/:id
Seeding complete!
      ✓ should return a single project
Seeding complete!
      ✓ should not return a project if it doesnt exist
    GET /api/v1/palettes/:id
Seeding complete!
      ✓ should return a single palette
Seeding complete!
      ✓ should not return a palette if it doesnt exist
    POST /api/v1/projects/new
Seeding complete!
      ✓ should create a new project
Seeding complete!
      ✓ should not create a project with missing data
    POST /api/v1/palettes/new
Seeding complete!
      ✓ should create a new palette
Seeding complete!
      ✓ should not create a palette with missing data
    DELETE /api/v1/palettes/delete/:id
Seeding complete!
      ✓ should delete a palette
   13 passing (917ms) ```
 #### Link to Design Inspiration
 [design inspiration](https://wdexplorer.com/20-examples-beautiful-css-typography-design/)
I really liked the look of the 'bold' theme typeface by Rafal Tomal. I think it looks really clean, so I used that as the typeface for my project. I also liked having everything in lowercase, and used that as well. I based my color scheme off of 'Classic Dark,' also from that article.
 #### Please feel free to ask any other questions or make any other statements below!
 It was more fun than I expected using jQuery again!
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
