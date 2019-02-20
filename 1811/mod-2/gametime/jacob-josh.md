# Game Time
* Students: Jake and Josh
* Evaluator: Pam

Comments:
* Nice README!
* Overall, UI and UX is pretty good. Would suggest flipping the colors for letters that are available to buy/pick. It is confusing from a UX perspective that the vowels show as light red while the other letters (which are actually available to pick) match the color of the background. I found that I had to remind myself several times that red indicated that they _weren't_ available.
* Minor bug - wheel seems to land on `BANKRUPT` a lot more than it should, pretty consistently.


### Functional Expectations

* [x] Proficient - Application is fully playable and meets all requirements of the spec.

### User Interface

* [x] Proficient - The application has many strong pages/interactions, but a few holes in lesser-used functionality.

### Testing

* [x] Advanced Beginner - Project has sporadic use of tests at multiple levels. The application contains numerous holes in testing and/or many features are untested. ESLint shows 5+ complaints.

* 2 errors in ESLint
* Mosts tests are verifying data types. Always lean for quality over quantity with tests. Remember to test for different outputs from conditionals - opportunities around this, mostly in `Game`
* (This)[https://github.com/JakeAdmire/Wheel-of-MisFortune/blob/master/test/wheel-test.js#L37 ] should be `deep equal` since you are comparing objects. You would also want to update your test so that it's checking/comparing the actual elements (as each new `Wheel` instance does equal each other, initially, before values are assigned)

### JavaScript Style & OOP


* [x] Proficient - Application is thoughtfully put together with some duplication and no major bugs. Developer can speak to choices made in the code and knows what every line of code is doing. Application is organized into classes (and correctly uses inheritance) with some misplaced logic and no major bugs. Business-logic code is mostly separated from view-related code. Developer can speak to choices made in the code and knows what each line of code is doing.

* Naming is good and easy to follow!
* Overall, code is easy to read. Some longer methods (especially in `Game` that could be refactored)
* (These properties)[https://github.com/JakeAdmire/Wheel-of-MisFortune/blob/master/src/Game.js#L12-L15 ] seem like things `Game` should not be tracking
* `Game` is doing quite a bit - make sure `Puzzle` is dealing with the logic for the puzzle... same with `Wheel`...

### Workflow

* [x] Exceptional - Meets all requirements for `Proficient`. In addition, the developer/team effectively uses Git branches and many small, atomic commits that document the evolution of their application with descriptive commit messages. The team displays good pairing practices (driver-navigator, dividing up work, etc) and utilizes some sort of planning tool (GitHub issues, Waffle, Trello, etc). The team develops a clear MVP (minimum viable product) and conducts a DTR (define the relationship). Both members contribute meaningfully to the application.