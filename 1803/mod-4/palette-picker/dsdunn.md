# Palette Picker Submission Form

[Project Spec](http://frontend.turing.io/projects/palette-picker.html)

# Basics

#### Link to the GitHub Repository for the Project
[palette-picker](https://github.com/dsdunn/pallete-picker)

#### Link to the Deployed Application
[heroku](https://dsd-palette-picker.herokuapp.com/)

#### Link to your annotated server file
[annotated server file](https://github.com/dsdunn/pallete-picker/tree/comments)

## Completion

#### Were you able to complete the base functionality?

Yes.

#### Which extensions, if any, did you complete?

# Code Quality

#### Link to a specific block of your code on GitHub that you are proud of
Pretty much all the configuration for the various environments. While a bit overwhelming, it was interesting to learn about sql and setting up databases, as well as dev vs test environments and getting it all to work together.

Also, It felt good to write a server top to bottom with all the various endpoints.
[server.js](https://github.com/dsdunn/pallete-picker/blob/master/server.js)


* Why were you proud of this piece of code?

#### Link to a specific block of your code on GitHub that you feel not great about
```
function updateColors(colors = []) {
  currentColors = [];
  $('.color-square-big').each(function(i) {
    if( $(this).hasClass('locked')){
      return;
    }
    let color;
    if(colors.length) {
     color =  colors[i] 
    } else { 
      color = generateColor() 
    }
    $(this).css('background', `linear-gradient(${color} 78%, #fffbe8)`)
    $(this).find('.color-code').text(color)
    currentColors.push(color);
  })
  updateBackground();
}
```
* Why do you feel not awesome about the code? What challenges did you face trying to write/refactor it?

This could use some refactoring. Maybe pulling out some functionality to clean it up. It got kind of messy when I built in the condition enabling the colors to be populated from existing palettes. Given a little more time, I could improve this.

#### Attach a screenshot or paste the output from your terminal of the result of your test-suite running.
```
[Palette Picker is running on 3000.
  Client routes
    ✓ should return an html homepage
    ✓ should return a 404 for a route that doesnt exist

   API routes
     GET api/v1/projects
Seeding complete!
      ✓ should return all projects
     POST api/v1/projects
Seeding complete!
      ✓ should add a project to the database
Seeding complete!
      ✓ should return an error if required params are missing
    GET api/v1/palettes/:id
Seeding complete!
      ✓ should return a palette with the correct id
Seeding complete!
      ✓ should return an error if id doesn't exist
    POST api/v1/palettes
Seeding complete!
      ✓ should return a palette object on success
Seeding complete!
      ✓ should return an error if required params are missing
    DELETE /api/v1/palettes/:id
Seeding complete!
      ✓ should delete a palette by id


  10 passing (694ms)]()
```
#### Link to Design Inspiration

* Show us what you used as design inspiration (another color picker site, a dribbble UI element, a user flow, etc.) and explain what you stole from it

I liked and tried to emulate the backdrop with the colors blending behind the stripes, and the main palette floating on top of it

[link to design](https://www.behance.net/gallery/32154055/Minimalist-Color-Palettes-2015)

#### Please feel free to ask any other questions or make any other statements below!

I spend a considerable amount of time making this responsive. Hopefully that translates to the deployed version... Which is broken right now, and hopefully I can redeploy to fix....

-----


# Instructor Feedback (Instructor Name)

## Specification Adherence

**x points**: (50 possible points)

## User Interface

**x points**: (20 possible points)

## Testing

**x points**: (20 possible points)

## Commented Server File

**x points**: (10 possible points)

## JavaScript Style

**x points**: (30 possible points)

## Workflow

**x points**: (20 possible points)


### To get a 3 on this project, you need to score 110 points or higher
### To get a 4 on this project, you need to score 130 points or higher

# Final Score: x / 150
