# FitLit
* Students: Noah & Chris
* Evaluator: Brittany

## Rubric

### Functional Expectations
* [ ] 4: Application fulfills all expectations of iterations 1 - 5 with no bugs or missing functionality *as well as* [ ] an extension.
* [x] 3: Application fulfills expectations of iterations 1 - 5 with no bugs or missing functionality.
* [ ] 2: Application is usable but has some missing functionality.
* [ ] 1: Application crashes during normal usage.

* Functionality in place/attempted for all 5 iterations, despite maybe missing some tests for iteration 5? 

### Fundamental JavaScript & Style
* [ ] 4: Application demonstrates excellent knowledge of JavaScript syntax, style, and refactoring.
* [x] 3: Class methods use array and object prototypes - `for` loops are not used in the application. Application shows strong effort towards organization, content, and refactoring. 
* [ ] 2: Class methods use a mix of array and object prototypes and `for` loops. Application runs but the code has long methods, unnecessary or poorly named variables, and needs significant refactoring.
* [ ] 1: Application generates syntax error or crashes during execution.

* You have a lot of method names that are either `getMinutesActive` or something like `returnMinutesActive` -- stick with the word get. You won't see functions with the word `return` in their name because it could get confusing if you ran into a scenario where you had to write something like `return returnAverageMinutes()` 

* I like the way you broke out your prototype methods in files like [this](https://github.com/chrisdbasham317/FitLit-Activity-Tracker/blob/master/src/Activity-repository.js) and assigned their results to variables. I think in this project it makes it way easier to keep track of what you're working with when you have these separate variables you've been creating, rather than chaining all your methods together.

* Looks like you got great practice in with your prototype methods. [This](https://github.com/chrisdbasham317/FitLit-Activity-Tracker/blob/master/src/Activity.js#L23-L27) would be a perfect use-case for reduce. Any time you are using `forEach` to add onto a variable like `arr` - you're re-implementing the behavior of reduce. This is exactly what reduce is for! Refactor!

* Be careful of typos like [Activty](https://github.com/chrisdbasham317/FitLit-Activity-Tracker/blob/master/src/Activity.js#L44) - even if your code is working because you spelled it wrong everywhere, it will stand out to employers as something that's a little sloppy/lazy

* No need for bracket notation [here](https://github.com/chrisdbasham317/FitLit-Activity-Tracker/blob/master/src/Activity.js#L51) - any time you have a string inside the brackets, switch it to dot notation.

* Very nice use of a ternary [here](https://github.com/chrisdbasham317/FitLit-Activity-Tracker/blob/master/src/Activity.js#L53), don't let your ternaries get any more complex than this!

* Try to have all of these [elements](https://github.com/chrisdbasham317/FitLit-Activity-Tracker/blob/master/src/scripts.js#L22-L87) already laid out in your HTML so that you can just access them by their classes and IDs, and update the text/html inside of them rather than having jQuery do all of this appending/inserting. e.g. instead of inserting an entire new paragraph tag for `<p class="p p--comunity-stairs">` - put that in your index.html to start, and just leave its inner text empty for now, until jQuery can go find it and put the necessary data in it. That will clean up your jQuery/dom manipulation code quite a bit.


### Test-Driven Development
* [x] 4: Application is broken into components which are well tested in both isolation and integration using appropriate data. Test feature many sad paths for methods as well.
* [ ] 3: All classes and methods are tested. Application is well tested but does not balance isolation and integration tests, using only the data necessary to test the functionality. Tests use smaller, sample data files as input rather than the large, original data files.
* [ ] 2: Application makes some use of tests, but the coverage is insufficient given project requirements.
* [ ] 1: Application does not demonstrate strong use of TDD.

* Take your data subset files from [this directory](https://github.com/chrisdbasham317/FitLit-Activity-Tracker/tree/master/test) and throw them into another directory called mocks.  e.g. `test/mocks/data.js`  - you'll see this convention in the wild and it will just help clean up your directory structure a bit.

* Because you are passing in different inputs for [these method calls](https://github.com/chrisdbasham317/FitLit-Activity-Tracker/blob/master/test/Activity-repository-test.js#L33-L38), and expecting different outputs, I would put each of these expectations in their own it blocks. You can also wrap related it blocks in their own describe block to organize your test output a bit better, like so:

```js
describe('getAvgActivityWeekly', () => {
  it('should return average numSteps', () => {

  });

  it('should return average minutesActive', () => {

  });

  // etc...
});
```

* Push yourself a bit further [here](https://github.com/chrisdbasham317/FitLit-Activity-Tracker/blob/master/test/Activity-repository-test.js#L9) - look into using a `beforeEach` block to instantiate this new activity repository. You're doing it in every single test and you could DRY up that redundant code with a `beforeEach`. (Edit: I see you're doing this elsewhere in other tests, GOOD JOB. Do it everywhere!)

* Overall very good coverage, looks like we might just be missing our tests for iteration 5 challenges, that's alright!

### Encapsulation / Breaking Logic into Components
* [x] 4: Application is expertly divided into logical components each with a clear, single responsibility.
* [ ] 3: Application effectively breaks logical components apart but breaks the principle of SRP.
* [ ] 2: Application shows some effort to break logic into components, but the divisions are inconsistent or unclear.
* [ ] 1: Application logic shows poor decomposition with too much logic mashed together.

* We talked about how you had some similar methods in many of your classes, and I mentioned this would be a great use-case for inheritance. You'll learn this for game time, but in a project like this, here's how it might go:

Let's say all of your Repo classes had a `getAveragePerWeek` method that would return the average data over the course of a week for a given user. You might create a base/parent `Repo` class that `HydrationRepo`, `SleepRepo`, `ActivityRepo` could all inherit that method from, like so:

```js
class Repo {
  constructor() {}

  getAveragePerWeek(userId, dataToCompare) {
    // return the comparison of your given user's data and your total data
    // (e.g. whatever logic you put in this method that you used in all of your classes)
  }
}

class HydrationRepo extends Repo {
  constructor() {
    super(); // super tells this class to inherit methods and properties from the Repo class
  }

  // no need for the getAveragePerWeek method in this class or any of your others any more
}

let hydroRepo = new HydrationRepo();
hydroRepo.getAveragePerWeek(3, {somedata}); // this would still work because your HydrationRepo would be inheriting this method from the `Repo` class
```


### User Interface
* [ ] 4: The application is pleasant, logical, and easy to understand. There are no holes in functionality and the application stands on its own to be used by the instructor _without_ guidance from the developer.
* [x] 3: The application has many strong displays/interactions, but a few holes in lesser-used displays.
* [ ] 2: The application shows effort in the interface, but the result is not effective. The evaluator has some difficulty using the application when reviewing the features in the users' needs.
* [ ] 1: The application is confusing or difficult to use.

* Heading title I think could be spread out a bit more, on a wide screen it looks weird that it's on 3 separate lines -- it ends up taking up a lot of vertical space 

* Font choices are making it a little difficult to decipher the heirarchy of content in places like [this](https://imgur.com/vgBOpDt) -- I feel like the headings here (Todays Stairs and Weekly Stair Average) dont stand out quite enough against the body copy. I would make your body font size a bit smaller, or fix up some line spacing here so that it more clearly denotes that "4 flights of stairs climbed today!" is related to "Todays Stairs". Right now i feel like all the text in this box is kind of competing for my attention. Something like [this](https://imgur.com/RUy7iqw) might read a little easier. (This goes for all your boxes of content -- lets denote that heirarchy of content a little better)

* It's a little weird for some boxes to be superrrr long vertically when they dont have that much content in them. I think the content you're displaying is pretty predictable and consistent, so you can be confident that certain boxes will only need x amount of vertical space, and you can combine them a bit better. e.g. I would combine the 'Time Active' and the 'Stair Count' boxes into one, and stack them on top of each other so that it fills up a bit more vertial space in a single box and aligns well with the 'Miles Walked'/'Step Goal' boxes. 

* Overall things just feel a bit HUGE. I have to do a lot of scrolling to see all the content. I think you can bump down the size of everything a tad, even with my very bad old tired eyes, I would still be able to read the content if it were a bit smaller.


### Workflow
* [x] 4: The team effectively uses Git branches and many small, atomic commits that document the evolution of their application with descriptive commit messages. The team displays good pairing practices (driver-navigator, dividing up work, etc.) and utilizes a planning tool more than GitHub issues (GitHub Projects, Trello, etc).
* [ ] 3: The team makes a series of small, atomic commits that document the evolution of their application. The team conducts a DTR (define the relationship) and utilizes GitHub issues and best pairing practices. Both members contribute meaningfully to the application.
* [ ] 2: The team makes large commits covering multiple features that make it difficult for the evaluator to determine the evolution of the application. The team does not utilize a planning tool or equitable pairing practices. One or both members do not contribute meaningfully to the application.
* [ ] 1: The team committed the code to version control in only a few commits. The evaluator cannot determine the evolution of the application.

* Your last three commits are all "Update README" -- look into `git squash` to see how you can squash all three of these into a nice single commit to clean up that history a bit. 

* Beautifully consistent commit messages, very easy to read through your history and see what changes were made based on just the messages. Keep that up!!

* Looks like a very nice even division of labor with equal contributions from both partners, great work.

* Research how to add that `.DS_Store` file to your global gitignore file (this will be a file on your machine) and you will never have to worry about committing those files again. We don't want these in our repos! Share with your friends when you learn how to do this :) 

* Typo in the abstract of your README, make sure to re-read this closely it's almost like a resume, the first thing employers will see when they come to this project! I'd maybe move the images up above the data examples in your readme, it helps me to better understand what the project is all about at a really quick glance and I'd like to see those earlier.