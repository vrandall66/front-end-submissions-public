# Palette Picker Submission Form

[Project Spec](http://frontend.turing.io/projects/palette-picker.html)

# Basics

#### Link to the GitHub Repository for the Project
[palette-picker](https://github.com/danalvarez5280/Palette-Picker)

#### Link to the Deployed Application
[heroku](https://palette-picker-alvarez2.herokuapp.com/)

#### Link to your annotated server file
[annotated server file](https://github.com/danalvarez5280/Palette-Picker/blob/master/server.js)

## Completion

#### Were you able to complete the base functionality?

I believe I was able to complete everything aside from diplaying the hexcodes when you click on a palette name. I wrote the tests, however I am having trouble with two of them failing for some odd reason.

#### Which extensions, if any, did you complete?

N/A

# Code Quality

#### Link to a specific block of your code on GitHub that you are proud of
[happy code](https://github.com/danalvarez5280/Palette-Picker/issues/13)

* I was happy with this code, mainly because it was the last thing I did and it worked pretty much right away. I was also about to grab the id i needed for the delete fetch functionality quickly.

#### Link to a specific block of your code on GitHub that you feel not great about
[sad code](https://github.com/danalvarez5280/Palette-Picker/issues/14)

* I dont really know that I understand the premise of the seed when it comes to the testing. I feel like I was supposed to set up a seed/test file but I am not really sure. My tests are apssing for the most part but there are two that either have an issue with what I'm sending to the endpoint or what is being returned by the end point.

#### Attach a screenshot or paste the output from your terminal of the result of your test-suite running.

![My Testing Suite](https://user-images.githubusercontent.com/26985984/31293469-8601ba9a-aa94-11e7-9df1-30b180bb2677.png)
![My testing suite errors](https://user-images.githubusercontent.com/26985984/31293493-99321d9e-aa94-11e7-990b-d2d8762511af.png)

#### Please feel free to ask any other questions or make any other statements below!

I feel bad that I did not finish what should be a roughly simple aspect of the project. As well I lost too much time to a stupid mistake. I was running my app on my file path instead of localhost:300. As well I feel like I woud like to know about the testing a bit more. I was able to get most all to pass, but it bothers me why I'm getting 422 errors and 500 errors no matter what I change in the test file or server.js file.

-----


# Instructor Feedback (Brittany)

## Specification Adherence

**x points**: Lorem ipsum dolor set amet

## User Interface

**x points**: Lorem ipsum dolor set amet

## Data Persistence with SQL Database

**20 points**: The application persists data in a SQL database with correct relationships between folders and URLs.

## Testing

**x points**: Lorem ipsum dolor set amet

## JavaScript Style

**x points**: Lorem ipsum dolor set amet

## Workflow

**10 points**: Developer(s) make large, inconsistent commits that contain irrelevant changesets and make it difficult to follow the evolution of the application. Developer(s) rarely use git branches and frequently incorporate changes directly into master with little or no review process. There are instances of committed source code that should be .gitignored and instances of dead code and/or debugger statements.

* Without even looking into any of your commits, I can tell you don't have enough and that each of them will be doing too much work and have difficult diffs to read. There's no hard and fast rule for how many commits you should have, but for a project of this size and scope, I'd expect no less than 100.

* Commit messages like [this](https://github.com/danalvarez5280/Palette-Picker/commit/256e358a8dc6112f0225c2a4b1c715181f06f42c) are too long and verbose. They should be written in the imperative tense and less than 80 characters. [This](https://chris.beams.io/posts/git-commit/) is a good post to follow for writing commit messages. Many of yours are too vague to be helpful. Like [this one](https://github.com/danalvarez5280/Palette-Picker/commit/7b207942f9d6ada4704b9a41cb7c08b508e9f6f7)

* Node modules made it into the repo, as well as some instances of [commented out code](https://github.com/danalvarez5280/Palette-Picker/commit/990d677f6e766f2bca5a365f432ba40e4bd4d845). You can use `git stash` to hide changes that you don't want to commit yet and pop them back on when you want them back with `git stash pop`. 


### To get a 3 on this project, you need to score 120 points or higher
### To get a 4 on this project, you need to score 140 points or higher

# Final Score: x / 160
