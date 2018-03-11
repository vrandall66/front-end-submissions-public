## Project Name: Travel Map

#### Check In #1

#### Project Pitch 
My app will be an interactive map and trip log for users who travel often or just want to show off where they've been over the course of a year. It will have themes for users to choose from to customize their maps. It will also feature a travel log where users can describe the reason for their trip and add a journal entry about the trip. 

### Deliverables

#### Stack:
JavaScript
React
React Router
Redux

#### APIs: 
[Google Maps](https://developers.google.com/maps/documentation/javascript/adding-a-google-map)

#### Wireframes
![Wireframes]('./Wireframes.pdf')

#### Waffle & Github
[GitHub](https://github.com/michellehoffman/personal-project)

#### Order Of Attack
1. Get api data and create a mock data file
2. User can set a hometown // Will load current location as default. 
3. Show a map of the US
4. Create a button for user to add travel location
5. Inputs for user to submit location and type of travel (air v. road) 
6. Towns are shown in text
8. Destinations are shown on map with pins
7. Total miles are calculated and displayed
8. Map has a default theme
9. User can scroll through additional themes
10. User can click on a specific state or region
11. User can see route in the url and use back button
12. In that state or region, user is shown their travel log
13. User can add a location from the state's page
14. User can see a timeline of all travel
15. User can access a settings page to reset their hometown

#### MVP
- User can input their hometown and travel destinations / app will default to current location unless specified by user.
- User can click on certain areas of the map to see data about their trip(ie. reason for trip/trip journal)
- Trip Log is functional and works with user location.
- Clean UI/UX 
- User can apply different themes to their map

#### Nice To Haves
- User can share their map on social media.
- User can log in with Firebase.
- User can upload pictures to their map.
- Map is available for all countries.
- Map suggests locations to check out.
- Multiple users can add to the same map.

#### Biggest Challenges
- Figuring out how to lay themes on top of the map with location accuracy
- Figuring out what to store in Redux 
- Figuring out how to click into regions and have a clean animation to the next screen

#### Instructor Notes
- Location information needs to be in redux 
- Travel Log info will live in redux store 

#### Deliverables for next checkin:
- Have test file started. 
- Have map loaded on page 
- Have location pullin and saved in store (lat and long is fine for now you'll need to convert to a city/state) 
- Build out search field 
