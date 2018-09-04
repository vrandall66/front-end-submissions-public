# Game Time
* Students: Jessica & Chris
* Evaluator: Brittany

Comments:
* Great job taking the project in a creative direction
* Try to schedule a check-in with instructors before evals happen; it seemed like there were a lot of things that 'clicked' as we spoke that could've been fixed during a check-in


### Functional Expectations

* 4 - Application is fully playable and exceeds the expectations set by instructors

* GH-pages deploy

### User Interface

* 4 - The application is pleasant, logical, and easy to use. There are no holes in functionality and the application stands on its own to be used by the instructor _without_ guidance from the developer.

* Love the creativity and new spin on the theme for the game!

### Testing

* 3 - Project has a running test suite that tests multiple levels but fails to cover some features. All functionality is covered by tests. The application makes some use of integration testing. ESLint shows < 5 complaints.

* Not sure where all of your tests went but [this](https://github.com/Jessica-Erickson/game-time/tree/master/test) is definitely not all of them. Make sure they get back into the test directory wherever they went. You might have to go back into older commits to find those files and put them back in place.

### JavaScript Style & OOP

* 3 - Application is thoughtfully put together with some duplication and no major bugs. Developer can speak to choices made in the code and knows what every line of code is doing. Application is organized into classes (and correctly uses inheritance) with some misplaced logic and no major bugs. Business-logic code is mostly separated from view-related code. Developer can speak to choices made in the code and knows what each line of code is doing.

* Little confusion on what values you did/did not have access to at a given time, which caused some funky code and opportunities for refactoring.

* Be consistent with your variable declarations - you're using [let](https://github.com/Jessica-Erickson/game-time/blob/master/lib/index.js#L123) / [var](https://github.com/Jessica-Erickson/game-time/blob/master/lib/index.js#L136) in similar places, pick one and stick to it. Otherwise it looks arbitrary.

### Workflow

* 3 - The developer/team makes a series of small, atomic commits that document the evolution of their application. There are no formatting issues in the code base. The team conducts a DTR (define the relationship) and utilizes a planning tool and pairing practices. Both members contribute meaningfully to the application.

* Mostly nice, consistent commit messages - a few that don't follow conventions in terms of capitalization/punctuation/tense but overall readable

* Commits should probably be a bit tinier and do less. [This](https://github.com/Jessica-Erickson/game-time/commit/c3df1f6d3e93a60a608f1b22f47119100c461643) for example should be split into at least 2 or 3 different commits. You want to keep your diffs as tiny as possible so that when you pull request changes, it's easier for other developers to follow along with the changes because there are only relevant changesets in the PR.