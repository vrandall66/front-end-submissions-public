### Evaluator: Travis Rollins
### Students: Colby Allen & Jacqueline Moore
### Comments:
* Awesome work keeping your App pretty clean
* Nice work breaking out fetches into separate file
* Think about when you need to fetch your data as opposed to fetching it all at the beginning
* Should only need one catch to handle errors
* After fetching the data, see how you can clean out the unneeded data
* Might create a Card container, and as we map through it, return a Card component passing the props we need
* Keep thinking about when to use shallow vs mount
* Shouldn't need to include BrowserRouter for testing components
* Great work testing our changes in state, would continue adding tests to simulating events like clicks
* Nice work testing out async tests
  * Might include another sad path test to check if property of ok is true
* Might included a 404 page if a route doesn't exist
* Make sure to include propTypes on functional components as well
* Continue to make more atomic commits and have more conversation/review on GH
* Great work on your readme

## LightSide Rubric

### Specification Adherence

* 3 - The application completes all iterations above without error. Evaluator has minimal recommendations for design changes.

### Project Professionalism

* 2 - Project is missing PropTypes, README updates, wireframes, or has more
  than 5 linter errors. Project team makes large infrequent git commits.
  Project shows a basic understanding of React.

### Testing

* 3 - All requirements from 2 are met and a valid attempt to test asynchronous functionality has been made.

### Routing

* 3 - Application uses React Router to display appropriate components based on URL.

