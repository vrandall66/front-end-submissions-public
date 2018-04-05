## Project Name: Ghibli Box

#### Check In: 1

#### Project Pitch  
Utilizing the Studio Ghibli api to make an application that allows users to view films, people, and locations. 

### Deliverables  
- This markdown
- A wireframe of the project
#### By Monday: 
- Boilerplate setup
- Switch/Route setup in App.js
- Redux wired in
- At least 1 API call being made
- API call(s) are getting sent to Redux store
- Updated, fleshed-out wireframes

#### Stack:  
- React
- React-Redux
- React-Router
- ESLint
- Jest
- Enzyme
- Sagas middleware

#### APIs:  
[Studio Ghibli API](https://ghibliapi.herokuapp.com/#section/Studio-Ghibli-API)

#### Wireframes  
![Wireframe image](https://i.imgur.com/wlGESO8.png)

#### Waffle & Github  
[Github](https://github.com/Kc2693/Ghibli-Box)  
[Waffle](https://waffle.io/Kc2693/Ghibli-Box)

#### Order Of Attack  
- API calls being made in general
- API calls cleaned into desired format to return. In this order: Films, People, then Locations
- Write API-calls tests
- Put API cleaned objects in Redux Store
- Start making React components. Get Films displayed on page
- Bring in React-Router, work on User Sign-in/Signup
- User favorites with Router
- Put user favorites in Store
- Put user and their favorites in LocalStorage
- Bring in People data to display & favorite
- Bring in Locations data to display & favorite
- Write a lot of tests for React/Redux stuff
- Do CSS


#### MVP  
- A user can sign in, view films, favorite films on the main /films page and go to /favorites and view their favorite films. User data persists through a reload. 

#### Nice To Haves  
Some sort of search or filter that covers all 3 categories (films/people/locations)

#### Biggest Challenges  
- Nested fetch calls
- React-Router makes no sense
- Tests are scary

#### Instructor Notes

#### Deliverables for next checkin:
