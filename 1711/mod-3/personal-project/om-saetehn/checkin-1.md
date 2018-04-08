## Project Name: 
Wisdom Cookies

#### Check In (what checkin number is this?)
1

#### Project Pitch
Choose wisdom to guide your fortune. No need for a Chinese carry-out, unlimited cookie everyday, one click away. Users can also save each wisdom in a jar to remind themselves again later. 

### Deliverables

#### Stack: 
React Redux, Router, External API

#### APIs:
http://forismatic.com/en/api/ (ran into issues with CORS, changed to the one below)
http://fortunecookieapi.herokuapp.com/v1/fortunes?limit=10&skip=&page=

#### Wireframes
![home](https://github.com/chunktooth/wisdom-cookies/blob/master/src/images/cookie-home-wireframe.png)
![opencookie](https://github.com/chunktooth/wisdom-cookies/blob/master/src/images/wisdom-cookie-wireframe.png)
![jar](https://github.com/chunktooth/wisdom-cookies/blob/master/src/images/jar-wireframe.png)

#### Waffle & Github
https://github.com/chunktooth
https://waffle.io/chunktooth/wisdom-cookies

#### Order Of Attack
- Fetching API and cleaning data to get a nice clean quote for two categories (based on a specified length)
- Implement a randomizer to generate clean quote data
- Implement a router to a 'jar' feature (favorite quotes)
- User can view previous quotes or trash them
- Photoshop realistic images of a jar, a left and right element for a fortune cookie and an iconic blue fortune cookie paper
- Implement an animation/image transition

#### MVP
- Generating randomized quotes after every click
- A feature to save favorite quotes and re-read them

#### Nice To Haves
- A router to a jar for re-reading past favorite wisdom 
- A transition of left and right cookie element opening and sliding outward to reveal the wisdom inside
- Log-in and sign-up feature to allow each user to revist their previously read wisdom
- If a quote is a greater than a certain length, users hit a jackpot and gets routed to a slighty different UI, possibly a moon cake.
- To make the app fully responsive

#### Biggest Challenges
- Getting more comfortable with Redux store && backend server and testing
- Integrating original images with animations for revealing and hiding wisdom

#### Instructor Notes

#### Deliverables for next checkin:
