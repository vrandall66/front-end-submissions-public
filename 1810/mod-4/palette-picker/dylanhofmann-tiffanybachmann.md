# Palette Picker Submission Form

[Project Spec](http://frontend.turing.io/projects/palette-picker.html)

# Basics

#### Link to the GitHub Repository for the BE
[palette-picker BE](https://github.com/dylhof/palette-picker-be)

#### Link to the Deployed BE
[heroku BE](http://palette-picker-be.herokuapp.com/)

#### Link to the GitHub Repository for the FE
[palette-picker FE](https://github.com/trbachmann/palette-picker-fe)

#### Link to the Deployed FE
[heroku FE](https://colorations.herokuapp.com/)

## Completion

#### Were you able to complete the base functionality?

Yes we were able to complete the base functionality

#### Link to an image of your wireframe(s)
[wireframes](https://user-images.githubusercontent.com/40586291/55119479-a771c880-50b7-11e9-8002-3f155a4697a0.png)

#### Which extensions, if any, did you complete?

# Code Quality

#### Link to a specific block of your code on GitHub (from either repository) that you are proud of
[happy code](https://github.com/trbachmann/palette-picker-fe/blob/6ba92dfe69ffd32263eb5a6cd06fe8f403e86575/src/Reducers/CurrentPaletteReducer.js#L10)

* Why were you proud of this piece of code?  
We worked on this together. It updates the isLocked property on a specific color in the currentPalette. We used array destructuring and wrote it correctly the first time. We both haven't used array destructuring often and were very excited to see it work correctly on our site right away.

#### Link to a specific block of your code on GitHub that you feel not great about
[sad code](https://github.com/dylhof/palette-picker-be/blob/19375343dba7024b652eac0a5f621045a55ee6c5/app.js#L142)

* Why do you feel not awesome about the code? What challenges did you face trying to write/refactor it?
We aren't super happy with the three nested knex database calls. We wanted to consider going back to refactor using async await, but at the same time wanted more practice using .then() since it could be what we use in a future job. We also think there are probably edge cases for errors that we are not accounting for.

#### Link to Design Inspiration

* Show us what you used as design inspiration (another color picker site, a dribbble UI element, a user flow, etc.) and explain what you stole from it  
[design inspiration](https://dribbble.com/shots/4136598-Flat-UI-Colors-2)    
We really liked the shape of colors from this dirbble design. We used the same shape for displaying the colors on our main palette and our mini palettes.

#### Reflection on New Concepts

* Describe your thoughts on server-side testing  
It is more straightforward than FE testing. We were surprised by how quickly the ids in our database exceeds 1,000 😳
* Describe your thoughts on TravisCI  
It takes a lot of steps to get it up and running correctly, but it is really helpful and another great check to try and ensure you don't deploy code with bugs.
* Describe your thoughts in creating a single project whose codebase was distributed across multiple repositories
We're starting to get more comfortable with referencing external data sources. The environmental variables are really helpful and make a lot more sense now.
#### Please feel free to ask any other questions or make any other statements below!

Anything else you wanna say!

-----


# Instructor Feedback (Instructor Name)

## Specification Adherence

**x score**: 

## User Interface

**x score**: 

## Testing

**x score**: 

## Workflow

**x score**: 

# Outcome: pass/fail
