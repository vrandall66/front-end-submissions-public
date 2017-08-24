# Jet Fuel Submission Form

[Project Spec](http://frontend.turing.io/projects/jet-fuel.html)

# Basics

#### Link to the Github Repository for the Project

[jetfuel](http://frontend.turing.io/projects/jet-fuel.html)

#### Link to the Deployed Application

[heroku](https://jtfule.herokuapp.com/)

#### Link to your annotated server file

[annotated server file](https://gist.github.com/jsullivan5/79cdcb95e6a3095bcc8f8b495b0d4c2a)

## Completion

No.

If not, explain what is missing and why.

I completed everything but the CSS transition. I finished this really late Sunday night and could not figure out how to debug
the issues in time. See sad code below.

None

# Code Quality

#### Link to a specific block of your code on Github that you are proud of
[happy code](https://github.com/jsullivan5/jet-fuel/blob/master/public/scripts.js#L159)

This is just reordering the cards with jQuery.  But it took me a long time to arrive at this.  I like it because I was able to
impliment it without any server side code, which I initially thought I would need to do.

#### Link to a specific block of your code on Github that you feel not great about
[sad code](https://github.com/jsullivan5/jet-fuel/blob/master/public/styles.css#L115)

This was the CSS transition I could not figure out at 3:00 AM.  I thought it would be simpler to do.  My app has a get request 
every time the folder changes and renders.  My understanding is that adding a class can be trickier when a component is rendering
and there are default browser optimizations to consider.  I wish I would have gotten this to work.

#### Attach a screenshot or paste the output from your terminal of the result of your test-suite running.

```
Jet Fuel is running on http://localhost:3000.
  Client Routes
    ✓ should return the home page
    ✓ should return a 404 if endpoint not found

  API Routes
    GET /api/v1/folders
done seeding
done seeding
      ✓ should get the folders
    POST /api/v1/folders
done seeding
done seeding
[ anonymous { name: 'beers', id: 3 } ]
      ✓ should create a new folder (40ms)
done seeding
done seeding
[ anonymous { name: 'beers', id: 3 } ]
      ✓ should return an error if user tries to duplicate folder.
done seeding
done seeding
      ✓ should return 422 if insufficient data is provided
    GET api/v1/folders/:id/links
done seeding
done seeding
      ✓ should get links for a folder
    POST /api/v1/links
done seeding
done seeding
{ long_URL: 'http://www.expedia.com',
  short_URL: 'http://jt.fl/ca2ea3b5',
  folder_id: 1,
  description: 'expedia' }
      ✓ should create a link
done seeding
done seeding
{ long_URL: 'http://www.expedia.com',
  short_URL: 'http://jt.fl/ca2ea3b5',
  folder_id: 1 }
      ✓ should return 422 if insufficient data is provided
    GET /api/*/:charHash
done seeding
done seeding
      ✓ should accept GET request to redirect (225ms)
```


  10 passing (1s)

#### Please feel free to ask any other questions or make any other statements below!

It was a fun project. I really enjoyed working in the back and and have some ideas on how I need to level up on these skills.

-----


# Instructor Feedback (Instructor Name)

## Specification Adherence

**x points**: Lorem ipsum dolor set amet

## User Interface

**x points**: Lorem ipsum dolor set amet

## Data Persistence with SQL Database

**x points**: Lorem ipsum dolor set amet

## Testing

**x points**: Lorem ipsum dolor set amet

## JavaScript Style

**x points**: Lorem ipsum dolor set amet

## Workflow

**x points**: Lorem ipsum dolor set amet


### To get a 3 on this project, you need to score 110 points or higher
### To get a 4 on this project, you need to score 135 points or higher

# Final Score: x / 150
