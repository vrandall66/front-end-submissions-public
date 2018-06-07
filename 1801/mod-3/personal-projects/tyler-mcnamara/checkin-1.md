## Project Name: Daytrip

#### Check In (what checkin number is this?)

Check-in 1

#### Project Pitch

Too many people travel to new cities and without a real plan, end up wondering aimless down the street, with nothing to do. I would like make an App that, with only a few clicks, plans their day for them based on a few preferences, bringing joy and purpose to these people's day.

Daytrip allows a user to search for an event or choose an activity category, in turn presenting 5 different plans to choose from. These plans provide a restaurant within walking distance with the best rating before the event and a place to go after, also walking distance. After selecting the plan, more details will be displayed about each stop along the way, including where to purchase tickets and location of each stop.  

Per the well known botanist George Washington Carver, "Where there is no vision, there is no hope". Daytrip brings vision to the visionless, fun to the boring, and a plan to the disorganized. 

### Deliverables

#### Stack:

React, Redux, Router, Middleware

#### APIs:

- Yelp
- Ticketmaster
- Google Maps

#### Wireframes
![image](https://user-images.githubusercontent.com/479463/40498845-6209a306-5f3d-11e8-8901-a15f95ff6b82.png)
![image](https://user-images.githubusercontent.com/479463/40498850-674ba602-5f3d-11e8-96d7-81489422ca39.png)
![image](https://user-images.githubusercontent.com/479463/40498857-6ac88ab6-5f3d-11e8-9bb4-5a2d1142ac24.png)
![image](https://user-images.githubusercontent.com/479463/40498865-6d5695c0-5f3d-11e8-888f-6a47ddac23ac.png)

#### Waffle & Github

https://waffle.io/mcnamara14

#### Order Of Attack

- Figure out the architecture of the app
- Determine what data is needed
- Setup React / Redux files and folders based on desired structure
- Fetch data and clean the data using search parameters
- Display daily plans

#### MVP

Ability for user to search for an event without any other filters and display 5+ plans with the ablity to select one which will provide more details about each stop.

#### Nice To Haves

Ability to search by event or by category with the additional of a filter for price range.

#### Biggest Challenges

- Understanding how to use each individual API as well as how to make them work effectively in combination. 
- Organizing the data coming in so that the "events" are filtered correctly and display in an easy to understand and useful way.

#### Instructor Notes

#### Deliverables for next checkin:
* Set up Firebase
* User logs in and must give a location
* Set up Redux and Router
* Make initial fetch and add data to the store
* Add a linter
* Start testing - test along the way
* Keep Wafffle up to date
* Start building out the UI
* store stucture - flat and try not to duplicate data
