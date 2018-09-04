# Game Time
* Students: Drake & Laura
* Evaluator: Pamela Lovett

Comments:
* Overall, nice, clean UI/UX. Movement on the left side of the screen when snake eats the food/score updates is _very_ distracting. Make sure that selected level stays selected as indicated by color change
* Medium and Hard are so fast as to almost be unplayable. Maybe harder levels could not only speed up a bit but also add obstacles that the snake has to avoid?
* Separation of the "Snake" by having a `Snake` class and a `Body` class is strange. Just have `Snake` class.

### Functional Expectations

* 3 - Application is fully playable without crashes or bugs

### User Interface

* 3.5 - The application is pleasant, logical, and easy to use. There are no holes in functionality and the application stands on its own to be used by the instructor _without_ guidance from the developer.

### Testing

* 3.5 - Project has a running test suite that exercises the application at multiple levels. The test suite covers almost all aspects of the application and uses mocks and stubs when appropriate. ESLint shows 0 complaints.

- ESLint shows ZERO complaints for lib files - nice work
- Your formatting/indentation in your test files make your tests _very_ hard to read. This prompted me to run ESLint on your testing suite (which we don't normally) and it shows 40+ errors from indentation and improper spacing. I would recommend adding this as an issue to fix. 

### JavaScript Style & OOP

* 3 - Application is thoughtfully put together with some duplication and no major bugs. Developer can speak to choices made in the code and knows what every line of code is doing. Application is organized into classes (and correctly uses inheritance) with some misplaced logic and no major bugs. Business-logic code is mostly separated from view-related code. Developer can speak to choices made in the code and knows what each line of code is doing.

### Workflow

* 3 - The developer/team makes a series of small, atomic commits that document the evolution of their application. There are no formatting issues in the code base. The team conducts a DTR (define the relationship) and utilizes a planning tool and pairing practices. Both members contribute meaningfully to the application.

- Be sure that you are following conventions for commit messages - capitalize first letter, no puncutation. A fair number of commits could use better descriptions either in the header or the body.
