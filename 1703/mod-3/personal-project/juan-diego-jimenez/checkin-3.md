# Lit Wellness Game

#### Check In: 1  

#### Project Pitch :

###### Description

* Make Turing's wellness challenge into a game.
* Great UI/UX to attract more users

###### Sugar and spice!

* Accountability buddy that bets both points (win double or both lose)
* Other players motivation poke/claps

###### Features

* Users can track their own scores
* Easy form to add daily challenge
* Easy way to toggle completed challenge
* Dashboard of progress and notifications
* Cool UI that shows other players scores and challenges
* Recommendations of challenges (saved tags, autocomplete)
* Challenge of the week for extra points
* Rewards to add extra challenge to other players

### Deliverables  

| Stack                   |
|-------------------------|
| React                   |
| Redux                   |
| React Router            |
| Recharts                |
| firebase or express     |
| React styled components |

#### APIs:  

Own backend (firebase or express)

#### Wireframes  

* See sketch

![Wireframes](wireframe/wireframe.png)

#### Waffle & Github

[Waffle Link](https://waffle.io/jdiejim/wellness-challenge)

[Github Link](https://github.com/jdiejim/wellness-game)

#### Order Of Attack  

| Attack                       | Status    |
|------------------------------|-----------|
| Build database schema        | pending   |
| Choose a backend             | completed |
| Home page with instructions  |           |
| Build main components        |           |
| Setup Redux                  | completed |
| Setup Router                 | completed |
| Router map                   |           |
| Sign Up                      |           |
| Login                        |           |
| Profile and dashboard        |           |
| Display users data           |           |
| Add challenges               |           |
| See other people challenges  |           |
| Score calculation            |           |
| Challenge completed logic    |           |
| Displays leaders             |           |
| Unit testing                 |           |

#### MVP

###### Overall

* Track and persist personal wellness data
* See other players scores and progress
* Add challenges
* See other peoples challenges
* user is saved in backend
* tests for your backend
* tests for the front end

###### Dashboard

* Display rest, sweat, nutrition, wellness charts
* Display personal score
* Display day's challenges
* Easy completed toggle

#### Nice To Haves

* Leaders UI to see who is winning
* Rewards - adding challenges to other players
* Challenge of the week
* Accountability buddy!
* Recommendations for challenges
* Display calendar
* Private groups
* Motivation poke/claps
* Sockets

#### Biggest Challenges  

* Add a backend for saving data in a database
* Score calculation (overall math logic)
* Charts
* UX animation
* Race UI
* Calendar persisted data
* Rewards logic
* Accountability buddy logic

#### Instructor Notes

#### Deliverables checkin1

| Checkin 1           | Status    |
|---------------------|-----------|
| Node.js and Express | completed |
| Knex with PG        | completed |
| Bookshelf           | pending   |
| Backend testing     | pending   |
| OAuth               | pending   |
| React Setup         | completed |
| Redux Setup         | completed |
| Router Setup        | completed |

#### Deliverables checkin1

| Checkin 2                | Status                    |
|--------------------------|---------------------------|
| BE: Build pending tables | 1 table pending           |
| BE: add Bookshelf        | pending  (finishing knex) |
| BE: Backend testing      | pending                   |
| BE: OAuth                | pending                   |
| FE: Side Bar with Routes | completed                 |
| FE: Login w/ post        | completed                 |
| FE: Sign Up  w/ post     | completed                 |
| FE: Get Users activities | completed                 |

#### Next Potential Deliverables

| Checkin 3                | Status    |
|--------------------------|-----------|
| BE: Build pending tables |           |
| BE: add Bookshelf        |           |
| BE: Backend testing      |           |
| BE: OAuth                |           |
| BE: get weekly scores    |           |
| FE: Activities UI        |           |
| FE: update act status    |           |
| FE: Leader UI            |           |
| FE: Begin with charts    |           |
| FE: Finish Homepage      |           |


#### Instructor Summary Checkin 1

- Have your backend set up
    - look into Node.js / express
    - Knex with PG && Bookshelf
    - look into testing (it's super easy I Promise.all)
    - have your tables set up
        - look into OAuth -> [auth0]('https://auth0.com/docs/quickstart/spa/react/01-login')
- Have your initial react, redux, router setup (boiler plate)

#### Instructor Summary Checkin 2

So I saw what you've completed and thats amazing! One thing that might help you in your quest is to make some seed data so that you can have a populated DB once everything is set up. Setting up your associations isn't going to be too difficult with Bookshelf.

TBH I don't think I have much to add to your PR. I think that if you focus on getting your tables set up correctly the moves in the front end will be pretty easy. Great job. Let me know if you run into any snags and we can 🍐 next week on some stuff!
