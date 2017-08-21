+# Jet Fuel Submission Form
 +
 +[Project Spec](http://frontend.turing.io/projects/jet-fuel.html)
 +
 +# Basics
 +
 +#### Link to the Github Repository for the Project
 +[jetfuel](https://github.com/noetic97/jet-fuel)
 +
 +#### Link to the Deployed Application
 +[heroku](https://joes-jet-fuel.herokuapp.com/)
 +
 +#### Link to your annotated server file
 +[annotated server file](https://github.com/noetic97/jet-fuel/blob/server-descriptions/server.js)
 +
 +## Completion
 +
 +#### Were you able to complete the base functionality?
 +
 +Mostly.  You can not filter the links by date and the date is not showing next to the links.  I underestimated the time it would take to complete the testing, and did not finish implementing all the UI.
 +
 +#### Which extensions, if any, did you complete?
 +
 +* All of the client-side interactions are tested
 +
 +# Code Quality
 +
 +#### Link to a specific block of your code on Github that you are proud of
 +[happy code](https://github.com/noetic97/jet-fuel/blob/master/test/routes.spec.js)
 +Line 250-258
 +``` response.body.map((link) => {
 +          link.should.have.property('id')
 +          link.should.have.property('description')
 +          link.should.have.property('ogURL')
 +          link.should.have.property('shortURL')
 +          link.should.have.property('folder_id')
 +          link.should.have.property('created_at')
 +          link.should.have.property('updated_at')
 +        })```
 +
 +* It was a simple solution to testing multiple links without having to test each link by hand.  I wasn't sure if it was possible to map and then test over each result, but it worked right away!
 +
 +#### Link to a specific block of your code on Github that you feel not great about
 +[sad code](https://github.com/noetic97/jet-fuel/tree/master/db/migrations)
 +
 +* I do not like having these accidental migrations that now throw warnings in my test results.
 +
 +#### Attach a screenshot or paste the output from your terminal of the result of your test-suite running.
 +
 +[test suite]
 +```Client Routes
 +    ✓ Should return the home page with text (38ms)
 +
 +  API Routes
 +    GET /api/v1/folders
 +Knex:warning - migration 20170818120129_initial.js did not return a promise
 +Knex:warning - migration 20170818120143_initial.js did not return a promise
 +Knex:warning - migration 20170820002113_add.js did not return a promise
 +      ✓ Should return all folders in the DB
 +    POST /api/v1/folders
 +      ✓ Should add a new folder to the DB
 +      ✓ SAD PATH - Should return an error message if the folder is missing title
 +      ✓ SAD PATH - Should not allow a user to add a folder if it already exists
 +    GET /api/v1/folders/:id
 +      ✓ Should return a specific folder in the DB
 +      ✓ SAD PATH - Should return an error message when an improper id is passed in
 +    GET /api/v1/links
 +      ✓ Should return all links in the database
 +    POST /api/v1/links
 +      ✓ Should add a new link to an existing folder
 +      ✓ SAD PATH - Should return an error message when an improper parameter is passed in
 +    GET /api/v1/folders/:id/links
 +      ✓ Should return all of the links to a specified folder
 +
 +
 +  11 passing (368ms)```
 +
 +#### Please feel free to ask any other questions or make any other statements below!
 +
 +Anything else you wanna say!
 +
 +-----
 +
 +
 +# Instructor Feedback (Instructor Name)
 +
 +## Specification Adherence
 +
 +**x points**: Lorem ipsum dolor set amet
 +
 +## User Interface
 +
 +**x points**: Lorem ipsum dolor set amet
 +
 +## Data Persistence with SQL Database
 +
 +**x points**: Lorem ipsum dolor set amet
 +
 +## Testing
 +
 +**x points**: Lorem ipsum dolor set amet
 +
 +## JavaScript Style
 +
 +**x points**: Lorem ipsum dolor set amet
 +
 +## Workflow
 +
 +**x points**: Lorem ipsum dolor set amet
 +
 +
 +### To get a 3 on this project, you need to score 110 points or higher
 +### To get a 4 on this project, you need to score 135 points or higher
 +
 +# Final Score: x / 150
