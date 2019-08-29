# FitLit 
* Students: Amy & Brady
* Evaluator: Brittany

## Rubric

### Functional Expectations
* [x] 4: Application fulfills all expectations of iterations 1 - 5 with no bugs or missing functionality *as well as* [ ] an extension.
* [ ] 3: Application fulfills expectations of iterations 1 - 5 with no bugs or missing functionality.
* [ ] 2: Application is usable but has some missing functionality.
* [ ] 1: Application crashes during normal usage.

* Deployed to GH pages - I dont think this is listed as an actual extension but I'm making it one! Good job

### Fundamental JavaScript & Style
* [ ] 4: Application demonstrates excellent knowledge of JavaScript syntax, style, and refactoring.
* [x] 3: Class methods use array and object prototypes - `for` loops are not used in the application. Application shows strong effort towards organization, content, and refactoring. 
* [ ] 2: Class methods use a mix of array and object prototypes and `for` loops. Application runs but the code has long methods, unnecessary or poorly named variables, and needs significant refactoring.
* [ ] 1: Application generates syntax error or crashes during execution.

* I can tell based on your [tests here](https://github.com/bradybridges/fit-lit/blob/master/test/ActivityRepo-test.js#L22-L32) that this is logic that could be refactored. Without even looking at your JS, I would put money down that these methods are all doing the exact same logic with only a single, subtle difference with regards to what data point it's returning. Good opportunity for refactoring here!

* [This constructor](https://github.com/bradybridges/fit-lit/blob/master/src/User.js) is a good place to try out that `Object.assign()` syntax I mentioned in class the other day -- you'll see assign in Mod 3 so you might want to practice it now!


### Test-Driven Development
* [ ] 4: Application is broken into components which are well tested in both isolation and integration using appropriate data. Test feature many sad paths for methods as well.
* [x] 3: All classes and methods are tested. Application is well tested but does not balance isolation and integration tests, using only the data necessary to test the functionality. Tests use smaller, sample data files as input rather than the large, original data files.
* [ ] 2: Application makes some use of tests, but the coverage is insufficient given project requirements.
* [ ] 1: Application does not demonstrate strong use of TDD.

* If you do the refactoring mentioned above for [these methods](https://github.com/bradybridges/fit-lit/blob/master/test/ActivityRepo-test.js#L22-L32) you could be testing the same single method here in each of these it blocks, and then organize your test output better by wrapping them in a describe block. eg:

```js
describe('getAvgAllUsers', () => {
  it('should return all users avg steps given date', () => {
  });

  it('should return all users avg min active given date', () => {
  });

  it('should return total steps for week for a user', () => {
  });
});
```

* Make sure for tests like [this](https://github.com/bradybridges/fit-lit/blob/master/test/HydrationRepo-test.js) we're still doing some of those easier gimmee tests where we check that any instance properties in the constructor were set appropriately. Glad you got your method tests in for your classes, but don't skip over the easy ones! That's where your code will inevitably end up biting you in the butt if you skip those tests.

* Nice consistent use of your beforeEach blocks for setup code in all your files

* Dont intermingle your test data with your application data by having it all in the data directory. Make a separate directory under your test folder for `mocks` where you have any test-specific datasets you're using.


### Encapsulation / Breaking Logic into Components
* [x] 4: Application is expertly divided into logical components each with a clear, single responsibility.
* [ ] 3: Application effectively breaks logical components apart but breaks the principle of SRP.
* [ ] 2: Application shows some effort to break logic into components, but the divisions are inconsistent or unclear.
* [ ] 1: Application logic shows poor decomposition with too much logic mashed together.

### User Interface
* [ ] 4: The application is pleasant, logical, and easy to understand. There are no holes in functionality and the application stands on its own to be used by the instructor _without_ guidance from the developer.
* [ ] 3: The application has many strong displays/interactions, but a few holes in lesser-used displays.
* [x] 2: The application shows strong effort in the interface, but the result is not effective. The evaluator has some difficulty using the application when reviewing the features in the users' needs.
* [ ] 1: The application is confusing or difficult to use.

* I like the attempt at keeping the context super simple to start and not showing everything on the page all at once, but it's *really* difficult to tell that something has been added to the page when I click on an icon. e.g. after I click on the profile and I see the user's data, if I click on the hydration icon after that it's really difficult for me to know that something appeared below my profile. I would rework this so that as you click on those icons, only one section of content is displayed at a time rather than each piece staying displayed until you click its icon again. The way it's working now I would also expect some sort of active state or styling to be on the icons to denote that section is currently displayed or not. It's unclear that I can toggle those content areas on and off (e.g. i wasn't sure what would happen if I clicked the profile icon for a 2nd time)

* We also want some differentiation in the text on the page to better denote heirarchy -- right now a lot of that content is the same font-size/style which makes everything kind of compete for my attention


### Workflow
* [ ] 4: The team effectively uses Git branches and many small, atomic commits that document the evolution of their application with descriptive commit messages. The team displays good pairing practices (driver-navigator, dividing up work, etc.) and utilizes a planning tool more than GitHub issues (GitHub Projects, Trello, etc).
* [x] 3: The team makes a series of small, atomic commits that document the evolution of their application. The team conducts a DTR (define the relationship) and utilizes GitHub issues and best pairing practices. Both members contribute meaningfully to the application.
* [ ] 2: The team makes large commits covering multiple features that make it difficult for the evaluator to determine the evolution of the application. The team does not utilize a planning tool or equitable pairing practices. One or both members do not contribute meaningfully to the application.
* [ ] 1: The team committed the code to version control in only a few commits. The evaluator cannot determine the evolution of the application.

* Nice consistent git commit messages, but lots of duplicates and merge/conflict fix commits that clutter up the history. Look into `git squash` for squashing duplicate commits into one (e.g. if you have 3 'Update Readme' commits, we can just merge those all into one). Also, if you're looking to push yourself further, you can do some research on the rebasing workflow. So far you've been doing the merge workflow, but on the job you'll likely be expected to rebase instead. This will help you avoid adding a bunch of merge commits into your history (we want to avoid those because they dont give us a ton of insight into the changes that were made there and clutter up our history). You can try the rebasing workflow with your group project if you feel comfortable after doing some research on it.

* Looks like an even distribution of work although maybe Brady committed some large external files/libraries/dependencies? 94K lines of code added is quite a lot :) But commits seem even!