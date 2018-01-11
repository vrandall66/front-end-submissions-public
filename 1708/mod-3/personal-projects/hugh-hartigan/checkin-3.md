## Project Name: Our Planet

#### Check In: 1

#### Project Pitch

* An app that identifies the top most engangered species by continent, making their situation digestible to the user. A prominent goal is also to relate how each particular animal's existence is important to the world ecosystem, specifically their benefit to humans in their region and/or worldwide. Each animal will have information on their habitat, estimated population, and the aforementioned benefit to humans, as well as high-resolution photos. Credit will be given to data gained from the World Wildlife Foundation, as well as for any photos used for each animal. Links will also be provided to direct users towards charities that work toward the benefit of animal welfare.

### Deliverables

* Finish seeding the data and creating any endpoints you need
* Have a functioning UI that has multiple routes and is connected to the redux store
* Test all the things
* Have eslint file set up
* Add search functionality for animals

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

##### Complete BE
* Complete sourcing all animal/continent data (including images)
* Final clean of data
* Build middleware for API fetch
* Feed data to FE application from BE application
* Look into hosting BE on Heroku

##### FE Build Out Phase 1
* Build out assumed components and basic file structure
* Render `Header` on the page
* Successfully load BE data to redux store
* Render `Card` components on home page with animal name and image

##### Testing Phase 1
* Test `Header` component
* Test helper functions and API calls
* Test reducers and actions
* Run linter

##### Design
* Design project logo and basic branding

##### FE Build Out Phase 2
* Build out `Search` component, actions, and reducers for home page to filter animals
* Style `Card`, `CardContainer`, and `Search` components
* Setup SASS structure including `variables` and `mixins`

##### Testing Phase 2
* Test `Card`, `CardContainer`, and `Search` components
* Test all added actions, reducers, and helper functions
* Run linter

##### FE Build Out Phase 3
* Build dynamic routes to `AnimalPage` when animal is clicked from root
* Render animal data based on what animal is clicked and routed too
* Style `AnimalPage` component

#### Results from Deliverables

* Successfully built database and completed server functionality
* Strong beginnings of FE application with basic UI/UX
* Search functionality that will work with all animals and can be implemented across the application
* Testing built out for most components, actions, reducers, and helper functions
* Basic design and color scheme established

#### Unfinished / On the Chopping Block

* Have yet to test BE application
* Build out `ContinentPage` and `Map` component
* Testing Phase 3 (`AnimalPage`, `ContinentPage`, `Map`)
* Build `AboutPage` component
* Looked into Heroku for BE, but need help with hosting complications
* Need a faster way to load images to FE application (initial load of homepage or re-rendering is slow)

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

#### Instructor Notes:

#### Deliverables for next checkin:
* Have yet to test BE application
* Build out `ContinentPage` and `Map` component
* Testing Phase 3 (`AnimalPage`, `ContinentPage`, `Map`)
* Build `AboutPage` component
* Looked into Heroku for BE, but need help with hosting complications
* Need a faster way to load images to FE application (initial load of homepage or re-rendering is slow)
* Be able to click home button and re-render all the animals
