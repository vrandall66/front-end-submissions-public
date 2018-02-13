## Project Name: 
Twitter Gazette (or Gazetter)

## Check In One

#### Project Pitch
- Love the news, but hate the newsfeed?  
- The Twitter Gazette is for people who like to read the news through Twitter and yet find the newsfeed overwhelming. For every user, the Gazette will curate their most relevant newsworthy tweets from the Twitter API based on features such as: likes, retweets, credentials, proximity, etc. 
- The Gazette will pull in tweet content as headlines for a "front page" of a newspaper that is independent of news outlets. Ideally it will have sections like a traditional newspaper, such as Local News. 
- The desktop design will mimic that of a print newspaper. The mobile site will have some of the same flourishes as the desktop but be optimized for people on the go.

## Deliverables

#### Stack:
React
Redux
Router
Firebase

#### APIs:
Twitter (realtime tweets)

#### Wireframes
On paper

#### Waffle & Github
https://github.com/nogully/gazetter

#### Order Of Attack
- Create React app and set up Router & Redux
- Explore Twitter API and map out endpoints to fetch
- Figure out Firebase and OAuth
- Sign in users
- Get all of a user's tweets on the page
- Design front page
- Filtering tweets based on content, likes etc
- Display content by scraping link content
- Use character length to determine styling on the page


#### MVP
An app that pulls tweets from a user's feed and displays 1 page of trending news tweets. 

#### Nice To Haves
- Ability to scrape the content of links that are embedded in those tweets and display those as articles rather than tweets. 
- Not just 1 page, but multiple pages based on topic. 
- Local news section that would be somewhat location-based. 
- Ability to interact with tweets on the site, liking articles and sending tweets from the page.  

#### Biggest Challenges
- Authentication
- Using the page to send tweets
- Scraping external website data
- Deciding on criteria to curate tweets
- Writing algorithm to curate tweets

#### Instructor Notes

#### Deliverables for next checkin:
