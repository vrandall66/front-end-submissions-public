## Project Name:

Stella Via

#### Check In: 1

#### Project Pitch

A mobile app for stargazers that will take a user's geolocation or allow them to search for a location and show them what they can see in the night sky with their naked eye and with a telescope, taking light pollution into account.

### Deliverables

#### Stack:

React Native
Redux
Router
Firebase (if we get to the backend features) (probz node)

Possibly data visualization map with light pollution data


#### APIs:

[NASA API] (https://api.nasa.gov/)
[Google Maps API](https://developers.google.com/maps/)


#### Wireframes

(Paper copies)

#### Waffle & Github

[GitHub Repo](https://github.com/katiescruggs/stella-via)

[Waffle board](https://waffle.io/katiescruggs/stella-via/settings/sources)

#### Order Of Attack

1. Create homepage for our app in React Native that displays NASA's Astronomy Picture of the Day, takes in a user's geolocation and allows them to search for a location.
2. Create stargazing landing page with route links to Constellations, Planets, Satellites, Moon Phase, and Events.
3. Create pages for Constellations, Planets, Satellites, Moon Phase, and Events that display information based on the location of the user and the API data.
4. Integrate light pollution data and maps to help users decide where they should go for best stargazing experience.

#### MVP

User can go to the App and see multiple options for what they can view in the sky that night.

#### Nice To Haves

* User can login and have a record of what they have viewed (will need a backend).

##### Unrealistically abmitious: 
* Additional feature where user can search for stars, constellations, or other astronomical bodies and get information about them (like Wikipedia but FOR STARS).
* User can favorite stars, constellations, etc. and see them quickly later.
* User can communicate with other star gazers on a message board.

#### Biggest Challenges
* learning React Native
* getting multiple APIs to work together 

#### Instructor Notes

#### Deliverables for next checkin:

- have a landing in react native built 
- hook up redux. 
- look into testing 
- look into light pollution data and see if you can find an api 
    - if not you'll have to scrape. 
