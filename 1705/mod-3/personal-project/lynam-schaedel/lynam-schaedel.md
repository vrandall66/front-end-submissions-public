## Project Name: Do You. (where Personality meets Passion)

#### Contributors: Christie Lynam and Margo Schaedel

#### Check In: 1

#### Project Pitch: Application offering personality testing for high school and college students (can expand to include any demographic) to help guide them in making educational and career choices. Students will learn what kinds of jobs that people with their same personality type enjoy and are good at. They will also be able to share this personality info with friends on social media. Possibility to extend app to include compatibility in love, work, and friendships.

### Deliverables

#### Stack: React, Router, Redux, SAAS, (React Native for mobile?)

#### APIs: Traitify

#### Wireframes: [Do you homepage wireframe](https://www.dropbox.com/s/9jv1z6740j05de4/do-you-hompage.png?dl=0), additional screenshots in wireframes folder. Note: We will wireframe the assessment display as soon as we receive API key.

#### Waffle & Github: https://github.com/christielynam/do-you, https://waffle.io/christielynam/do-you

#### Order Of Attack: Get API set up, fetch personality test, display on route and design homepage UI, Be able to share with social media (facebook, twitter, instagram, linkedin). Login through facebook or google possibility. Possible extension: extend app to include love assessment compatibility, and friends compatibility.

#### MVP: Fetching personality test and results from Traitify API, and displaying info about that personality type (personal and career)

#### Nice To Haves: All of the extensions. And mobile!

#### Biggest Challenges: Once we have the api key, we will be able to better assess the hurdles we will face in this project.

### Instructor Notes

#### Deliverables for next checkin:

- have auth0 hooked up 
  (alternatively you can use passport as well)
- have initial call to api loading redux store 
  - have tests coming in 
- have backend started 
  - migration / user table created 
  - test score table created 
- start testing 
- have login view built

### Checkin 2

- Set up all file structue
- Build out multiple components
- Partial build out of backend server (HELP!)
- Initial fetch from API
- Configure store

### things to do 
 
 - write user to the database 
 - build out the scores results table 
 - build out front-end so that user can take a test. 
 - start testing the front-end
 - look into testing backend
 
 ### Checkin 3
 
 - started testing front-end
 - looked at backend testing examples
 - results table is built in postgres
 - login with users already created works (with database)
 - display assessment
 - display personalities
 - currently storing user's assessment progress in traitify
 
 ### things to do
 
 - add functionality to store the user's assessment id in results table in postgres
 - add multiple assessments
 - add results display
 - handle unfinished assessments when user returns to page
 - handle user must be logged in to take an assessment (redirect)
 - finish personalities display (animations)
 - add backend testing
