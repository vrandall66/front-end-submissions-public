### Evaluator: Leta
### Students: Theo, Adam
### Comments:

Number of commits is 89, which is low for a project of this scope. This indicates that the changeset in a given commit is probably a bit larger than is good to see. Commit messages are inconsistent (use imperative voice, and be more descriptive than naming the component being worked on).

Container tests are failing to test mapStateToProps and mapDispatchToProps. Many containers are also failing to test their component methods. For example, Card does not test its fetch, or that `handleToggleFavorite` is calling `deleteFavorites` or `changeFavorites`.

Your routing is a bit weird. I saw that you're having to directly force the history in some spots, rather than refactoring so you can make use of the Link or NavLink components.

## Rubric

### Specification Adherence

* 3 - The application completes all iterations above without error. Evaluator has minimal recommendations for design changes.

### Project Professionalism

* 3 - PropType functionality is complete, the codebase has less than 5 linter errors, README has been updated with all group members. Project utilized wireframes from the outset. All git commits are atomic, made first to branches, and use descriptive and concise commit messages. Project demonstrates a fundamental understanding of React architecture.

### Testing

* 2 - Nearly all unit tests for Redux and React are in place. No attempt to test async functionality was made.

### Redux Architecture

* 3 - Appropriate components are wrapped in connected Redux container components. The Redux store contains all necessary application data. All state changes are handled through Redux actions and reducers.

### Routing

* 3 - Application uses React Router to display appropriate components based on URL.
