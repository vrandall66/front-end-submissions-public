##
update from last checkin:

build file structure

add Login page

research Firebase auth and data storage




## Project Name:
Snowedin

#### Check In: 1

#### Project Pitch
Create a snowboarder friendly app that allows access to a multi-day forecast (snow report), traffic report and message board for ride share etc.

### Deliverables

#### Stack:
React and Redux

#### APIs:

Weather Unlocked API??
Weather Underground

Waze API?
Google Maps API

#### Wireframes
[Imgur](https://i.imgur.com/lr50ld9.png)

[Imgur](https://i.imgur.com/uL0Vwim.png)

#### Waffle & Github
Github Issues
#### Order Of Attack
1. create report
2. create forum per resort (ride share, sick runs, Apres-ski)
3. create route map to specified resort

#### MVP


#### Nice To Haves
Functional and appealing UI

#### Biggest Challenges
redux and message board

#### Instructor Notes

#### Deliverables for next checkin:


# Teacher Notes:

Ralph:

Name: SnowedIn

Description:
* Snowboard specific weather and chat app that allows users to connect and discuss rides, ski spots and apres plans

MVP:
* User account required
    * Must have email to contact ppl with
    * Email must unique
* Clicking a resort shows a resort-specific view
    * Weather report up top featuring 3 levels of weather data
        * Base, mid, upper mountain conditions
    * Main body of view shows chat window with 3 options to chat about:
        * Rides
        * Runs (but seriously who would give this info up???)
        * Apres
    * Clicking a specific message in any chatroom, will prompt user to open their email client and clicking that will open their preferred email client with the to: field already populating the correct email

Backend:
* Firebase

Auth:
* Yes
    * Google Auth
    * Email/Password

API:
* WeatherUnlocked
    * Resort-specific weather data
    * 3 levels of weather
Extensions:
* Scrape resort sites for specific lift information
* Add phone as a contact method to fire off text

Deliverables:
* Create new user
* Sign in / sign out
* Have a few routes built
    * Look at using dynamic routing
    * <Route to=‘/:resort-name/messages’ component={Messages} />
