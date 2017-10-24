## Project Name: Happy Now?

#### Check In: 1

#### Project Pitch:  
I want to create an app to list any happy hours that are happening at bars and restaurants around a user.  However, I will only be able to display happy hours that are listed on foursquare.  I would also like to include the food menu for any restaurants that have it listed as well.

### Deliverables

#### Stack: 
React 

Reducx 

Router 

Node.js?

#### APIs: 
[foursquare](https://developer.foursquare.com/docs)

[GoogleMaps](https://developers.google.com/maps/documentation/javascript/tutorial)


#### Wireframes
![Homepage](wireframes/1.png)

![Mappage](wireframes/2.png)


#### Waffle & Github
[GitHub](https://github.com/NikBorn/happy-now)

[Waffle](https://waffle.io/NikBorn/happy-now)

#### Order Of Attack

Build out a boilerplate of all components

Learn how to make an API call with Node.js(make an intial call for bars/restaurants based on current location)

Get familiar with googlemaps(insert the sample map)

Connect Array of locations to display using google maps

Display list identifying closest locations and highlight those with current or upcoming happy hour.

Have link to location showing happy hour specials and food and beverage menu.

#### MVP

(worst case scenario, there is no uniform way to dig into happy hour specials)

search for closest restaurants and bars

display those locations on a map

have a list of locations

have a link to location page displaying 
inforamtion and menu(where restaurants/bars have a menu listed on foursquare)

#### Nice To Haves

Backend for users to save favorite locations.

#### Biggest Challenges

Implementing Node.js and google maps for the first time.

Digging into the menu on foursquare to identify the happy hour specials.

#### Instructor Notes

- Nice to have would be the ability for users to vote on what happy hour they want to go to 
    (firebase can give this to you for free basically) 
- Look into react-foursquare and see if thats working 

#### Deliverables for next checkin:

- Determain if API data is good 
    - ideally you can make a request 
- have the map loading with the current location 
- have redux and react set up 
  -store should be loaded with some of the available happy hours
  - look into favoriting. 
- get the google cloud vision api hooked up 


