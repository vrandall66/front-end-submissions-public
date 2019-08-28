# FitLit
* Students: Ayla & Pol
* Evaluator: Brittany

## Rubric

### Functional Expectations
* [x] 4: Application fulfills all expectations of iterations 1 - 5 with no bugs or missing functionality *as well as* [ ] an extension.
* [ ] 3: Application fulfills expectations of iterations 1 - 5 with no bugs or missing functionality.
* [ ] 2: Application is usable but has some missing functionality.
* [ ] 1: Application crashes during normal usage.

* Drag and drop, deployed to GH pages, nice!!!

### Fundamental JavaScript & Style
* [ ] 4: Application demonstrates excellent knowledge of JavaScript syntax, style, and refactoring.
* [x] 3: Class methods use array and object prototypes - `for` loops are not used in the application. Application shows strong effort towards organization, content, and refactoring. 
* [ ] 2: Class methods use a mix of array and object prototypes and `for` loops. Application runs but the code has long methods, unnecessary or poorly named variables, and needs significant refactoring.
* [ ] 1: Application generates syntax error or crashes during execution.

* You have a lot of methods that start with the word `return` -- usually you would use the word `get` instead. Like `getAverageStepCount()`. Get is better than return in these cases because there might be instances where you are returning the result of that method and you'd be writing code like `return returnAverageStepCount()` which is a little hard to read.

* Overall the code is readable and mostly linted. There are a couple of inconsistencies - arbitrarily using `var` or `let`, missing some semi-colons in places, etc. Little nit picky things that can be cleaned up. 

* Some redundancies in places like [this](https://github.com/posi7790/fitlit/blob/master/src/Activity.js#L41) - in every method you are re-finding that specific user. You could call this directly in the constructor and set it as an instance property right away so that you don't have to keep finding that user over and over again. e.g.:

```js
constructor(activityData, user) {
  this.activityData = activityData;
  this.user = this.findUser(user.id);
}
```

and then in the rest of your methods you can just work with `this.user` instead of having to call that function and get your specific user each time.

* Try out that `Object.assign()` syntax I mentioned in class the other week for assigning your instance properties. Just for practice! Everything else looks so solid you can push yourself a little here. You'll see `Object.assign()` when you get to Redux in Mod 3, so you can practice it now and get ahead of things a bit :) 

* I'm not sure I've ever seen anyone use the `Number` class like [this](https://github.com/posi7790/fitlit/blob/master/src/ActivityRepo.js#L10) before. I think it might be bad practice :grimace emoji:  Did you read up on this somewhere or was it recommended some place or is it doing something especially helpful for you?? I'd be interested to know!

* Very nice use of all your prototype methods! Some lines get a little long like [here](https://github.com/posi7790/fitlit/blob/master/src/SleepRepo.js#L53), when this happens, break away from all the chaining and just start assigning the result of each method to a variable instead.

### Test-Driven Development
* [ x ] 4: Application is broken into components which are well tested in both isolation and integration using appropriate data. Test feature many sad paths for methods as well.
* [ ] 3: All classes and methods are tested. Application is well tested but does not balance isolation and integration tests, using only the data necessary to test the functionality. Tests use smaller, sample data files as input rather than the large, original data files.
* [ ] 2: Application makes some use of tests, but the coverage is insufficient given project requirements.
* [ ] 1: Application does not demonstrate strong use of TDD.

* Little confused by the wording of these [it blocks](https://github.com/posi7790/fitlit/blob/master/test/Sleep-test.js#L28-L33). You mean it should store those values as instance properties? Or accept them as arguments?

* Overall very solid tests, I believe I would be able to re-implement all your functionality just by reading your tests. One convention for working with that mock data is to have a folder inside of your test directory called `mocks` to store all of that fake data for yourself. This just helps keep it separate from your actual application data and helps others recognize that it's only for testing purposes. 


* For tests [like this](https://github.com/posi7790/fitlit/blob/master/test/ActivityRepo-test.js#L20-L30) that are all testing the same method, just giving it different arguments, I would wrap these in another describe block like so:

```js
describe('returnAverage', () => {
  it('should return the average number of stair climbed for all users for a specific date', () => {
    expect(activityRepo.returnAverage("2019/06/15", 'flightsOfStairs')).to.equal(21);
  });

  it('should return the average number of steps for all users taken for a specific date', () => {
    expect(activityRepo.returnAverage("2019/06/15", 'numSteps')).to.equal(6027);
  });

  it('should return the average minutes active for a specific date for all users', () => {
    expect(activityRepo.returnAverage("2019/06/15", 'minutesActive')).to.equal(144);
  });
});
```

That will help format your test output a little cleaner and help group all of these related tests together 

### Encapsulation / Breaking Logic into Components
* [x] 4: Application is expertly divided into logical components each with a clear, single responsibility.
* [ ] 3: Application effectively breaks logical components apart but breaks the principle of SRP.
* [ ] 2: Application shows some effort to break logic into components, but the divisions are inconsistent or unclear.
* [ ] 1: Application logic shows poor decomposition with too much logic mashed together.

* Very good class structure with appropriate instance properties and methods in each. Take some time to reflect on what areas of your code seem a bit redundant. Were there very similar methods across your classes that you would have liked them to share? This will be a helpful thought exercise for when we get into inheritance and extending classes.


### User Interface
* [x] 4: The application is pleasant, logical, and easy to understand. There are no holes in functionality and the application stands on its own to be used by the instructor _without_ guidance from the developer.
* [ ] 3: The application has many strong displays/interactions, but a few holes in lesser-used displays.
* [ ] 2: The application shows effort in the interface, but the result is not effective. The evaluator has some difficulty using the application when reviewing the features in the users' needs.
* [ ] 1: The application is confusing or difficult to use.

* B-E-A-utiful UI! Drag and drop is a little tough to interact with. The drop-shadow hover effect was a little confusing at first, it made me feel like I should be able to click on each section, but nothing happened on click. Very unlikely that someone other than me would recognize that they can drag and drop, unless they accidentally did it. Fix for this would be to change that cursor into one of those draggy hands on hover as well. `cursor: grab` https://developer.mozilla.org/en-US/docs/Web/CSS/cursor The elements also go into kind of weird places when you drag them. This is something I would either fix up over intermission, or disable as a feature for when you start interviewing. (Either get it working GREAT or just remove it so potential employers aren't like hmmmmmm) Love the icons for water/trophies/etc. Really helps me understand what kind of charts and data I'm going to be looking at.

### Workflow
* [x] 4: The team effectively uses Git branches and many small, atomic commits that document the evolution of their application with descriptive commit messages. The team displays good pairing practices (driver-navigator, dividing up work, etc.) and utilizes a planning tool more than GitHub issues (GitHub Projects, Trello, etc).
* [ ] 3: The team makes a series of small, atomic commits that document the evolution of their application. The team conducts a DTR (define the relationship) and utilizes GitHub issues and best pairing practices. Both members contribute meaningfully to the application.
* [ ] 2: The team makes large commits covering multiple features that make it difficult for the evaluator to determine the evolution of the application. The team does not utilize a planning tool or equitable pairing practices. One or both members do not contribute meaningfully to the application.
* [ ] 1: The team committed the code to version control in only a few commits. The evaluator cannot determine the evolution of the application.

* Very nice consistent commit messages, and even distribution of work. (Though it looks like Pol may have committed a library or some big external code? +31,000 lines is a lot of contributions, but I'd imagine some of that is adding in dependencies)

* Push yourselves further: your commit history has a *lot* of merge commits. These clutter up the history and make it hard to really see what changes were made when, because the merge commit messages aren't super detailed. A more common (and somewhat challenging) workflow that you'll see on the job is called Rebasing. Research that on your own, and feel free to try it out on your group project. You can start with this [video](https://www.youtube.com/watch?v=CRlGDDprdOQ). Let me know if you dig into it a bit and have any questions.

* Very nice README! This looks in tip-top shape for showing to employers. Research how to add that `.DS_Store` file and `.vscode` directory to your global gitignore file (this will be a file on your machine) and you will never have to worry about committing those files again.