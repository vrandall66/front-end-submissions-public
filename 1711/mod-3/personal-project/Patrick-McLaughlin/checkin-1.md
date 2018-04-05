## Project Name: fullSend

#### Check In 1

#### Project Pitch

An app that allows a user to track their mountain bike rides and view them by month or year. 
The app will pull in a user's strava information and trail information from MountainbikeProject to provide ride information.

### Deliverables

#### Stack:

* React
* Redux
* React-Router
* CSS
* Node Express
* postgres

#### APIs:

* Strava
* MTBProject

#### Wireframes

![main page](https://scontent-sjc3-1.xx.fbcdn.net/v/t1.0-9/29594928_10155516104136275_1427897049042386944_o.jpg?_nc_cat=0&oh=4f9ede72b7547b4a083335f8666a18ed&oe=5B6F20AC)

#### Waffle & Github

[Github](https://github.com/patrickmc21/fullSend)
[Waffle](https://waffle.io/patrickmc21/fullSend)

#### Order Of Attack

* Phase 0
  * Initial File Structure
* Phase 1
  * Setup Backend/OAuth for strava api
* Phase 2
  * Api calls
  * Clean Response data
  * Setup React/Redux/Router

#### MVP

* User should be able to sign in via Strava, and import activities from strava. 
* User can view activities by month, and each activity card will have information from both MTBproject and strava (date, mileage, time, pace, elevation gain, trail name, trail difficulty, trail summary, image of trail via mtbproject).


#### Nice To Haves

* User can look at the entire year of activities
* User can add ride details to each activity card (weather, trail conditions, riding partners, etc)
* User can upload their own photo to replace default trail photo on activity card
* User can click a `show more` button on each activity card that brings in additional strava/mtbproject info, as well as add additional photos
* App has a `bikes` page where a user can pull in their bike(s) information from strava so the user can keep track of mileage on each bike per month/year/lifetime
* `bikes` page allows a user to keep track of mileage on bike components, and allows them to update a component

#### Biggest Challenges

* Creating my own server/database
* Implementing OAuth for strava API use
* Chaining fetch calls from two different APIs

#### Instructor Notes

#### Deliverables for next checkin:
