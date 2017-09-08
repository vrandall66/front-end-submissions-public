## Project Name:

#### Check In: 1

#### Project Pitch

The app will start as a recipe finder, being able to index by ingredients, type of cuisine, and food restrictions. Once finding a recipe that you would like to follow, it will have the ability to generate a grocery list which can be edited if there are ingredients on the list which you already have. Eventually I would like to incorporate the ability for a user to be able to create an account and log in so that recipes can be favorited/saved and give the user the ability to plan out a menu for the day/week/or month. At that stage after the ability to menu plan I would like to have users be able to think about planning out meals while vacationing with the ability to search for restaurants and reviews in different destinations. In future stages I would also like to give users the ability to share favorite recipes with friends/family and even be able to create their own recipe cards or variations of existing recipes.

### Deliverables

Recipe finder & grocery list producer based on chosen recipe

#### Stack:

React,
Redux,
Router,
Firebase (possible)

#### APIs:

Yummly

#### Wireframes

Find in wireframes folder - please excuse lack of color, I am still working on design.

#### Waffle & Github

Github: https://github.com/anajauregui/Menu-Planner,
Waffle: https://waffle.io/anajauregui/Menu-Planner

#### Order Of Attack

My approach for this project will be to to work in small steps and build out. I will start with working on building out functionality that is familiar to me to solidify what we have been learning throughout mod-3 so far. With each iteration I would like to add a new piece of functionality. I would like each iteration to be a fully functional app that scales in size while incorporating additional API's and grows the stack of tools I am using.  

#### MVP

Application which a user can search recipes through different criteria and be able to generate a grocery list based on chosen recipes.

#### Nice To Haves

-Ability for user to log in and save favorite recipes
-Menu planning capabilities/ nutrition incorporation
-Trip menu planning  
  - being able to search for restaurants in desired destinations with reviews
  - on-the go recipe suggestions
- Ability to share favorite recipes and create new recipe cards / social media

#### Biggest Challenges

- Keeping small steps in mind to achieve MVP and not becoming overwhelmed trying to figure out the big picture all at once.


#### Instructor Notes

#### Deliverables for next checkin:

#### Current status of project:

- I spent quite some time digging through the documentaion for my chosen API and dissecting how I am going to begin working with the data. I feel like I have a pretty good grasp on how to work with it at this point.
- I begin with creating basic create-react-app template and hooked things up to make the initial API call for recipe searching and created some mock-data to try and avoid exhausting limited calls.
- My next step was to implement thunk and try and convert from the basic react app to use Redux... At this point I have reached a bump in the road as I am not getting what I was expecting in the Redux store so I am still trying to work on getting that going in the right direction.
- Once I get things sorted out with my initial calls and Redux showing what I am expecting in the store I will be moving forward to create a basic recipe search and moving forward with the ability to select recipes before I begin to work on more detailed filtered search that you will find as my 2nd iteration of searching.
- I hope to get up and running with that and incorporate styles over the weekend.



# Teacher Notes:

Ana:

Name: Menu Planner (likely to change)

Description:
* App that allows users to search for recipes, generate shopping lists, and save both

MVP:
* User can search for recipes based on:
    * Ingredient
    * Cuisine Category
    * Potentially health concerns
* Search
    * Multiple fields or Single search field?
    * Surprise me option? Complete random recipe
        * Featured recipe of the day?
        * Home page default?
* Shopping List
    * How do the API’s deliver ingredients data?
    * Needs ability to input number of people and get accurate ingredient amounts

Backend:
* Firebase

Auth:
* Yes

API:
* Yummly
    * Requires multiple calls, first is just browsable menu options
    * Second call gets specifics

Extensions:
* Sharing: Favoriting/Following other users and having a feed of their favorite recipes
* Building out search to be extremely customizable
    * Dietary restrictions
    * Calorie count (max)

Deliverables:
* Start with basic search, have results populating on the Dom
* Get second API call fired on click and data at least in console
