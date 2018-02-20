## Project Name: Puzzle Swap

#### Check In: 3

#### Progress made?
Auth:
Can sign up/log in and sign out. User is stored in redux store with id and name. Post puzzle button only shows up when logged in.

Puzzles:
Post puzzle form posts text to firebase realtime database and images to firebase cloud storage. Puzzles update automatically on the front end and load whether someone is loggedin or not. Authorization in cloud storage does not allow images to load unless an authorized user is logged in. Puzzles also have a user associated with them.

Tests:
Testing for apicalls, reducers, action creators, and outlines/partial tests for all containers and components. Proptypes.

UI: 
Start to pivot to a white/gray/yellow theme. Style forms.

Chats:
Claim button leads to chat between owner of puzzle and logged in user. First checks to make sure a chat doesn't already exist, and makes one if it doesn't. Each chat has usernames and space for a timestamp and the most recent message. All of a users chats are displayed in inbox. Can't click on them or write in a chat. 

#### What deliverables still need to be completed from your last checkin?
More tests

#### Next Steps?

#### What are your concerns (if any)

#### Deliverables for next checkin:
