## Project Name:

Accountable - Colorado political accountability App

#### Check In: 1

#### Project Pitch

App that lets Colorado voters search and contact their lawmakers and see how they vote 

### Deliverables

#### Stack:

React
Redux
Router
Geolocation
Data viz library like D3
Mapping library like D3-maps/leaflet/carto
Possible Firebase (if extension reached for lawmaker donors)

#### APIs:
[Open States API](http://docs.openstates.org/en/latest/api/index.html)

#### Wireframes

[Basalmiq Wireframe](https://balsamiq.cloud/sugro/pn0c9)

#### Waffle & Github

[GitHub Repo](https://github.com/mariastlouis/accountable)

[Waffle board](https://waffle.io/mariastlouis/accountable)

#### Order Of Attack

1. Make a search bar to let people search for individual lawmakers
2. Make details pages for the individual lawmakers that includes:  
* Photos
* Email address
* Web page
* Physical address
* Phone
* Occupation
* Committees 

3. Use geolocation and put on home page to find lawmakers
4. Build out maps on the home page to show where the location is
5. Add additional committee data including: 
* Committee name 
* Committee members w/ links back to lawmakers

6. Add additional bill tracker data
* Tie in sponsored bills to lawmaker details page
* Start separate page that just tracks the bills  

#### MVP

User can search for their address or use geolocation to find details on their lawmakers 

#### Nice To Haves

* Robust bill tracker that allows people to easily find bills they are interested in. 

##### Unrealistically abmitious: 
* Get contribution data from Colorado Secretary of State and make a backend database to include lawmaker contributions on their details pages. 

#### Biggest Challenges

Getting all of the routes set up for individual lawmakers
Connecting the data between lawmakers/committees and votes on bills

#### Instructor Notes
* Love the idea.... cant wait to see how this turns out! Great job on having such a detailed plan.

#### Deliverables for next checkin:
* Have basic structure of front-end built out with route to individual lawmaker
* Set up redux, and have data in the store 
* Set up testing environment
