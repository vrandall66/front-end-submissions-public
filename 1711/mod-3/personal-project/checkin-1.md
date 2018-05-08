## Project Name: 
Refuge

#### Check In 1

#### Project Pitch
Many people suffer from panic attacks without any treatment. Refuge is an attempt at using heart rate and physical activity data collected from fitbit wearable devices to help predict and mitigate the effects of impending panic attacks. As a user's heart rate increases without any other signs of physical activity, Refuge will attempt to help redirect their thoughts and focus away from triggers that might escalate into a panic attack. Refuge will recored the time and date of the panic attacks as well as allow users to append notes to each event in order to help diagnose possible external triggers. 

### Deliverables

#### Stack:
React   
Redux  
Router  
eslint  
Middleware: Sagas or Thunk  
Node Express?  

#### APIs:
https://dev.fitbit.com/
https://waffle.io/rvwatch/Refuge

#### Wireframes
https://imgur.com/a/EjENN 

#### Waffle & Github
https://github.com/rvwatch/Refuge    
https://waffle.io/rvwatch/Refuge

#### Order Of Attack
Setup React Boilerplate    
Pull in relevant fitbit realtime data  
Simulate realtime user data  
Test fetch calls  
Test core action creators  
Test Reducers  
Connect containers   
Add data to store  
Test & create relevant components  
Test / Write core logic to monitor heart rates  
Test / Write user alerts  
Store events in store/localstorage - maybe setup database if all goes well?     
Test / Write note taking functionality that will be attached to events / timeframes  
Style, style style  
Ensure Full responsiveness for multiple devices  

#### MVP
Real time heart rate monitoring.   
Setup alerts based on comparison of current heart rate to average resting heart rate.  
Login / Logout functionality.   
Profile / setup page to enter relavent info / numbers of support personel.  
Prompts for breathing excercises and mindfullness, link to headspace app, call therapist button.   
Note taking functionality that allows users to list any potential causes or triggers of a panic attack and attach notes to an event. 

#### Nice To Haves
Database to store relevant data.   
Integration with some sort of chat service that allows users to connect with a registered therapist.  
Portal for therapists to access their clients data and to monitor their status or even call them / message them directly. 

#### Biggest Challenges
Tapping into relevant and accurate data from fitbit.   
Creating a UI that is intuitive and relevant to the situation.   
How will I setup "events" and store them?   
Setting up a database (assuming I get to that point)  

#### Instructor Notes

#### Deliverables for next checkin:
