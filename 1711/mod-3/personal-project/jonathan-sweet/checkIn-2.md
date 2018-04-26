## Project Name: Lost and Found

#### Check In: 2

#### Progress made?
* Initial landing page complete
* DB schema created
* Created users DB with postgreSQL/Knex
* Emailed lostAndFound API creators about using their API, issues with examples on the site. 
* Started to explore Google Maps Javascript API and Google Maps Web Services API

#### What deliverables still need to be completed from your last checkin?
n/a

#### Next Steps?
* Add tables for items and locations
* Create report form (must be logged in)
* Display map with marker of found item location

#### What are your concerns (if any)
* Using promises with Google Maps Javascript API - NPM packages available (google-maps-react)
* Allowing users to upload image (drag and drop?)

#### Deliverables for next checkin:
* Encrypt password prior to sending to DB
* Add items & locations tables to DB
* Report Found Item form
  * title
  * description
  * lat/lng
  * date
  * reward?
  * Saves to DB upon submission (new item row; new location row or add item_id to existing location)
* Google Maps - drop marker to populate lat/lng on form
