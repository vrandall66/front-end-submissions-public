## Project Name: Weekly Menu Planner

#### Check In #1

#### Project Pitch
Users can plan a weeks worth of meals by selecting recipes categorized by diet type, food 'genre', nutrional needs, and allergies.  
Save recipes and tag with 'breakfast', 'lunch', or 'dinner'.  
Look up nutritional information.  
App will populate and update a grocery list based on the current menu items.  

### Deliverables

#### Stack:
React, Redux, 

#### APIs:
edamam

#### Wireframes
![home page](https://user-images.githubusercontent.com/33009555/40505409-4f38c64e-5f51-11e8-9a09-024cbe849cf9.png)

#### Waffle & Github
Github issues

#### Order Of Attack
Determine what state tree will look like  
Confirm data fetch and create mockdata  
What actions do I need?  
Create Recipe List with click function to add recipe to Menu  
Create Grocery List that tallies up same items and  
Create Favorites  
Create Today's menu page  

#### MVP
List of recipes accessible by clicking category button.  
Click link recipe to menu day and meal-time redirect to Form Page.  
Menu and favorite recipes saved in local storage or firebase  
Today's menu page with links to recipes  

#### Nice To Haves
Add Search feature  
Access to nutritional information  
Serving size modifier  
Firebase server to save user accounts    
Option for monthly meal plans  
Use of edamam's beta spanish translation  
Intelligent grocery list: knows that 10 cups of flour will mean an initial purchase of a pound of flour, then deducts accordingly.  

#### Biggest Challenges
Design decision-making  
Is there enough time for full-on TDD?  

#### Instructor Notes

#### Deliverables for next checkin:
Github issues listing iterations to MVP  
Wireframes for code logic  
Plan for state tree and actions  
npm start and npm test working  
Install redux, react, react-router, saga and test with small code  
The scaffolding of an architecture  