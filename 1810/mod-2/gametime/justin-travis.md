# Game Time
* Students: Justin & Travis
* Evaluator: Brittany


### Functional Expectations

* 4 - Application is fully playable and exceeds the expectations set by instructors

* Still some bugginess around the wagering for final jeopardy -- it seems like the wager is adding onto everybody's wager when you click through those numbers rather than resetting each time. 
* +1 for deployment to GH pages

### User Interface

* 2.5 - The application has many strong pages/interactions, but a few holes in areas that are important for determining what the user should be doing and where they should be looking.


* Font is a bit difficult to read in places; save cool/unique fonts for headings and large titles, not smaller text like on inputs and buttons
* Is the loading bar actually doing/caculating progress on something? Or is it just there for show? It looks kind of out of place right now/inconsistent with the overall UI.
* Name entry page is way too spread out, looks like it was designed for a mobile device even when being viewed on a smaller laptop. 
* Difficult to tell whose turn it is with the small font text in the bottom left.
* Hover effects are too subtle/non-existant which makes it difficult to tell what's actually clickable or not
* I think it's a bit *more* confusing to have the players rotating at the top to denote the current player -- you want to avoid moving UI elements around on people unless absolutely necessary. With the rotation as it is, now as a player, I have to keep looking in a different spot to find my score.
* Shouldn't be able to start a game without inserting player names -- it makes the text in the bottom left unusable.
* Not sure what the negative numbers are when the wager option pops up for daily doubles -- I would simplify this to just have a single number input field where they can enter their wager manually rather than clicking those numbers. It's also difficult to know that I'm supposed to click on the final wager in order to move on to the actual question. This should be a clearer button that says something like 'Submit Wager >'


### Testing

* 4 - Project has a running test suite that exercises the application at multiple levels. The test suite covers almost all aspects of the application and uses mocks and stubs when appropriate. ESLint shows 0 complaints.
* 3 - Project has a running test suite that tests multiple levels but fails to cover some features. All functionality is covered by tests. The application makes some use of integration testing. ESLint shows < 5 complaints.
* 2 - Project has sporadic use of tests at multiple levels. The application contains numerous holes in testing and/or many features are untested. ESLint shows 5+ complaints.
* 1 - There is little or no evidence of testing in this application. ESLint shows 10+ complaints.

### JavaScript Style & OOP

* 4 - Application has exceptionally well-factored code with little or no duplication. SRP (single responsibility principle) and DRY (don’t repeat yourself) principles are utilized. There are zero instances where an instructor would recommend taking a different approach. Application is organized into classes (and correctly uses inheritance) and there are no instances where instructor would suggest moving logic or data to another class. The business-logic code driving functionality is cleanly separated from rendering, view-related code.
* 3 - Application is thoughtfully put together with some duplication and no major bugs. Developer can speak to choices made in the code and knows what every line of code is doing. Application is organized into classes (and correctly uses inheritance) with some misplaced logic and no major bugs. Business-logic code is mostly separated from view-related code. Developer can speak to choices made in the code and knows what each line of code is doing.
* 2 - Your application has a significant amount of duplication and one or more major bugs. Application is organized into classes that do not display a good understanding of encapsulation, and logic is not well-divided. Developer cannot articulate what each line of code is doing. There are one or more major bugs.
* 1 - Your client-side application does not function. Developer writes code with unnecessary variables, operations, or steps that do not increase clarity. Application is not separated into classes, or methods and properties are illogically assigned to classes. Developer writes code with unnecessary variables, operations, or steps that do not increase clarity. Business-side logic and view-related code is not separated at all.


### Workflow

* 4 - The developer/team effectively uses Git branches and many small, atomic commits that document the evolution of their application with descriptive commit messages. The team displays good pairing practices (driver-navigator, dividing up work, etc) and utilizes some sort of planning tool (GitHub issues, Waffle, Trello, etc). The team develops a clear MVP (minimum viable product) and conducts a DTR (define the relationship). Both members contribute meaningfully to the application.
* 3 - The developer/team makes a series of small, atomic commits that document the evolution of their application. There are no formatting issues in the code base. The team conducts a DTR (define the relationship) and utilizes a planning tool and pairing practices. Both members contribute meaningfully to the application.
* 2 - The developer/team makes large commits covering multiple features that make it difficult for the evaluator to determine the evolution of the application. The team does not utilize a planning tool or equitable pairing practices. One or both members do not contribute meaningfully to the application.
* 1 - The developer/team committed the code to version control in only a few commits. The evaluator cannot determine the evolution of the application.
* 0 - The application was not checked into version control.
