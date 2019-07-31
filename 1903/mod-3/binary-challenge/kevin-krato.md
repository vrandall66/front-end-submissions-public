### Evaluator: Travis Rollins
### Students: Kevin Krato
### Comments:
* Good number of commits
  * Some commits could still get broken out a bit like the tests
  * Good consistency with commit messages
  * Would be good to have a few more branches & PRs
* Nice work with the README
* No propTypes at all
* No linter errors though, nice work.
* Missing a 404 page.
* Very cool looking project, nice animations.
* Some duplicated data in currentSong and currentPlaylist
  * Keep track of the id in the currentSong. 
* Don't render components that don't exist.
  * Login, Register, genres, artists, etc.
* Would have liked to see some dynamic routing.
* Should separate reducers into their own files.
  * Double check naming of files as well.  Test file should match name of file it is testing.
* Lots of duplicate code in `AudioPlayer` file
* Good work with testing reducers
  * Missing tests with actions
* Missing container tests with mapStateToProps, mapDispatchToProps, etc. in `AudioPlayer.test.js`
* Missing significant amount of tests in `AudioPlayer.test`
* No tests in `AsideNav`


## Rubric

### Specification Adherence

* 2 - The application is in a usable state, but is missing part of one or more of the technologies outlined above. Evaluator has multiple recommendations for design changes.

### Project Professionalism

* 3 - PropType functionality is complete, the codebase has less than 5 linter errors, README has been updated with all group members. Project utilized wireframes from the outset. All git commits are atomic, made first to branches, and use descriptive and concise commit messages. Project demonstrates a fundamental understanding of React architecture.
* 2 - Project is missing PropTypes, README updates, wireframes, or has more than 5 linter errors. Project team makes large infrequent git commits. Project shows a basic understanding of React.

### Testing

* 2 - Nearly all unit tests for Redux and React are in place. No attempt to test async functionality was made.

### Redux Architecture

* 3 - Appropriate components are wrapped in connected Redux container components. The Redux store contains all necessary      application data. All state changes are handled through Redux actions and reducers.

### Routing

* 3 - Application uses React Router to display appropriate components based on URL.
