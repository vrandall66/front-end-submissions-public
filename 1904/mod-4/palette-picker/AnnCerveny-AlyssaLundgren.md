# Palette Picker Submission Form

 [Project Spec](http://frontend.turing.io/projects/palette-picker.html)

## Basics

#### Links
 - [BE GitHub Repository](https://github.com/lundgrea/PalettePicker-BE)
 - [BE Heroku](https://palette-picker-be-ac.herokuapp.com)
 - [FE Github Repository](https://github.com/lundgrea/PalettePicker-FE)
 - [FE Heroku](https://happy-little-palette-picker.herokuapp.com)

## Completion

#### Were you able to complete the base functionality?
We were able to complete the base functionality of the back-end application. The front-end application has functionality including adding and deleting to the database without pageload. The application's FE does not integrate PATCH functionality on the DOM, however, the endpoints are fully set-up and capable.

 #### Links:
 - [Wireframes](https://user-images.githubusercontent.com/38546045/67012212-89fe5d80-f0e0-11e9-88e7-73fe4b63435f.jpeg) 
 - [DTR](https://gist.github.com/lundgrea/db6a74a9495e3eeb96690a5c36ea7dae)
 - [FE Github Project Board](https://github.com/lundgrea/PalettePicker-FE/projects/1)
 - [BE Github Project Board](https://github.com/lundgrea/PalettePicker-BE/projects)
 
 #### Which extensions, if any, did you complete?
 - N/A

 ## Code Quality

 #### Link to a specific block of your code on GitHub (from either repository) that you are proud of
[happy code](https://github.com/lundgrea/PalettePicker-BE/blob/c2a501d13c8ee66adc665532a9d672c37491e835/app.js#L53-L61)

 * Why were you proud of this piece of code?  
 
Our team is thrilled to have created a functioning backend, and more specifically, a dynamic function that gives a front-end developer using our API what they need to maneuver the app. We were able to think through the needs of the developer and expose an API endpoint that returns the palettes of a specififed folder based on the folder ID. Our source of pride on this piece of code comes from piecing together what we learned in class and reaching outside of that to create a truly useful endpoint.  
 
 #### Link to a specific block of your code on GitHub that you feel not great about
[sad code](https://github.com/lundgrea/PalettePicker-FE/blob/20f9e6637c537c0134b5cb4be48d7bc0b3e2828e/src/Components/App/App.js#L125-L135)

 * Why do you feel not awesome about the code? What challenges did you face trying to write/refactor it?
 
There are lots of things to be proud of in this project. Our team worked together well, communicated effectively, and implemented a working application. Unfortunately, we were unable to utilize all of our API endpoints. Eventually, our team had to make a strategic decision on how best to allocate time. We were happy with creating the backend patch requests, apiCalls asyncronous functions, and app-level implementation, but were unable to connect it on the DOM-level. These projects require priotitization and this is one of those instances. We've created a set of issues in GitHub for this reason.

 #### Link to Design Inspiration

 - [Our project design inspiration](https://user-images.githubusercontent.com/38546045/67012064-44da2b80-f0e0-11e9-9625-7a84a8ac459d.png) - Besides the obvious inspiration of Mr. Bob Ross, our team also drew inspiration from the attached project comp that utilizes transparency over imagery. We utilized this feature in our project. 

 #### Reflection on New Concepts

 * Describe your thoughts on server-side testing
 
 Server side testing was a pleasure. The syntax of the testing is friendly and you are able to easily query the database directly to create "mock data" and then utilize those results to create expectations. It was great to be able to easily test both happy and sad paths. 
 
 * Describe your thoughts on TravisCI - 
 
 TravisCI seems like a very useful tool. It is great to have a failsafe in place to run your test suite prior to deployment. Thank you for this lesson.
 
 * Describe your thoughts in creating a single project whose codebase was distributed across multiple repositories - 
 
The project was very interesting in terms of connecting the BE and FE repositories. It was particularly interesting to be in charge of the way that data is served up to the front end. The project gave a great full-picture view of application development. It was nice to have two repositories and clear responsibilities between each. 

#### Please feel free to ask any other questions or make any other statements below!

 Anything else you wanna say!

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
