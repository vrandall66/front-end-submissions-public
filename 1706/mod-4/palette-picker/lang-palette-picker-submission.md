# Palette Picker Submission Form

[Project Spec](http://frontend.turing.io/projects/palette-picker.html)

# Basics

#### Link to the GitHub Repository for the Project
[palette-picker](https://github.com/francylang/palette-picker)

#### Link to the Deployed Application
[heroku](https://lang-palette-picker.herokuapp.com/)

#### Link to your annotated server file
[annotated server file](https://github.com/francylang/palette-picker/blob/annotated-server/server.js)

## Completion

#### Were you able to complete the base functionality?
Missing:~~Folder names must be unique (you should not be able to create two folders with the same name), annotated server.js file, testing- not fully tested, yet~~
~~I ran out of time.~~

Yes

#### Which extensions, if any, did you complete?
* User can edit the hex code in the aside palette and update to the new color. 

# Code Quality

#### Link to a specific block of your code on GitHub that you are proud of
[happy code](https://github.com/francylang/palette-picker/blob/master/public/js/scripts.js#38-47)
* I like this piece of code because I broke out the logic for the append and fetch palettes function. This eliminated nested fetch calls within the fetch projects function. 

#### Link to a specific block of your code on GitHub that you feel not great about
[sad code](https://github.com/francylang/palette-picker/blob/master/public/js/scripts.js#126-142)

* I would like to see if there is a way to check for duplicates within my main project fetch/post instead of doing two fetch calls to projects. I haven't had success, yet. I am not able to figure out how to get the response and then make the post if there are not duplicates without fetching again. 

#### Attach a screenshot or paste the output from your terminal of the result of your test-suite running.

[test suite](![image](https://user-images.githubusercontent.com/24443103/33521830-6882d1d8-d79a-11e7-8c19-93bc853bef7e.png))

#### Link to Design Inspiration
http://palettab.com/
* I really liked the horizontal color block aside, so I used that to ground my application and build the UI from there. 

#### Please feel free to ask any other questions or make any other statements below!

* I've seen how done is used in testing, but I am not exactly sure where it comes from and why it some times causes my test suite to timeout. 

-----


# Instructor Feedback (Brittany)

## Specification Adherence

**58 points**: (50 possible points) No approach was taken that is counter to the spirit of the project and its learning goals. There are no features missing from above that make the application feel incomplete or hard to use. Data persists on refresh using a knex/postgreSQL database.

* Nice implementation of the extension - but the UI for it is a little funky. Would like some visual indicator that you can edit that hex code value. (Maybe a little 'edit'/'pencil' icon?). Additionally, if I make the HEX value white, I lose the ability to see the HEX value text. Would be good to change that text to a dark color when white is the chosen color.


## User Interface

**17 points**: (20 possible points) User interface is mostly intuitive, though the instructor might need some guidance on interactions. Styling is mostly consistent, but could use some clean up.

* I like the vertical layout of the colors for each palette but on my screen it cuts off after the 4th one and I have to scroll down to see the 5th color. Would be nice to set a `height: 100%` on the containing element here to ensure it's always the height of a user's screen no matter what size their browser is.

* I'm seeing a weird bug where the 5th color stays in place (even when it's not locked). When I click on a pre-existing palette, the 5th color doesn't change.

* I like the handwriting font, but I wouldn't use it *everywhere*. With smaller elements, stick to something a little more rigid and basic. Fancier fonts are great for bigger headings rather than tiny button text.

## Testing

**17 points**: (20 possible points) Project has a running test suite that tests every server-side endpoint with many happy and sad path cases.

* Don't particularly need [all](https://github.com/francylang/palette-picker/blob/master/test/routes.spec.js#L119-L127) of [these](https://github.com/francylang/palette-picker/blob/master/test/routes.spec.js#L76-L84) assertions, they are all doing the same thing -- asking if there a resource at a bad URL

* Curious how [this](https://github.com/francylang/palette-picker/blob/master/test/routes.spec.js#L130-L155) test is working. If it should be returning a single palette, the response shouldn't be an array, it should be an object. Additionally, if the length of the array is 1, there wouldn't be an element at `response.body[2]`. There would only be an element at index 0.

* Would be good to assert against an error message [here](https://github.com/francylang/palette-picker/blob/master/test/routes.spec.js#L191) as well, not just a status code

* You wouldn't send through an [id](https://github.com/francylang/palette-picker/blob/master/test/routes.spec.js#L188) during a POST request naturally, so don't do it in your tests either. Just send through an empty object.




## Commented Server File

**x points**: (10 possible points)

## JavaScript Style

**x points**: (30 possible points)

* [This](https://github.com/francylang/palette-picker/blob/master/server.js#L30-L32) isn't really doing anything meaningful for you, and can sometimes be confusing when you're really returning the index file on your root get request through express.static. I'd get rid of this.

* Is [this check](https://github.com/francylang/palette-picker/blob/master/server.js#L64-L68) necessary? Would it not return an empty array by default if there were no records?

* Would be nice to break this type of [error handling](https://github.com/francylang/palette-picker/blob/master/server.js#L95-L101) out into a helper file. You're repeating it through a lot of your server file, DRY this up a bit.

* Send back the [id in this error message](https://github.com/francylang/palette-picker/blob/master/server.js#L147) as well just to give the user an indicator of what they actually tried to delete. I'm also torn about this being a 422 rather than a 404. A 404 literally means a resource doesn't exist at that endpoint, a 422 is generally used more for user error when you're passing through a formatted body object.

* Fetch requests [aren't dependent on the DOM](https://github.com/francylang/palette-picker/blob/master/public/js/scripts.js#L3). So they don't need to wait for document ready. Kick off this request and get that data ASAP.

* Why is there this lonely [.catch](https://github.com/francylang/palette-picker/blob/master/public/js/scripts.js#L53-L54) here?

* Was it supposed to go [here](https://github.com/francylang/palette-picker/blob/master/public/js/scripts.js#L58-L60) instead? ;)

* You don't want to be [appending to the DOM](https://github.com/francylang/palette-picker/blob/master/public/js/scripts.js#L63-L68) on each iteration of a for loop. DOM manipulations are expensive. Instead, you'd want to use Document Fragments to build up all the HTML you want to append, and then add it to the DOM all at once at the end of the loop.

* [This](https://github.com/francylang/palette-picker/blob/master/public/js/scripts.js#L65) is a poor naming convention for a method. Function names should be actions/verbs, like `appendProject`. Variables of any other data type should be nouns.

* This is a [lot of arguments](https://github.com/francylang/palette-picker/blob/master/public/js/scripts.js#L96) to be passing into a function. When you argument lists get long like this, it can be really easy to mess up their order and pass things in at the wrong spots. I'd refactor this to just take in a single object.

* You could have just added a `unique()` flag in your database schema that would do this [check](https://github.com/francylang/palette-picker/blob/master/public/js/scripts.js#L126-L142) for you automatically.

## Workflow

**x points**: (20 possible points)


### To get a 3 on this project, you need to score 110 points or higher
### To get a 4 on this project, you need to score 130 points or higher

# Final Score: x / 150
