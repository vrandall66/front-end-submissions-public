## Project Name: Cover

#### Check In: 3

#### Project Pitch

Domestic abuse is prevalent in communities across the country and affect people of all backgrounds. Physical violence often comes with emotionally abusive and controlling behaviors. In the US, 1 in 3 women have been victim of some form of violence by an intimate partner, and 1 in 2 women have been victim of psychological abuse. It can be incredibly difficult for people in abusive relationships to get help, many times, due to fear of getting caught asking for help or trying to leave.

Cover is an app for people seeking help, whether in an emergency or when they need a friend to talk to. With the silent and quick click of one button, users can call for emergency services from 911. Users can send a custom text message to a contact, or if time is short, can send a pre-written text, including the users current location to any contact. The user will also be able to call the National Domestic Abuse Hotline though the app. All features eliminate the risk of their abuser seeing texts or calls from their phone/computer log. 

Statistics from National Coalition Against Domestic Violence: https://ncadv.org/statistics

### Deliverables
- Have firebase and redux playing together 
  - have store populated with state 
  - so any update to firebase will be funneled to redux first (redux isn't needed); 
- Work on contacts only being saved to a current User 
   - I shouldn't log in and see your contacts 
   - User should be able to log in and log out. 
   - it would be nice to have the option to log in and log out via google oauth
- You might want to move some of the logic in your componentDidMount into an action   
- start on the twillio backend 
- start testing. 
  - also maybe move the api calls into a firebase functions file. 

#### Waffle & Github
- https://github.com/ameseee/cover
- https://waffle.io/ameseee/cover

#### Order Of Attack
- Build react/redux
- Sign in with firebase
- Set up twillio endpoint

#### MVP
Contacts functionality
  - Save contacts (name and number)
  - Custom text to contact
  - Text my location now to contact
  
Text to 911
  - Send location to 911

#### Nice To Haves
Call NDV Hotline
  - Call hotline through app
Data Visualization of stats


#### Biggest Challenges
- Node and Twilio
- 

#### Deliverable From Last 
 

#### Deliverables for next checkin:


