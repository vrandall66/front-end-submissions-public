## Personal Project Proposal - Check In 1
> Nick Svetnicka - Mod 3 - FE1705

> **Project Name:** snorlab (_codename_)

> **TLDR:**

- I am proposing to build an advanced reminder and task tracking app which **slowely unlocks features** as more tasks/reminders are completed, in which the user _levels up_. There are several 'fun', non-functional rewards also granted upon completing tasks/reminders. This creates incentive for the user to continually use the app, as rewards are forever granted for completing tasks, creating an infinite level system.

> Mockups:
- https://slack-files.com/T029P2S9M-F6Z2XAP98-c6e2a6a63c

## **Overview**

> This project is really the mashup of a few ideas. They are:

1. Celebrating the small wins...feel good moments. _I have a friend that studies the brain alot, and says that these wins are really giving yourself small dopamine hits (see more in Psychology Section)_

2. Reward based system that incentivises recurring visits to the site. There are a million to-do apps out there, why use this one...more importantly, why not...it's fun, and rewarding...literally! (**see section on Loot Bags**)

3. Randomized loot bags. These are all the rage in video games (hearthstone, overwatch, fortnite), because there's something about the randomness and 'slot machine' aspect that people really love and get addicted to.(**see section on Loot Bags**)

4. To Do list. Yes, it's been done many times, and I want to do it once more. With many layered and complex features (based on the previous 3 ideas) (**see below**)


> **Psychology Behind Wins**

Dopamine motivates us to take action toward goals, desires, and needs, and gives a surge of reinforcing pleasure when achieving them. Procrastination, self-doubt, and lack of enthusiasm are linked with low levels of dopamine.

Break big goals down into little pieces — rather than only allowing our brains to celebrate when we’ve hit the finish line, we can create a series of little finish lines which releases dopamine. And it’s crucial to actually celebrate — buy a bottle of wine, or head to your favorite restaurant whenever you meet a small goal.

This concept will govern the overall functionality of snorlab, in which there will be an aggressive attempt to bake in these small hits of dopamine within every aspect of the application.


## **Technology List**

- Must Haves

> React, Redux, Router

> React Notification System

> Database/local API (postgreSQL/express?)

> Remote APIs:
1. Avatar -- https://robohash.org
2. Quote: Rick and Morty -- http://loremricksum.com/documentation/
3. Quote: Chuck Norris -- http://www.icndb.com/api/ -- https://api.chucknorris.io/
4. Moods -- avatars.adorable.io
5. Extras: Theme/Font/Marvel/YodaSpeak/Gify


> Server-Driven Events: I've wanted to get my hands on some web sockets or SSE (server side events) exposure, and it can nicely be incorporated into this project (I hope) for the time-based reminders. Research and Discovery needed here.

> Drag-n-Drop: This would be a mostly drag and drop application (especially if React Native is used). Possibly using: https://react-dnd.github.io/react-dnd/

- Extensions?

> React Native _must be decided on 1st_

- Unknowns

> Firebase??

> API Fetch Library - maybe Axios / Moxios

> Middleware - maybe Thunk


## **MVP**

> Progression of unlocking features
- Full task/description/checklist/reminder functionality

> Target: Full loot bag system with at least avatars and moods

> Dream: Themes/Fonts/Quotes/Gify generator/slack integration


## **Resources**
- https://github.com/markerikson/redux-ecosystem-links/blob/master/middleware-sockets-adapters.md
- https://github.com/PlatziDev/socket.io-redux
- http://spraso.com/real-time-data-flow-with-redux-and-socket-io/
- https://github.com/versatica/JsSIP

- Themes
-- http://www.colr.org/api.html




## **Features**

* **Levels**: There would be a level system, and the more todo's you completed, the higher level you climbed.

* **User Account** - likely will include full user account creation (or possibly a more simplified model), which will contain an accounts page with some settings.

* **Feature-Rollout**: Each time you climb to a new level, you gain new features in the application. Features start VERY simple early on...basically...what is the task...then on each new level, you gain more feature unlocks. These are awarded through the loot bags. They are guarenteed loot drops on hitting that level. _See Section on Feature Unlocks for detailed functionality_ 

* **Loot Bags** (see section on loot bags) This will essentially be how features are rolled out, but then later on will allow for an infinite level system where you keep getting loot bags full of unlock and re-roll tokens.

* **History**: All tasks are stamped in time, meaning they stick around forever. this incentivises bad tasks to be deleted instead of completed.

* **Delete**: Possibly might do something semi rewarding for deleting a task... good to reward the user for keeping their tasks tidy. At the very least, it'll be a drag-n-drop action.

## **Feature Unlocks (one time drops)**

#### [level 1] Simple Task:
- only the ability to add 1 task string. Can ADD/EDIT/COMPLETE the task. (no drag and drop needed. complete and edit actions will be on task itself!)

#### [level 2] Loot Bags (first loot reward delete and drag/drop):
- See section below for more details. Introduces loot bags to user. Also grants first 2 loot rewards DELETE and DRAGnDROP onto trash can image or to re-sort tasks.

#### [level 3] Description Field:
- Allows the user to save task and description now. This is a toggle that the user can click on when creating a task.

#### [level 4] Avatar:
- _this site is looking a bit bare, lets get some color added_
- avatar comes from site: https://robohash.org and is the user's main avatar for their profile. only 1 slot available, but re-randomize tokens availbale through loot bags.

#### [level 5] Checklists (maybe called steps or task list):
- Allows the user to toggle not only a description field but also a checklist tied to the task. At this point, the user can toggle one or both of the description/checklist features tied to a task.

#### [level 6] Themes:
- Allow to user to change theme on the site. There are 2 rewards:
- new theme (random or let user chose)
- theme re-randomize token


#### [level 7] Moods:
- The user can categorize tasks however they want using mood emoji's from the site avatars.adorable.io the user has the ability to name moods however they want. These can be thought of as status's but not pre-locking the traditional status codes...allowing the user to set them.
- Mood slots rewarded through loot bags
- Identiy Change - re-randomize token (also chance to rename?)


#### [level 8] Reminders:
- Reminders would be server-based timed events which would generate a notification to the user (likely a perminent one). The user would be able to set a reminder to fire in x minutes or to fire at specific date/time. could use date/hour/minute.


#### [level 9] Quotes:
Quotes would display in header and loot bag tokens would be granted to generate new one. There is also a language filter in the settings

##### Rick and Morty: 
- http://loremricksum.com/documentation/
##### Chuck Norris:
- http://www.icndb.com/api/
- https://api.chucknorris.io/


#### [level 10+] Cat Images/Marvel API/Yoda Speak/etc:
- Additional fun api connection to provide additional types of token rewards.


## **Loot Bags (recurring drops)**

##### Loot drops come after completing X amount of items, and possibly other conditions

##### Loot drops also come when reaching a new level (as this is where feature unlocks occur)

**New Feature** (**see Feature Unlocks above**)
- There would be a series of feature unlocks awarded through the loot bags which are guanteed to drop in that bag upon reaching that level.
- Features include:
1. non-functional components like themes, fonts, avatars, quotes, images. (recurring)
2. funcitonal features (non recurring)

**Themes** : 2 types of drops
- new theme (random colors or let user choose)
- theme re-randomize token (or ability to just choose once)

**Fonts** : 2 types of drops
- Refer to Theme, as fonts would work very similarly. Need to investigate API's for fonts and themes.

**Avatar** : 1 type of drop
- https://robohash.org
- drop is token to change to new random one (also gives new name?)

**Moods** : 2 type of drop
- New slot unlock - get to name it initially
- Identiy Change - re-randomize token (also chance to rename?)

**Quotes** : 1 type of drop
- a token to swap out quote with new one...based on language filter.

**Cat Images/Marvel API:** : extension
- place holder not sure if will have time to keep adding any further non-functional components.



## **Routes**


#### /
- Root will display both reminders and tasks, also will handle all the crud on tasks and reminders.

#### / account
- displays control for language setting (rick n morty)
- slider to advance you through the functional unlocks (mostly used for testing)

#### / moods
- moods are the icons generated from: avatars.adorable.io
- they are unlocked as part of a feature unlock.
- they essentially represent status's but giving the user the ability to set them however they want (name and icon)
- this route would let them change the moods.

#### / loot
- this is the page that will show your un-opened loot bags, allow you to open them, and also shows what tokens you have available (granted from loot bags)


## Biggest Challenges

> API's going down / not accessible
- Might want to save data offline

> Drag-n-drop
- knowing where on the grid the pieces were placed
- computing rotations (words going hor -> vert)
- getting the Wolfram alpha api hooked up

> SSE / Web Sockets - if this turns out not easy to hook up or doesn't work as expected

## Instructor Notes

## Deliverables for next checkin:
