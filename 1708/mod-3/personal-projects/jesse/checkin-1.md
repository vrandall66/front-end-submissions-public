## Project Name:

Crypto Vis

#### Check In: 1

#### Project Pitch

App that gives a user access to the coins they are tracking. The data will be presented with data vis that is easier to read than the most commonly used applications to date.

### Deliverables

#### Stack:

React-Native
Redux
Router
Firebase --> (Simple as possible backend?)

Some sort of data visualization / charting use of D3 ( one of or similar to VictoryJS / ChartJS / GraphQL )


#### APIs:

[Coin Cap API](http://coincap.io/coins/)


#### Wireframes

[Wirefame 1](./Login-page.png)
[Wirefame 2](./home-page.png)


#### Waffle & Github

[GitHub Repo](https://github.com/jessepackwood/Crypto)

[Waffle board](https://waffle.io/jessepackwood/Crypto)

#### Order Of Attack

1. Create a login page/route
2. Render Coin data for 1 day, 7 days, 30 days
2. Allow user to select a second coin to compare performance
3. Data vis rendering all coins with a growth comparison

#### MVP

User can create an account, login, track multiple coins. View graphs of at least two coins at one time. 

#### Nice To Haves

* Pull in user crypto portfolio

##### Unrealistically abmitious: 
* Overlapping graphs

#### Biggest Challenges

Keeping track of multiple users information
Consistent design for data vis

#### Instructor Notes: Cool idea! I like the data viz!

#### Deliverables for next checkin:

* Incorporate Firebase for user sign in 
* Be able to save a user in the store
* Be ablle to make a request to the API and save response in the redux store
* Set up testing environment
