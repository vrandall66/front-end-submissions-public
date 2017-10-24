## Project Name:

Finance Portfolio Game - to be named at a later date

#### Check In: 1

#### Project Pitch

App that gives a user access to a game that tracks an imaginary stock portfolio and tracks gains / losses against all other users on a leaderoard. 

### Deliverables

#### Stack:

React
Redux
Router
Firebase --> (Simple as possible backend?)

Some sort of data visualization / charting use of D3 ( one of or similar to VictoryJS / ChartJS / GraphQL )


#### APIs:

[IEX Trading Financial information API](https://iextrading.com/developer/docs/)


#### Wireframes

In progress

#### Waffle & Github

[GitHub Repo](https://github.com/AdamMescher/MoneyTree)

[Waffle board](https://waffle.io/AdamMescher/MoneyTree)

#### Order Of Attack

1. Create search bar that allows user to show stock information of individual stock
2. Add ability to buy and sell stocks at current price
3. Track user portfolio's gains and losses over time
4. User dashboard with major financial news, data viz of current state of portfolio
5. Add ability to have login / logout to allow multiple users
6. Have a leaderboard page in which all user's current portfolio worth is displayed
7. User can create a group in which only the scores of members are displayed on the leaderboard. Invites sent via email.


#### MVP

User can create an account, login, track stock portfolio value over time and compare their score to all others in the game. 

#### Nice To Haves

* Fancy stock ticker
* Inclusion of data from sources other than IEX
* What if game where user can pick date to invest in company in the past and see how much they would have gained / lost
* Ability to pull financial statements from SEC's EDGAR and display in PDF form 
* Microtransactions via Stripe API for if bankrupt player wants to try again

##### Unrealistically abmitious: 
* use OCR to create financial statement components
* Implement more complex securities like commodities and allow options trading
* Suggest stocks based on current makeup of user's portfolio


#### Biggest Challenges

Keeping track of multiple users information
Coherent design of multiple visualization components

#### Instructor Notes

#### Deliverables for next checkin:
