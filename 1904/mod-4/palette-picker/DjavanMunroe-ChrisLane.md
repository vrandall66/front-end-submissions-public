# Palette Picker Submission Form

 [Project Spec](http://frontend.turing.io/projects/palette-picker.html)

 # Basics

 #### Link to the GitHub Repository for the BE
[palette-picker BE](https://github.com/djavanm/color-picker-api)

 #### Link to the Deployed BE
[heroku BE](https://color-picker-api.herokuapp.com/)

 #### Link to the GitHub Repository for the FE
[palette-picker FE](https://github.com/CLLane/color-picker-ui)

 #### Link to the Deployed FE
[heroku FE](https://color-picker-ui.herokuapp.com/)

 ## Completion

 #### Were you able to complete the base functionality?

 Cheers. We were able to complete the base functionality.

 #### Link to an image of your wireframe(s)
- On GitHub FE repository

 #### Which extensions, if any, did you complete?
 
 - N/A

 # Code Quality

 #### Link to a specific block of your code on GitHub (from either repository) that you are proud of
[Recursive Hex Code generator](https://github.com/CLLane/color-picker-ui/commit/92b0dca5a3f07afbfba2ca3fdf99402ab43213ff)

 * Why were you proud of this piece of code?  
- Lines 17-27: We wanted to implement a recursive function into our project, and thought this woudld be a good place. And it is one of the pillars of our project.

 #### Link to a specific block of your code on GitHub that you feel not great about
[sad code](https://github.com/CLLane/color-picker-ui/commit/d7e8b580c218c5eb5a096964568586cba871186b)

 * Why do you feel not awesome about the code? What challenges did you face trying to write/refactor it?
- Lines 56-59 of Project Form: We needed a way to disable our Save button, so we have a boolean being assigned to an || statement, followed by an if statement that will flip that same value under another condition.  
This was challenging because we only wanted to disable the save button in two seperate cases. One case is if they were creating a new project, we would need a Project Name plus Palette Name, but if they were adding to an existing project, then we would need a Palette Name only.
 #### Link to Design Inspiration
City life. 
 * Show us what you used as design inspiration (another color picker site, a dribbble UI element, a user flow, etc.) and explain what you stole from it  
[design inspiration](https://coolors.co/defffc-e2e4f6-e7c8dd-dbafc1-86626e)    
We chose to do more of a graffiti spin on this website.

 #### Reflection on New Concepts

 * Describe your thoughts on server-side testing  
- I wish all testing was server side testing.
* Describe your thoughts on TravisCI  
- Had some issues with the setup, but overall I can see how it would help in workflow.
* Describe your thoughts in creating a single project whose codebase was distributed across multiple repositories
- It was nice to break out each repo in regards to their responsibility.
#### Please feel free to ask any other questions or make any other statements below!

 N/A

 -----


 # Instructor Feedback (Leta)

 ## Specification Adherence

 **4**: 

 ## User Interface

 **3**: 

 ## Testing

 **4**: 

 ## Workflow

 **2**: 

 # Outcome: Pass
 
Notes:
 
- If something is hard to test, then it's time to refactor code 
- More specific error codes could be used (422, etc) in server
- UI could stand to be tweaked (error messages are hard to read, button text should have a bit more breathing room)
