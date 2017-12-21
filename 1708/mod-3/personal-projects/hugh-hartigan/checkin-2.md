## Project Name: Our Planet

#### Check In: 1

#### Project Pitch

* An app that identifies the top most engangered species by continent, making their situation digestible to the user. A prominent goal is also to relate how each particular animal's existence is important to the world ecosystem, specifically their benefit to humans in their region and/or worldwide. Each animal will have information on their habitat, estimated population, and the aforementioned benefit to humans, as well as high-resolution photos. Credit will be given to data gained from the World Wildlife Foundation, as well as for any photos used for each animal. Links will also be provided to direct users towards charities that work toward the benefit of animal welfare.

### Deliverables

* Build a backend
* Look into Nightmare if you want to scrape data
* Begin building out homepage and add some routes

#### Stack:

* React
* Redux
* Router
* SASS
* Node.js
* Knex
* Postgres

#### APIs:

* Personal Database API
* Google Maps
  * Reach goal: Watson Language Translator

#### Wireframes

* [Our Planet Wireframe](https://xd.adobe.com/view/a017c691-0ff2-4b78-979a-b5e5e64187b7)

#### Waffle & Github

* [Our Planet Waffle](https://waffle.io/HartiganHM/our-planet)
* [Our Planet GitHub Repo](https://github.com/HartiganHM/our-planet)
* [Our Planet BE GitHub Repo](https://github.com/HartiganHM/our-planet-be)

#### Order Of Attack

* Research `Knex`, `Express`, and `Postgres` to start setting up backend database
* Go through Mod-4 lessons and practice set-up
* Setup `our_planet` database
* Build `continents` and `animals` tables
* Build seed to populate tables with mock data
* Setup Postico to confirm data has been seeded properly
* Setup `api` for fetch requests
* Check request in Postman
* Finish building out database

* Research `Nightmare` docs and use case with building needed database

* Study dynamic routing for `Router 4`
* Build dynamic routes for animal and continents pages

* Build out homepage with basic links and `Header` component

#### Results from Deliverables

* Successfully built database in `postgres`
* Successfully built needed tables to store data
* Successfully seeded through all data, matching `animal` foreign id to `continent` primary id
* API listening to `localhost:3000` for fetch requests
* Alternate endpoints built for both `animals` and `continents` tables
* Get requests successfully pulling data in Postman
* Data mining nearly complete

#### Unfinished

* DB, table, and seeding setup took longer than expected, which delayed data mining
* Because data mining has not been completed, no frontend work is complete from last deliverables. However, I am confident I can setup dynamic routes and `Header` component quickly
* Initial confusion was with learning `knex` and `postgres` as it was new; no current questions or confusion with anything related to `react` or `redux`

#### MVP

* App displays animals with necessary info and images (of most importance is animals benefit to human life)
* Users are able to selectively view animals based on general location (ie continent)
* App links to charities
* Each animal has it's own page/component that displays its own information

#### Nice To Haves

* Each animal page will show general regional location through Google Maps API
* Global map that is interactive and displays animals by continent clicked
* Quick way to translate information to other languages (Spanish, French, German, Japanese, etc.)

#### Biggest Challenges

* Building database of necessary information (~40 animals)
* Dynamic routing to each animal information page/component
* Comprehensive UI/UX that makes information digestible, but meaningful

#### Instructor Notes

* Really great idea and great plan of attack!! 

#### Deliverables for next checkin:
