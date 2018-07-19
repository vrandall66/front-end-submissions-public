# Palette Picker Submission Form

[Project Spec](http://frontend.turing.io/projects/palette-picker.html)

# Basics

#### Link to the GitHub Repository for the Project
[palette-picker](https://github.com/danielafcarey/palette-picker)

#### Link to the Deployed Application
[heroku](https://palettez.herokuapp.com/)

#### Link to your annotated server file
[annotated server file](https://github.com/danielafcarey/palette-picker/blob/master/server.js)

## Completion

#### Were you able to complete the base functionality?

Yes, except I commented my server file on the main branch instead of a separate branch (lol).

#### Which extensions, if any, did you complete?

# Code Quality

#### Link to a specific block of your code on GitHub that you are proud of
[happy code](https://github.com/danielafcarey/palette-picker/blob/master/test/routes.spec.js)

* Why were you proud of this piece of code?

I'm proud of these tests because it took me a while to get it figured out. While I was waiting for someone to answer my calls for help, I filled in the tests as I thought they should be, but could not run them. When I finally fixed my test configuration, THEY ALL PASSED!! I was super pumped that I had written them correctly without the ability to run them to check.

#### Link to a specific block of your code on GitHub that you feel not great about
[sad code](https://github.com/danielafcarey/palette-picker/blob/a17c9d8d1171203a4d29184c62c3682829340b39/server.js#L151)

* Why do you feel not awesome about the code? What challenges did you face trying to write/refactor it?

This feels like a gnarly method and so many nested callbacks - there is likely a better way to refactor but I felt time-crunched so I just made it work and didn't go back to it.

Also, I did not have time to do error handling or any try/catches on my fetch calls, so I'm not super proud of that.

#### Attach a screenshot or paste the output from your terminal of the result of your test-suite running.

Palette Picker is running on 3000
  client routes
    ✓ should receive a response of index.html when we hit the root endpoint
    ✓ should return a 404 for a route that does not exist

  api routes
    GET /api/v1/projects
Seeding complete!
      ✓ should return an array of projects
    GET /api/v1/projects/:id
Seeding complete!
      ✓ should return a specific project
Seeding complete!
      ✓ should return a 404 if the project was not found
    GET /api/v1/projects/:id/palettes
Seeding complete!
      ✓ should return an array of palettes for a specific project
Seeding complete!
      ✓ should return an empty array if no palettes match the project
    GET /api/v1/palettes/:id
Seeding complete!
      ✓ should return a palette object
Seeding complete!
      ✓ should return a 404 if no palette was found
    POST /api/v1/projects
Seeding complete!
      ✓ should add a project to the database (42ms)
Seeding complete!
      ✓ should not add a project if the correct params were not sent
    POST /api/v1/palettes
Seeding complete!
      ✓ should add a palette to the database
Seeding complete!
      ✓ should not add a palette if any params are missing
Seeding complete!
      ✓ should not add a palette if the project was not found
    DELETE /api/v1/palettes/:id
Seeding complete!
      ✓ should delete a palette from the database
Seeding complete!
      ✓ should send a 404 if the project was not found


  16 passing (2s)

#### Link to Design Inspiration

* Show us what you used as design inspiration (another color picker site, a dribbble UI element, a user flow, etc.) and explain what you stole from it

I mostly stole everything from Coolors and the project spec.

#### Please feel free to ask any other questions or make any other statements below!

Anything else you wanna say!

-----


# Instructor Feedback (Leta)

### Specification Adherence (out of 50 points): 50 points

* **50 points** - No approach was taken that is counter to the spirit of the project and its learning goals. There are no features missing from above that make the application feel incomplete or hard to use. Data persists on refresh using a knex/postgreSQL database.

Notes:

- Complete functionality in place
- See notes below for breakdown of possible improvements

### User Interface (out of 20 points): 18 points

* **20 points** - User interface is intuitive and the instructor can easily use it on their own without guidance. Styling is consistent and call-to-action elements are obvious. The application provides the user with relevant feedback based on interactions.  
* **15 points** - User interface is mostly intuitive, though the instructor might need some guidance on interactions. Styling is mostly consistent, but could use some clean up. Application may be missing some relevant feedback that would help guide the user.

Notes:

- The placement of the Create and New Project section is a little unintuitive
- When projects or palettes are created, the success indications are very small and subtle - could be called out a bit more to communicate success more clearly to the user
- At narrow screen widths, the hex codes in the main palette get squished
- The lock buttons are great
- Hover states on the buttons would be a nice bit of feedback for users

### Testing (out of 20 points): 20 points

* **20 points** - Project has a running test suite that tests every server-side endpoint with many happy and sad path cases.

Notes:

- It's better to put [this](https://github.com/danielafcarey/palette-picker/blob/77a4e314019b9fc3ebda1e6e415fa5eb87894801/test/routes.spec.js#L1) in your test script in the package.json: `NODE_ENV=test mocha --exit`
- [This](https://github.com/danielafcarey/palette-picker/blob/77a4e314019b9fc3ebda1e6e415fa5eb87894801/test/routes.spec.js#L12-L20) test could be fleshed out a bit - examine the HTML that is coming back to make sure it's the right page (that's a bit ouside the scope of this project, but a note for your capstone)
- I'm not sure what's going on in [this](https://github.com/danielafcarey/palette-picker/blob/77a4e314019b9fc3ebda1e6e415fa5eb87894801/test/routes.spec.js#L252) test - it looks like the project_id being provided is 1, not the 111 the test is expecting....
- Great coverage of sad path testing!

### Commented Server File (out of 10 points): 9 points

* **10 points** - Each line of the server file (on a separate branch) is commented and explains the code using precise, correct terminology and specificity

Notes:

 - The lines [here](https://github.com/danielafcarey/palette-picker/blob/77a4e314019b9fc3ebda1e6e415fa5eb87894801/server.js#L12-L13) more specifically allow knex to parse the body of a post request as json so you can  access and use the values stored within it.
 - The [catch here](https://github.com/danielafcarey/palette-picker/blob/77a4e314019b9fc3ebda1e6e415fa5eb87894801/server.js#L60) will trigger if the promise is rejected

### JavaScript Style (out of 30 points): 30 points

* **30 points** - Application has exceptionally well-factored code with little or no duplication and all components separated out into logical components. There _zero_ instances where an instructor would recommend taking a different approach.

Notes:

- Good organization

### Workflow (out of 20 points): 20 points

* **20 points** - Developer(s) make many small, atomic commits that clearly document the evolution of the application and do not contain irrelevant changesets that aren't reflected by the commit message. Commit messages are concise and consistent in syntax and tense. Developer(s) effectively use git branches and pull requests when applicable to incorporate changes into the application, and are not pushing directly to master. There are no instances where the developer(s) have committed source code that should be .gitignored. There are no instances of "dead" or commented-out code and debugger statements like console.log.

Notes:

- Really great work here

### Project is worth 150 points: 

### To get a 3 on this project, you need to score 110 points or higher

### To get a 4 on this project, you need to score 130 points or higher

# Final Score: 147 / 150
