## Project Name:

Bitpoll

#### Check In (what checkin number is this?)

1

#### Project Pitch

Bitpoll helps determine consensus within the Bitcoin development community by providing polls rescricted to developers of the Bitcoin project.

### Deliverables

Wireframe, Stack, API

#### Stack:

React
Redux
Router
Firebase
GitHub Auth

#### APIs:

GitHub API
https://developer.github.com/v3/repos/#list-contributors

#### Wireframes

![Not logged in](https://raw.githubusercontent.com/hmmChase/bitpoll/master/assets/bitpoll1.png 'Not logged in')
![Logged in, but not verifed developer](https://raw.githubusercontent.com/hmmChase/bitpoll/master/assets/bitpoll2.png 'Logged in, but not verifed developer')
![Logged in, verifed developer, not yet voted](https://raw.githubusercontent.com/hmmChase/bitpoll/master/assets/bitpoll3.png 'Not logged in')
![Logged in, verifed developer, voted](https://raw.githubusercontent.com/hmmChase/bitpoll/master/assets/bitpoll4.png 'Logged in, verifed developer, voted')

#### Waffle & Github

https://github.com/hmmChase/bitpoll

#### Order Of Attack

Initialize repo with:
create-react-app
Redux
Router
Enzyme
ESLint
SCSS

Intergrate Firebase
GitHub authorization

Build poll

#### MVP

Just have one poll to vote on what the blocksize should be

#### Nice To Haves

Ability to add and delete polls, organized in a table
Have a custom route for each poll

#### Biggest Challenges

Fetching all contributors to the Bitcoin repo
Building a poll from scratch

#### Instructor Notes

#### Deliverables for next checkin:

React, Redux, Router boilerplate
Add vote results to Firebase
Intial page with poll
API calls to get all contributors
