## Rubric

### Project Specification Adherence

* **4** - No approach was taken that is counter to the spirit of the project and its learning goals. There are no features missing from above that make the application feel incomplete or hard to use. Data persists on refresh using a knex/postgreSQL database.
* **3** - There is one feature missing from the base expectations that makes the application feel incomplete or hard to use.
* **2** - There are two features missing from the base expectations that make the application feel incomplete or hard to use.

### User Interface

* **4** - User interface is intuitive and the instructor can easily use it on their own without guidance. Styling is consistent and call-to-action elements are obvious. The application provides the user with relevant feedback based on interactions.  
* **3** - User interface is mostly intuitive, though the instructor might need some guidance on interactions. Styling is mostly consistent, but could use some clean up. Application may be missing some relevant feedback that would help guide the user. 
* **2** - User interface demonstrates some effort, but is not intuitive and the instructor needs help figuring out how to use the application. Styling has several inconsistencies and it's sometimes unclear what elements a user can interact with. Application lacks useful feedback for the user.  
* **1** - User interface does not demonstrate effort and is unintuitive. The instructor cannot use the application on their own. Styling is inconsistent and user interactions are unclear. Application lacks useful feedback for the user.


### Testing

* **4** - FE shows 75%+ test coverage. Every server endpoint is tested thoroughly: status code, response content, happy and sad paths.
* **3** - FE shows 75%+ test coverage. Every server endpoint is tested: status code, response content, happy paths. Some sad paths are not tested. Response content tests are not robust enough.
* **2** - FE shows less than 75% test coverage. A few server endpoint tests are missing. Some happy paths are tested. Response content tests are unhelpfully vague.
* **1** - FE shows less than 75% test coverage. Several server endpoint tests are missing.

### Workflow

* **4** - Developer(s) make many small, atomic commits that clearly document the evolution of the application and do not contain irrelevant changesets that aren't reflected by the commit message. Commit messages are concise and consistent in syntax and tense. Developer(s) effectively use git branches and pull requests when applicable to incorporate changes into the application, and are not pushing directly to master. There are no instances where the developer(s) have committed source code that should be .gitignored. There are no instances of "dead" or commented-out code and debugger statements like console.log.
* **3** - Developer(s) make many small, atomic commits that document the evolution of the application but sometimes contain irrelevant changesets and inconsistent commit messages. Developer(s) use git branches and pull requests when applicable to incorporate changes into the application, and are not pushing fresh changes directly to master. Pull requests may contain little or no code review. There may be slight instances where the developer(s) have committed source code that should be .gitignored. There may be some instances of "dead" or commented-out code and debugger statements like console.log that need to be cleaned up.
* **2** - Developer(s) make large, inconsistent commits that contain irrelevant changesets and make it difficult to follow the evolution of the application. Developer(s) rarely use git branches and frequently incorporate changes directly into master with little or no review process. There are instances of committed source code that should be .gitignored and instances of dead code and/or debugger statements.
* **1**  - Developer(s) make very few commits that each cover too much responsibility and aren't indicative of how the application evolved. Branches and pull requests were not used and changesets were applied directly to master. There are many instances of committed source code that should be .gitignored and many instances of dead code and/or debugger statements.

If a project is not in a passing state, instructors _may_ offer the team the weekend to complete functionality with specific tasks to be completed. These extensions are not guaranteed and are only offered in some cases.
