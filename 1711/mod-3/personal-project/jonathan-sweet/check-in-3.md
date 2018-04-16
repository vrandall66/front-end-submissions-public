## Project Name: Lost and Found

#### Check In: 3

#### Progress made?
* Passwords encrypted (sha256)
* Items and locations tables added to DB
* Report found/lost item form completed
  * Submission saves to DB
* Google map visible next to report form

#### What deliverables still need to be completed from your last checkin?
* Map markers populate location on report form

#### Next Steps?
* Add markers
* Add 'My Reports' component
  * Column of selectable reports that when clicked display the last known or found location on the map.

#### What are your concerns (if any)
* I swapped out `google-maps-react` npm package for `react-google-maps` which I felt has better docs. Not sure yet if this was a mistake.
* Report form submission with lat/lng marker data vs. traditional address - currently geocoding address, need to determine what to do when lat/lng is submitted and geocoding is not needed.

#### Deliverables for next checkin:
