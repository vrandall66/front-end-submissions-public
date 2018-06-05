**Check In (what checkin number is this?)**
Initial checkin 1 

**Project Pitch**
Sports betting apps are often confusing, full of ads, and incredibly annoying. This app will make it possible to maintain a bet over the course of an entire season. It is designed to be a betting app for friends, with no daily pools, fantasy leagues, or confusing scoring systems. One can simply create a league, invite friends, pick teams and sit back. Users will have the ability to track their teams progress throughout the course of the season. 

**Deliverables**
wireframes
tech stack 
overall plan 

**Stack:**
Firebase 
Connex 
React
Redux 
Web sockets 

**APIs:**
https://developer.sportradar.com/docs/read/NBA_API
https://developer.sportradar.com/files/indexSoccer.html#soccer

**Wireframes**
[link to my wireframes](https://imgur.com/a/TnlNiaQ)

**Waffle & Github**
https://trello.com/b/rmpTtSAz/sports-app

**Order Of Attack**
Iteration 0: Build back end
Iteration 1: Create login system
Iteration 2: pull/clean/display data from the sportsRadar API 
Iteration 3: REACT it (with TDD) 
Iteration 4: hopefully web sockets but if not find another temporary solution to handle draft events

**MVP**
An app that displays sports data and lets one user create a league and pick teams for everyone in the league

**Nice To Haves**
Live draft feature  using web sockets 

**Biggest Challenges**
Building a backend and getting web sockets to work as I hope. 


**Instructor Notes**

**Deliverables for next checkin:**
- React/Redux/Router boilerplate setup
- 1st API call for pulling back available NBA teams
- 2nd API call for pulling back W/L for each team
- Firebase setup to save drafts
- UI:
   - Page for creating a new league/draft
   - Page for actively drafting
   - Page for tracking results of live league
