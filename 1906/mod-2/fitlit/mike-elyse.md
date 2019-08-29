# FitLit
* Students: Mike & Elyse
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

* Some inconsistencies in stylistic things like mixing some ES5 and ES6 arbitrarily (let vs var, function() vs. arrow) - just be sure to go back and clean this up later, but otherwise the code is overall clean and easy to read

* Try not to use the word `return` in your method names -- use `get` instead. You won't see functions with the word `return` in their name because it could get confusing if you ran into a scenario where you had to write something like `return returnAverageMinutes()` 

* [These](https://github.com/ec-myers/fitlit/blob/master/src/Activity-Repository.js#L33-L48) are all veryyyy similar methods. How can we combine them into one and make it more dynamic??? Same [here](https://github.com/ec-myers/fitlit/blob/master/src/Activity-Repository.js#L59-L72)

* Try using that `Object.assign()` trick I mentioned in class [here](https://github.com/ec-myers/fitlit/blob/master/src/User.js#L2-L10) -- e.g.:

```js
constructor(userData) {
  Object.assign(this, userData);
}
```

* It feels a little hard for me to decipher what's being returned [here](https://github.com/ec-myers/fitlit/blob/master/src/Hydration-Repository.js#L31-L34) because there are so many return statements. It's usually better practice to create a single variable for yourself that has a solid name for what you're returning -- and then reassign that value as necessary so that at the end of your function, you're returning a single variable no matter what. e.g. in this method I would do something like :

```js
let didDrinkEnough = true;

// a bunch of your reduce logic

if (avgDrank < 64) {
  didDrinkEnough = false;
}

return didDrinkEnough;
```


### Test-Driven Development
* [x] 4: Application is broken into components which are well tested in both isolation and integration using appropriate data. Test feature many sad paths for methods as well.
* [ ] 3: All classes and methods are tested. Application is well tested but does not balance isolation and integration tests, using only the data necessary to test the functionality. Tests use smaller, sample data files as input rather than the large, original data files.
* [ ] 2: Application makes some use of tests, but the coverage is insufficient given project requirements.
* [ ] 1: Application does not demonstrate strong use of TDD.

* Move that test-data directory into your test directory to keep your root organized. 

* Looks like we're missing the declaration for `user2` before our [beforeEach](https://github.com/ec-myers/fitlit/blob/master/test/activity-repository-test.js#L10-L16)? Did this cause any issues?

* VERY good coverage for all of your methods, I can't find any methods that are untested. Nice use of your beforeEach blocks to dry up that setup code. Good work!


### Encapsulation / Breaking Logic into Components
* [x] 4: Application is expertly divided into logical components each with a clear, single responsibility.
* [ ] 3: Application effectively breaks logical components apart but breaks the principle of SRP.
* [ ] 2: Application shows some effort to break logic into components, but the divisions are inconsistent or unclear.
* [ ] 1: Application logic shows poor decomposition with too much logic mashed together.

* The sleep and activity classes look just a littleeeee overloaded to me, but I think if you took some of the refactoring advice above and made your methods more dynamic, you could cut down on a lot of that code. Then I'd feel perfectly fine with your division of responsibilities among your classes!

### User Interface
* [ ] 4: The application is pleasant, logical, and easy to understand. There are no holes in functionality and the application stands on its own to be used by the instructor _without_ guidance from the developer.
* [x] 3: The application has many strong displays/interactions, but a few holes in lesser-used displays.
* [ ] 2: The application shows effort in the interface, but the result is not effective. The evaluator has some difficulty using the application when reviewing the features in the users' needs.
* [ ] 1: The application is confusing or difficult to use.

* Very very gray, maybe a little more color? :)

* Love the little sad ghost image for people who aren't sleeping well!!

* I see there's a drop shadow on my boxes on hover, which would make me kinda feel like I could do something with the box, like click on it or drag and drop it? Doesn't appear that I can actually do anything though. Save the hover states for elements that a user can interact with

* Nice heirarchy created for your text by making the headings stand out and the body text a bit smaller/less attention grabbing. I don't feel as though they are competing for my attention.

* I would consider adding a bit more margin between all the boxes, there are a lot of them and it's a lot of data we're looing at here so it can get a bit overwhelming if we don't give ourselves enough white space to rest our eyes in!



### Workflow
* [ ] 4: The team effectively uses Git branches and many small, atomic commits that document the evolution of their application with descriptive commit messages. The team displays good pairing practices (driver-navigator, dividing up work, etc.) and utilizes a planning tool more than GitHub issues (GitHub Projects, Trello, etc).
* [ ] 3: The team makes a series of small, atomic commits that document the evolution of their application. The team conducts a DTR (define the relationship) and utilizes GitHub issues and best pairing practices. Both members contribute meaningfully to the application.
* [x] 2: The team makes large commits covering multiple features that make it difficult for the evaluator to determine the evolution of the application. The team does not utilize a planning tool or equitable pairing practices. One or both members do not contribute meaningfully to the application.
* [ ] 1: The team committed the code to version control in only a few commits. The evaluator cannot determine the evolution of the application.

* Lots of commits which means that you're committing tiny changes frequently, great!

* Your last couple of commits are all about fixing up screenshots -- look into `git squash` to see how you can squash all of these into a nice single commit to clean up that history a bit. 

* Nice consistent git commit messages that make the history easy to read

* Division of labor looks *really* lopsided -- just based on commits it looks like Elyse was either doing all the work or driving the entire project. I'd like to hear what both of your thoughts are on this. What was that workflow like? I feel that you both are technically solid and have good work ethic and enjoy contributing code to your projects, but the history doesn't reflect that right now. I have to give you a 2 on workflow because of this for now, but if we want to have a conversation about it to clear it up that would be great.


