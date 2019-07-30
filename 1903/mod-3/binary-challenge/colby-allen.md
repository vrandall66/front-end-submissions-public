### Evaluator: Leta
### Students: Colby
### Comments:

* Very cool app idea!
* Not responsive, and colors are fairly aggressive, but very on theme!
* Redux store is flat and non-redundant - hooray! Nice job on that
* Nice separation of components and containers
* Components are very simple and clean
* Crimes container is nice - thank you for pulling out the displays into their own functions!
* The team sidebar could be cleaned up a bit - lots of redundant code. Could perhaps store team names in an array and loop through the data to generate the NavLinks
* The reducers should be in their own files? For readability. For example, it'd be nice to see a file called crimeReducer, and one called teamReducer, etc. Just to very clearly delineate the different pieces of state in the store.
* componentDidMount in App should be making use of `Promise.all`

```
<section className='crimes'>
  <CrimesContainer crimes={this.props.crimes} players={this.props.players} positions={this.props.positions}/>
</section>
```
^^^ Don't do that haha. Put the className inside the CrimesContainer component, on the outermost element in the return.

* Routes are redundant with a lot of repeated code - could you use a NavLink instead?
* Great use of PropTypes
* `App.js` is missing redux tests
* Your `mapStateToProps` tests should start out with state having MORE data than what you actually want added to the props of the component, to show for sure that it's only pulling in the data you want.
* Commit messages are vague and inconsistent
* Virtually no use of PRs
* Sad path tests for async functions are erroring out the test suite

## Rubric

### Specification Adherence

* 3 - The application uses the above technologies to a professional level. The evaluator has minimal recommendations for refactoring or design changes.


### Project Professionalism

* 3 - PropType functionality is complete, the codebase has less than 5 linter errors, README has been updated with all group members. Project utilized wireframes from the outset. All git commits are atomic, made first to branches, and use descriptive and concise commit messages. Project demonstrates a fundamental understanding of React architecture.
* 2 - Project is missing PropTypes, README updates, wireframes, or has more than 5 linter errors. Project team makes large infrequent git commits. Project shows a basic understanding of React.

### Testing

* 3 - All Redux functionality is tested (actions, reducers, mapStateToProps, mapDispatchToProps), all components are unit tested, and a valid attempt was made to test any async functionality.

### Redux Architecture

* 4 - All requirements from 3 met, and no duplication of data exists in the store. Data in the store remains flat (not nested).

### Routing

* 3 - Application uses React Router to display appropriate components based on URL.
