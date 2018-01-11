
# Palette Picker Submission Form

[Project Spec](http://frontend.turing.io/projects/palette-picker.html)

# Basics

#### Link to the GitHub Repository for the Project
[palette-picker](https://github.com/alexbanister/palette-picker)

#### Link to the Deployed Application
[heroku](https://ahb-palette-picker.herokuapp.com/)

#### Link to your annotated server file
[annotated server file](https://github.com/alexbanister/palette-picker/blob/comments/server.js)

## Completion

#### Were you able to complete the base functionality?

* Functionality complete. Couldn't complete tests. I have happy and sad paths for GET, POST, and DELETE projects but couldn't get palette endpoint tests to work. I think I was having a problem with the primary keys of projects and palettes auto incrementing and seed not resetting it. Tried adding .truncate() to the .del() in test seed file but psql won't let me do that. I tried .raw('ALTER SEQUENCE id RESET WITH 1') or something along those lines but also didn't work.

#### Which extensions, if any, did you complete?

* None, but I did add a random name suggestion to palettes and projects sort of the way repl does.

# Code Quality

#### Link to a specific block of your code on GitHub that you are proud of
[happy code](https://github.com/alexbanister/palette-picker/blob/df99d3388b24b379f1208f903adec0bb52764c17/src/index.js#L99-L116)

* Building DOM elements seems to always get super messy. This function is a bit longer than I'd like and there is a bit more complexity than I like but I'm happy with it's cleanliness and readability.

#### Link to a specific block of your code on GitHub that you feel not great about
[sad code](https://github.com/alexbanister/palette-picker/blob/df99d3388b24b379f1208f903adec0bb52764c17/src/index.js#L147-L165)

* This function kept growing as I developed and got messy, hard to read and does too much.

#### Attach a screenshot or paste the output from your terminal of the result of your test-suite running.
<img width="753" alt="screen shot 2017-12-01 at 11 59 15 am" src="https://user-images.githubusercontent.com/17756439/33498598-316c1968-d68f-11e7-95f4-12997a4f270a.png">

#### Link to Design Inspiration

[Inspiration](https://dribbble.com/shots/2761157-Brisk-Mate-Branding-Guidelines-Color-Pallete)

* I liked the "droplet" color dots and thought they would be a nice way to show colors and how they interact with the palette. the rest of the design was build around that.

#### Please feel free to ask any other questions or make any other statements below!

* Test seems better than DOM testing but still a bit squirrelly and I don't really understand how to debug tests and how to make them work consistently. 

-----


# Instructor Feedback (Brittany)

## Specification Adherence

**55 points**: (50 possible points) No approach was taken that is counter to the spirit of the project and its learning goals. There are no features missing from above that make the application feel incomplete or hard to use. Data persists on refresh using a knex/postgreSQL database.

## User Interface

**17 points**: (20 possible points) User interface is mostly intuitive, though the instructor might need some guidance on interactions. Styling is mostly consistent, but could use some clean up.

* It feels a little difficult to tell that I'm saving a palette to a particular project -- I would maybe add that project drop down or 'current project' text somewhere closer to the 'Save Palette' button.

* I appreciate the logic that goes into showing the little teardrop-shaped colors on top of each background color for the palette, but it's a little more distracting than helpful. I also feel like 'Tt' might mean something significant but I wouldn't be able to guess exactly what. (I'm understand you're just demontrating text colors on background colors, but it's not super clear that's the intent.) I think you could incorporate the teardrop design in the thumbnails under the project sections rather than overlaying them on the larger background colors.

* Nice use of CSS transitions but I'd make them a little snappier. Subtlety is key with transitions and you want them to be just barely above the line of perception rather than something that's super obvious. (Kinda subliminal messaging. It will still have the intended effect of making DOM updates smoother, but it won't stand out as something users have to wait for to finish)

## Testing

**10 points**: (20 possible points) Project has a running test suite that tests some of the server-side endpoints but is missing many happy/sad paths

* [This](https://github.com/alexbanister/palette-picker/blob/master/test/routes.spec.js#L121-L130) block doesn't really tell me that the code did nothing if the ID didn't exist. I'd rather you send back a 404 and an error here that says a project with that ID does not exist and assert against that instead.

* At first glance, your code looks accurate for your test seed data. I can't imagine why the palette tests wouldn't be working out. You shouldn't have to do anything fancy in order to get those IDs to be hard-coded, consistent values other than setting them in your seed data, which you're doing. Ping me if you'd like to debug this together.

* You shouldn't need to comment out all [this](https://github.com/alexbanister/palette-picker/blob/master/test/routes.spec.js#L148-L165) code. `it.skip` should take care of that for you.


## Commented Server File

**10 points**: (10 possible points) Each line of the server file (on a separate branch) is commented and explains the code using precise, correct terminology and specificity

## JavaScript Style

**20 points**: (20 possible points) Application is thoughtfully put together with some duplication and no major bugs. Developer can speak to choices made in the code and knows what every line of code is doing. 

* Some weird spacing on this [line](https://github.com/alexbanister/palette-picker/blob/master/test/routes.spec.js#L39) around those parens

* If you're sending back a 204 status code, you shouldn't be sending back a [response body](https://github.com/alexbanister/palette-picker/blob/master/test/routes.spec.js#L135-L139). 204 means success, but there is no information I need to send back to the client.

* You can switch [this](https://github.com/alexbanister/palette-picker/blob/master/server.js#L10-L11) to triple equals rather than disabling the eslint rule. `!==` My bad.

* Adding the random name generator was a cool touch but I feel really confused about what you're doing [here](https://github.com/alexbanister/palette-picker/blob/master/server.js#L28-L35).

* Wasn't a requirement to be able to delete projects, but there's an easier way to do [this](https://github.com/alexbanister/palette-picker/blob/master/server.js#L59-L71). You can set a `cascade()` option in your migration when you set up your schema so that the delete automatically removes any dependent records from other tables.

* Be careful about misspellings [here](https://github.com/alexbanister/palette-picker/blob/master/server.js#L97). 'palette' not 'pallet'

* Use template strings [here](https://github.com/alexbanister/palette-picker/blob/master/src/index.js#L28-L29) and [here](https://github.com/alexbanister/palette-picker/blob/master/src/index.js#L31) rather than concatenating with the plus sign.

* You're creating this selector twice [here](https://github.com/alexbanister/palette-picker/blob/master/src/index.js#L28-L29) which is expensive for jQuery because it has to traverse the DOM and find it more than once. You can chain these css properties by doing:

```js
  $('.color'+position).css({ 
    'background': color,
    'color': color
  });
```

* Can you put a class or ID on these [elements](https://github.com/alexbanister/palette-picker/blob/master/src/index.js#L49) so you don't have to find the closest `data-id`? This line is a little hard to read as-is.

* Ahhhh [this](https://github.com/alexbanister/palette-picker/blob/master/src/index.js#L99-L116) is a little unruly. You're also doing these DOM manipulations in a loop which is a significant performance suck. You want to use Document Fragments instead to build up all the HTML you need and append to the DOM once rather than on each iteration of the loop.

* You could pass both of [these](https://github.com/alexbanister/palette-picker/blob/master/src/index.js#L133-L134) classes as a string like `'.save-palette-area, .crate-project-area'` and your clearLoading function will take care of both of those at once.

* Lots of duplicate code on [these lines](https://github.com/alexbanister/palette-picker/blob/master/src/index.js#L138-L143), you'd be better off dynamically inserting the slideDown/Up methods and disabled values so you don't have to keep creating this jQuery selector on 4 separate lines.

* Make sure to be consistent with your naming conventions e.g. [savePalette](https://github.com/alexbanister/palette-picker/blob/master/src/index.js#L147) and [createProject](https://github.com/alexbanister/palette-picker/blob/master/src/index.js#L167) should either both be save or both be create.

* Are you posting multiple projects [here](https://github.com/alexbanister/palette-picker/blob/master/src/index.js#L171)? Or just one? If it's just one at a time, rename this to `postProject`. It's better not to use words like post at all though, as they're not as meaningful as save and create.

* What's with all the [single-line fetch requests](https://github.com/alexbanister/palette-picker/blob/master/src/api.js)? These are really long and hard to read. Line-lengths should be max 80 characters. Give your code some room to breathe between the .thens and catches.

## Workflow

**17 points**: (20 possible points)

* What is [this](https://github.com/alexbanister/palette-picker/commit/e690ce4ca054195fbb4fbbf6dcbba36560bb2bd7#diff-b085d5d01dd304cf7db21c04c08e7b43)? A bundle file? `javascript.js`? Bundle files shouldn't be committed to github. They change on the fly along with any other changesets and will cause a nightmare of merge conflicts when you're working with multiple people. You'd want to put this in your .gitignore file and tell Heroku to run a build to generate that file on the fly. Also clutters up your git commit history making changesets difficult to read.

* You don't have to file PRs on a project when you're working by yourself. You should still be using branches, but PRs are for code review.

* Commits seem like they contain mostly relevant changesets, but diffs like [this](https://github.com/alexbanister/palette-picker/commit/27de43178bbc675a35a652bfb3b1968c22bc10c1) are a little large. You should probably have no less than 100 commits on a project this size, so I'd get in the habit of trying to commit more frequently with less changes.


### To get a 3 on this project, you need to score 120 points or higher
### To get a 4 on this project, you need to score 140 points or higher

# Final Score: 129 / 160
