## Project Name: BetweenFriends (working title)

#### Check In: 1

#### Project Pitch
  I noticed a problem when I scheduled a meeting with a mentor a few weeks ago - I could not convince google to show me coffee shops between where she worked and Turing.
  
  BetweenFriends solves that problem. Instead of searching google for your location and trying to shuffle the map to show what you want, BetweenFriends lets you enter two addresses to create a search area for what you want. There won't be results 2 miles in the opposite direction of your friend's location, only locations that are convenient for both people.
  
  As the project grows, users of BetweenFriends will login to save their locations and associate locations with their friends. Our frequent locations like work, school, or home don't change often, and BetweenFriends remembers these locations and those of your friends. Using these saved locations, users can quickly find a place and meet instead of spending time searching.
  
  Traffic can affect where you want to go - BetweenFriends has a stretch goal of importing live traffic data and calculating the actual travel time between the two starting locations. In a rush? Users can pick a location that takes the same amount of time for both participants.
  
  As an ultimate stretch goal, BetweenFriends allows users to send notifications directly from the app to the other person selected from their Google contacts. Scheduling in advance? Send a Calendar invite. In a rush? Fire off a text message and start walking.
  
  BetweenFriends takes the hassle out of finding a meeting location that's convenient for both of you.
  
  
### Deliverables

#### Stack: React, Router, Redux, Node, postgres

#### APIs: Google Maps (Maps, Places), Custom user API, Google Maps (Directions), Google Contacts

#### Wireframes 

#### Waffle & Github
https://waffle.io/rufusasterisk/betweenfriends
https://github.com/rufusasterisk/betweenfriends

#### Order Of Attack
  The first order of business is determining the math to properly query the google APIs for the data required.
  Developing a scaleable UI for the project is required - the stretch goals must be loosely planned before first stage designs are set - avoiding a large UI rework as part of a stretch goal will waste too much time.
  The first two steps hit MVP. This first stage relies largely on technologies that are familiar from previous projects. Building a node server to host a postgres DB is unlike any other project and will require significant work outside of course materials.
  With a DB in hand, start storing logged in users places generically. Add options to create friends and associate locations with friends as the project grows.
  
#### MVP
  The minimum viable product allows users to search Google places for anything they would like inside a circle centered between two manually entered locations with a diameter of their distance difference.

#### Nice To Haves
  A place to store user data that isn't local storage.
  Traffic data for travel times would be huge
  I would _love_ to integrate contacts so people can save locations based on their google contacts to the local db.

#### Biggest Challenges
  The google maps API and Places is friendly to this idea - maps sends back GPS coordinates of locations searched, and Places allows calls based on a GPS location and a search radius.
  The biggest challenge will be hosting a node server for a custom built API on postgres. I'm familiar with SQL and have a lot of experience working with large data sets, so it does not seem an insurmountable challenge.

#### Instructor Notes

#### Deliverables for next checkin:
