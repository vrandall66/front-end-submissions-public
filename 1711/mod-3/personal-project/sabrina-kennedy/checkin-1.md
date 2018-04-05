## Project Name: Skywatch

#### Check In :1

#### Project Pitch:
Build an interactive learning experience app for people learn about space-x and its missions.  

### Deliverables
#### Stack:

React
Redux
Router
middleWare/saga
scss

#### APIs:

Space-x api: https://github.com/r-spacex/SpaceX-API/wiki
possible apis for extentions: 
https://developers.google.com/youtube/v3/ 
https://newsapi.org/


#### Wireframes

![wireframe-homepage](https://scontent-sjc3-1.xx.fbcdn.net/v/t31.0-8/29749367_902481468988_5020603432154058323_o.jpg?_nc_cat=0&oh=07aeeda2d3b7502306a08eb444a383fd&oe=5B386F97)

#### Waffle & Github

[waffle](https://waffle.io/skenne21/sky-watch)
[Github](https://github.com/skenne21/sky-watch)

#### Order Of Attack

Fetching data from API and setting up user information
set up logic for passing the information in-store/actions/reducers
move fetch call into middleware/sagas
fetch on search
setup routes and paths on button clicks
displaying information
saving user information in a login
loading image when fetching data

#### MVP
allow the user to be able to click on different areas of interest, company information, rockets, launches, and capsules data.
the user can bookmark information, to check again at a later date.
the user can save information and is reloaded on page load

    
#### Nice To Haves:
Use news API to allow the user to search for recent news articles on space-x.
Use youtube API to pull in video content of space-x launches.


#### Biggest Challenges
getting content to be fun and interactive. 
making the project scalable.
working with saga or middleware.


#### Instructor Notes

#### Deliverables for next checkin:
boilerplate setup with redux, react, router
initial routes working for the homepage and other locations
create more wireframes for what the project looks like overall
have design ideas solid
API request and set in store
