Project Name: Bands in the Backyard

Check In: 3



Progress made?

-Redux is fully connected 

-Did more testing

-Render cards for location...having trouble rendering cards for the artists...not sure why because I know its recieving the correct information

-locally storing location

-When you search for an artist, it puts the concert that matches the location in local storage in the redux store

-styled more...having touble adding a background color to the page, so weird stuff happens when I try on App.js or Home.js...I think its something with router messing with it

-Router functionallity for home and artists work

-user can enter a location in and cards for that location show up...for now it has to be exact ie: 'Denver, CO'



Next Steps?

-Get artist cards to render

-Errors... i.e. user enters invlaid location or artist doesn't have a show coming up near them

-artists in local storage

-take location out of store since its locally stored and im not really using it anymore??

-finalizing styling on cards 

-continue testing

-fix user input so it doesnt have to be exact

-refactor LocationSearch and ArtistSearch into one component because the are exactly the same




What are your concerns (if any)

-My api to pull in all events for a certain location is kind of funky because the api takes in a number for the location rather than the location name so i had to build out a locationObject.js to convert the location to the number. I feel like this can cause problems

-getting concerts to show up in chronological order

-Feeling a little stuck/overwhelmed




Deliverables for next checkin:
* Good Job with Testing and Prop Types! Keep it up!!
* Continue Testing
* Styling
* Consider a drop down of available locations
* Possibly getting users current location on page load and loading events
* Functionality for rendering the artists

