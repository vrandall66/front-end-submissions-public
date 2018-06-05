## Project Name: Tone of Voice 

#### Check In 1

#### Project Pitch
Tone of Voice is an app that allows you to compare different headlines in the US to see the general tone about specific issues and how they differ.

### Deliverables

#### Stack:

* React
* Redux
* React-Router
* CSS
* SCSS

#### APIs:
* Watson API
* [News API](https://newsapi.org/)

#### Wireframes
[WireFrame](https://balsamiq.cloud/s2o5kjc/p6gdpzv)

#### Waffle & Github
[GitHub Issues](https://github.com/JackLaird0/tone-of-voice/issues)

[GitHub](https://github.com/JackLaird0/tone-of-voice)
#### Order Of Attack
* Iteration 0
  * Set up file structure
* Iteration 1
  * Make api calls/test
  * Set up watson api for text analysis
* Iteration 2 
  * Create home page of app
    * Contains trending topics
    * Search bar for finding articles
  * Organize components and set up nav links

#### MVP
* User should be able to search for articles with keywords
* User should be able to click on different articles to compare them. 

#### Nice To Haves
* Sign In option so user can favorite comparisons or articles they want to read later

#### Biggest Challenges
* Using text analysis in the watson api
* Integrating an api that updates stories based off whats trending 
* Getting user location and displaying their local news

#### Instructor Notes

#### Deliverables for next checkin:
- Initial boilerplater for React/Router/Redux
- Api Calls
  - First Api call to be able to pull back articles
  - Api call to Watson capable of sending back tone analysis
- Listing of articles on main page