## Project Name: Geard

#### Check In: 2

#### Project Pitch

Living in Colorado, there are so many adventures to be had outside. The problem is, most of these adventures require expensive gear. There is so much gear that I would love to have, but can't afford. An alpine touring set up for skis can cost well over $1,200, and that is money that I don't have. On the other hand, I shelled out almost $200 for my backpacking pack, and it spends 90% of the year sitting in my basement. What if we could rent the gear we wanted at a reasonable price from fellow adventurers? This is where Geard comes in. Connecting adventurers and explorers alike, users can now rent anything from backpacks to climbing guides, and everything in between.

### Deliverables:

I wasn't given a deliverable for Check In 2, and I don't have much to actually turn in. I have spent my time so far trying to wrap my head around how I am going to organize my data and how to implement node modules to help me accomplish my goals. I think I finally have a handle on how to structure my data. Each user object will have a property that is an array of gear objects that they own called 'forRent'. Those objects will have a property of 'rented' which will be a boolean. Each user object will also have a property called 'renting' that is an array of any gear objects that they are currently renting.

I have started trying to implement Firebase, I have downloaded react-dates from airbnb, set up my react router and gotten my redux file structure set up.

#### Stack:

* React/Redux starting fresh with create-react-app(I really want to write a mobile platform in React Native, but I don't think I will have time)

#### APIs:
 * Google Maps API and navigator.geolocation object

#### Wireframes
 * [Desktop Wireframe](https://i.imgur.com/lLrk5B2.png)

#### Waffle & Github

[waffle](https://waffle.io/jackmallahan/geard) [repo](https://github.com/jackmallahan/geard)


#### Order Of Attack

* Set up components and actions.


#### MVP

* A searchable site that a user logs into and can search for and post gear online.


#### Nice To Haves

REACT NATIVE

#### Biggest Challenges

* Checkout process
* Login w/ Facebook
* Geolocation
* Google maps API to show where gear is located
* Mocking location for mocked gear
* Search gear by Activity

#### Instructor Notes

#### Deliverables for next checkin:



# Teacher Notes:

Jack M:

Name: Gear’d, Geard

Description:
* Adventure gear rental from everyday ppl. People with gear can submit gear for rental, people without gear can find and rent gear through the app. Payment submission likely mocked/faked.

MVP:
* Owners can post gear
    * See which gear is currently available for rent and currently being rented
* Renters can search gear
* Renters can select and rent gear for X amount of time
    * Renters can see current rentals on their profile
* Notices for renters and owners when gear is overdue
* Search functionality for gear
    * Likely require tags
* Location considerations

Backend:
* Firebase

Auth:
* Yes
* Roles
    * Owner and/or Renter

API:
* Potentially google API to be able to search gear by location
* Sierra trading post API?

Extensions:
* Actually accepting payment
* Ability to also sell things outright (triggered by user)
* Direct message between users
* Use prefix tree to autocomplete gear
* Ability to source product descriptions from Sierra trading post API

Meeting 2:

Deliverables:
* Auth working (firebase)
* Build out dynamics route to member profile
    * <Route to=‘/geard/profile/:id’ component={Profile} />
* Ability to add a product (even just Title/Body) and have it stored in user profile
