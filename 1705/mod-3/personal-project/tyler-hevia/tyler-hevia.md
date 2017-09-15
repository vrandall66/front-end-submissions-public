## Project Name:
  
 TBD
 
  #### Check In: 1
  
  #### Project Pitch
  
 I want to make an app where a user can create an account, add their favorite books, and then click on a book to get a recommendation 
 on what they should read next. I also want them to be able to make multiple selections to get a recommendation based on multiple books.
 Users should also be able to organize their books into lists.
 
  ### Deliverables
  
 I want to deliver a fullstack app with the features I just listed, but I need feedback on whether my pitch is too ambitious or not ambitous enough.
 
  #### Stack:
 - react, redux, router, typescript 
 - Node => express;knex/postgres
  
  #### APIs:
  
 Goodreads API, maybe the Google Books API and LibraryThing API.
 
  #### Wireframes
  
 [Wireframes](http://imgur.com/a/X8kEk)
 
  #### Waffle & Github
  
 [Waffle](https://waffle.io/tylerjhevia/personal-project)
 [GitHub](https://github.com/tylerjhevia/personal-project)
 
  #### Order Of Attack
  
 I think I'll have a better idea of this after my first checkin. I know that I definitely need to start getting familiar with 
 what the data will look like from Goodreads, and I need to figure out whether I'll need a backend. My plan is to use React and Redux, 
 so I want to get my Redux hooked up as soon as possible. I'll also need to figure out my logic for generating recommendations. 
 
  #### MVP
  
 - A user should be able to add a favorite book, click on it, and then see a recommendation displayed.
 - User can join a book club and users can vote on book. (nice to have)
 - typescript 
 
  #### Nice To Haves
  
 I'd like to try using TypeScript. I think I'll probably start writing in vanilla JavaScript and then convert to TypeScript as I 
 go.
 
  #### Biggest Challenges
  
 Backend stuff and deciding how to generate good, logical recommendations.
 
  #### Instructor Notes
  
  #### Deliverables for next checkin:

  - Hook up typescript to react, redux and router 
  - Have backend created 
      - initial table setup favorites && user 
  - have api making intial request and populating store. 
  
  #### Updates for check-in 2

  - Set up my file structure and hooked up my redux
  - Had trouble setting it up with TypeScript at first, so right now I'm going back through it and rewriting it
  - Started my backend repo and wrote a very basic file with express
  - Don't have a table yet
  - Can get the information from my api, but haven't set it to store yet
  - Still getting comfortable with TypeScript
  - Decided to use GoogleBooks API instead of Goodreads

### needs 

- decide what backend to use 
- if you're using node 
      - set up up the user table 
      - set up the favorites 
      - look into building the database for the groups. 
- If you're choosing FB 
    - have firebase hooked 
    - have the auth() function allowing the user to sign in 
- user should be able to login 
- user should be able to favorite books 
- have the frontend hooked so that user can see available books

#### Updates for check-in 3
- Created users and favorites tables
- User can search books
- Can fetch data from backend 
- Basic styling for Login, Register, and Search components

#### deliverables for next
- have the favorite fully hooked up 
- user can login and ui reflects 
    - we are not inserting a user we are finding the user 
 - whne user signs up you should set up an end point for ('user/new/')
 - user can actually favorite 
 - if you can get to this having some sort of catagories filter.
 - test stuff. 


#### Check-in 4
- Infinite fetch call loop in library
- Styling sucks
- Not checking for duplicate emails/usernames when registering new users
- Need to notify user when login is unsuccessful
- Need to communicate to the the user how to add a book to library and add styling for favorites
- Add remove favorite functionality
- Prevent duplicate favorites
- Save user to local storage
- Testing
