## Project Name: gyffy

#### Check In - 1

#### Project Pitch
In order to support the drivers who need alternative fuels, this app provides a resource to locate fuel stataions, whatever alternative fuel your vehicle needs.  Special support for military customers.

### Deliverables
responsive app with fuel-station search based on current zipcode and fuel type.

#### Stack:
React
Redux
Router

#### APIs:
http://developer.nrel.gov/api/alt-fuel-stations/v1/

#### Wireframes
mvp:
![Link To Wireframe](https://imgur.com/a/7lT8q69)

#### Waffle & Github
GitHub issues

#### Order Of Attack
Iteration 0: establish successful fetch call and render fuel stations based on electric charging in a given area code. Do not include government-access only. Prioritize styling for Iphone5.
Iteration 1: Add filter for specific harness types that correspond to high-speed charging. Include search functionality for non-electric alternative fuels. Add styling for laptop.  Add longintude/latitude search option.
Iteration 2: Add 500 mile trip functionality: User should be able to input two zipcodes limited to a 500 mile distance and see charging stations in starting locale, mid-point, and destination locale.  
Iteration 3: Add filtration functionality for co-locations/station-ownership:  e.g. owned by grocery store or Tesla
Iteration 4: Special filter for military use: military-owned stations, include non-electric fuel sources, eg: CNG.

#### MVP
User can enter current zipcode and preferred alternative fuel.  Search will provide 5 of the closest fuel stations with addresses (possibly the closest unless there is a high density in a given zipcode).

#### Nice To Haves
additional information about the station: e.g. type of payments accepted, hours of operation, etc.
option to enter starting and ending addresses for a journey and provide some alternative stations available along possible route

#### Biggest Challenges
Recognizing and adapting development as user empathy concerns/needs are more fully understood. 

#### Instructor Notes


#### Deliverables for next checkin:
1. Better prioritization for todos
2. Reorder the iterations after consideriation
3. Think about more pages and using Router for them
4. Mapping of Redux architecture
5. Simpl UI
6. Know what actions, reducers, store look like
7. repo on GitHub, file structure
8. Testing, linting, npm start work 
9. Do a fetch call
