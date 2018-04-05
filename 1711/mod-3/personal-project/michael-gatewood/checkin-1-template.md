## Project Name:  Bar Builder (title pending)

#### Check In 1

#### Project Pitch
Build an application of cocktail recipes with the ability to filter by drink category, ingredient, alcoholic content or search query.

### Deliverables

#### Stack:
+React
+Redux
+Router

#### APIs:
https://www.thecocktaildb.com/api.php

#### Wireframes
![Screen Shot 1](https://raw.githubusercontent.com/mngatewood/front-end-submissions-public/check-in-1/1711/mod-3/personal-project/michael-gatewood/ScreenShot-3.png)
![Screen Shot 2](https://raw.githubusercontent.com/mngatewood/front-end-submissions-public/check-in-1/1711/mod-3/personal-project/michael-gatewood/ScreenShot-1.png)
![Screen Shot 3](https://raw.githubusercontent.com/mngatewood/front-end-submissions-public/check-in-1/1711/mod-3/personal-project/michael-gatewood/ScreenShot-2.png)

#### Waffle & Github
https://waffle.io/mngatewood/bar-builder

#### Order Of Attack

##### Iteration 0
* Develop App component that fetches name and thumbnail for all recipes.
* Develop RecipeContainer and RecipeThumbnail components.

##### Iteration 1
* Develop RandomRecipe component.
* Develop RecipeDetail component that displays recipe details for a selected recipe.

##### Iteration 2
* Develop Search component with search field and filter buttons.
* Develop alcoholic/non-alcoholic drinks filter.
* Develop search by text functionality.
* Develop filter by category functionality.
* Develop filter by ingredient functionality.

##### Iteration 3
* Develop Login, Logout and Signup components.
* Develop add/remove favorites functionality.
* Develop Favorites component.

##### Iteration 4
* Setup backend to store/edit wishlist, personal inventory, and shopping list.
* Develop IngredientInventory component.
* Develop search by on-hand ingredients functionality.
* Develop ShoppingList component.

##### Iteration 5
* Link shopping lists to online merchant.

#### MVP
On load, the application displays a random recipe, a simple text search field and buttons to display drinks filtered by category, ingredient, or alcoholic content.

#### Nice To Haves
Display a checklist of ingredients where users may select ingredients on-hand.  On submit, a list of drinks containing the selected ingredients will be displayed.

Users may select desired recipes and print a shopping list of required ingredients.

Users may create an account to save favorite drinks, wishlists (for ingredients), and store/maintain an inventory of on-hand ingredients.

In addition to having a printable shopping list, user is provided a link to an online merchant (Amazon?) with a shopping cart pre-populated with required ingredients.

#### Biggest Challenges
Filtering recipes based on multiple criteria (ingredients).  Inclusive vs exclusive search?

#### Instructor Notes

#### Deliverables for next checkin:
