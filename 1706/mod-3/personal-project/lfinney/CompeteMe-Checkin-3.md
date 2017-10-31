## Project Name: CompeteMe

#### Check In: 1

#### Project Pitch: 
In recent decades, pick-up sports competitions have become ways for individuals to build community and get some exercise, while engaging in a a bit of friendly competition in the process. However, the "pick-up" nature of relying on word of mouth and strangers to come to together at a park keeps pick-up sports communities small. I believe that more people would play in these types of events if the process were more streamlined. I know I would. CompeteMe seeks to do just that. Allow a user to pick a park, create a competion, and invites others to join them.

### Deliverables

#### Stack:
React, Router, Redux, Firebase

#### APIs:
Google Places API

#### Wireframes:
![CompeteMe wireframe](https://user-images.githubusercontent.com/22566946/31972918-6bc39310-b8e0-11e7-9d95-c0764ee211a3.png)

#### Waffle & Github:
[Github Repo](https://github.com/lfinney/competeMe)

#### Order Of Attack
~~1) Finalize wireframe~~
~~2) Setup routes to major sections of page~~
~~3) Begin building wireframe in app using react components while also installing necessary dependencies~~
4) Successfully make an API call to Google Places and see if I can search for a park. It appears as if there is already a filter in place that will limit searches to parks, so that's neat.
4.5) Use google places autocomplete in park search
5) Determine optimum locations for each piece of data be it store, state, or firebase
~~6) Create controlled user profile component and pathing~~
6.5) In general, refine overall website paths. They are quite simple now.
~~7) Set-up Redux store where info from controlled form components can be placed (Should I set this up earlier?)~~
8) Refine CSS across the board, but mostly for event cards
~~8) Have event cards populating from ~~store~~ firebase~~

#### MVP
- Users can create and join sporting events
- When creating an event a user should be able to pick a sport, select a number of participants, select a time of day, and select a park to play at using Google Maps Places API. 
- Whatever park is selected by the user it should display on the event card.
- There should be a user profile page.
- There should be three places for an event card to live. In all places, these cards should be in chronological order:
  - Upcoming
  - User-joinged Events

#### Nice To Haves
- Nothing new.

#### Biggest Challenges
- Running into cors issues trying to make my google api requests function as I want them to. 
- Managing the flow from component to store to firebase is a lot to take in and navigate
- Testing environment is not currently working.

#### Instructor Notes

#### Deliverables for last checkin:

~~get firebase hooked up~~
 - ~~set up user~~
 - ~~user can't move forwared without being logged in~~
- ~~set up router, redux, react~~
- get google maps hooked up
  - it would be sweet if you could get the current location displayed on the map 
  *- currently in the midst of reading through api documentation from google*
- ~~start the controlled form and submit an event to firebase~~

######## Deliverables for next checkin:

- Firebase werk 
  - Set up the user interactions  
    * ~~user can log in.~~
    * ~~user can submit an event.~~
    * user can join an event. 
- Google Maps 
  - user can search for location on the map 
- ~~Redux~~
  -~~Redux store is populating with events from Firebase.~~
- Testing 
