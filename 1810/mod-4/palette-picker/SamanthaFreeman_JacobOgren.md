# Palette Picker Submission Form

 [Project Spec](http://frontend.turing.io/projects/palette-picker.html)

 # Basics

 #### Link to the GitHub Repository for the BE
[palette-picker BE](https://github.com/jogren/palette-picker-api)

 #### Link to the Deployed BE
[heroku BE](https://palette-picker-api-sfjo.herokuapp.com/)

 #### Link to the GitHub Repository for the FE
[palette-picker FE](https://github.com/jogren/palette-picker)

 #### Link to the Deployed FE
[heroku FE](http://palette-picker-sfjo.herokuapp.com/)

 ## Completion

 #### Were you able to complete the base functionality?

 Yes, we were able to complete the base functionality.

 #### Link to an image of your wireframe(s)
[FE Wireframe](https://user-images.githubusercontent.com/19739235/66968431-68e72f80-f042-11e9-8bb7-d8a16743d727.png)

 #### Which extensions, if any, did you complete?
 - Implemented TravisCI for your front-end repository
 - The user is able to update an existing palette and change any or all of the colors in the database with a PATCH.
 
 # Code Quality

 #### Link to a specific block of your code on GitHub (from either repository) that you are proud of
[happy code](https://github.com/jogren/palette-picker/blob/378d1b7c97bb9babdb7cb870fa6ce604ebbcfb37/src/App/App.js#L74-L86)

 * Why were you proud of this piece of code?  
- Lines 74-86: On one hand, this was one of our first use cases of a patch request. Further, we were faced with restructuring the palette and found a creative solution to manipulate our data.

 #### Link to a specific block of your code on GitHub that you feel not great about
[sad code](https://github.com/jogren/palette-picker-api/blob/cac41a9ef63be19a377ee748066d889ea123e4c4/app/app.js#L33-L52)

 * Why do you feel not awesome about the code? What challenges did you face trying to write/refactor it?
- Lines 33-52: We both agreed that this was a lengthy function which is in need of a refactor. We believe that our if and else if could be combined to save lines.

 #### Link to Design Inspiration

 * Show us what you used as design inspiration (another color picker site, a dribbble UI element, a user flow, etc.) and explain what you stole from it  
[Links Inspiration](https://user-images.githubusercontent.com/45364533/66968119-d3976b80-f040-11e9-9f45-cbaf98217ca3.png)    
- We liked the contrast of the white links for active vs. the gray for inactive. In addition, felt like the look of just text looked very clean and not as cluttered.

[Background Color Inspiration](http://coleweber.com/)
- The background color for this site really drew us in. It makes the white and orange of their logo pop, so we wanted to incorporate this same color scheme for our background color.

[Palette Inspiration](https://user-images.githubusercontent.com/45364533/66968237-54eefe00-f041-11e9-9e29-2fc09dd95321.png)
- Specifically the look of palettes next to each other, so you as the user could see how the colors actually work together. In addition, we liked a similar style for the smaller palettes. However, we ended up tweaking this look, so the palettes were shorter. This was because we felt the size of Adobe's palettes made it feel a bit cramped.

 #### Reflection on New Concepts

 * Describe your thoughts on server-side testing  
- It's definitely easier than front-end testing, and after the first few they quickly became manageable. We were very thankful for the in depth lesson, and feel as if it set us up for success.
* Describe your thoughts on TravisCI  
- We struggled a lot in the beginning, especially through the backend, but had much more success deploying the frontend. We even were able to get our badges displayed on the README. We agree that they're are various benefits, but it can be frustrating waiting for all the tests to run when you're trying to approve a PR right after it was opened.
* Describe your thoughts in creating a single project whose codebase was distributed across multiple repositories
- As our first full-stack project, it was a little strange being the architect of the API, and at times, it was unclear where data manipulation should occur. 
#### Please feel free to ask any other questions or make any other statements below!

- We'd like a bit explanation on the comment above. It seems like there are situations in which features could be implemented by the backend or frontend. For instance, we were unsure if we should add the foreign key to the POST request body or should the database find the foreign key.

 -----


 # Instructor Feedback (Instructor Name)

 ## Specification Adherence

 **x score**: 

 ## User Interface

 **x score**: 

 ## Testing

 **x score**: 

 ## Workflow

 **x score**: 

 # Outcome: pass/fail
