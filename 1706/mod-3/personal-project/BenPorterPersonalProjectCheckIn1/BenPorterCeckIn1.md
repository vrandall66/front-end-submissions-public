
## Project Name: Hometending Web app

#### Check In: 1

#### Project Pitch
The goal of this app is to allow clients/homeowners to quickly and easily request services from a hometending business, as well as well as streamline certain processes of the business. 

### Deliverables

#### Stack:
The Statck will include an stubbed backend of a few houses/homeowner users as well as a business side admin user.
The app will be buitl usins React and Redux. 

#### APIs:
APIs will include the stubbed backend, as well as the google cal api or other calendar api. 

#### Wireframes

Home

![home](https://user-images.githubusercontent.com/26842728/32000772-08ec3790-b955-11e7-83f9-191a1d8b81f0.jpg)

Business owner messages & properties pages

![owner-message-and-property-pages](https://user-images.githubusercontent.com/26842728/32000815-2b77dbde-b955-11e7-8ab8-92e0787c2f23.jpg)

Business owner invoice form

![owner-invoice-form](https://user-images.githubusercontent.com/26842728/32000910-6b424db2-b955-11e7-9933-b1b841446e8f.jpg)

#### Waffle & Github
[Github](https://github.com/bbp5280/homeTendingApp) 
[Waffle] (https://waffle.io/bbp5280/homeTendingApp)

#### Order Of Attack
0. Stub backend
1. Home page with info about the business linking to a login page allowing both homeowner login as well as business owner login
2. Home owner login has the ability to fill out a form requesting services on their house. Request should send an email to home owner to as a record of request. The subbmitted request should also email business owner as well as well as be visible in a "messages" section of the business owner login. Business owner should be able to set a time and date and schedule the request to a gmail calendar. Once scheduled an email should be sent to homeowner with details. 
3. Business owner should be have the ability to create an invoice. Upon submission the invoice should be saved to the home and generate an email to the homeowner. 
4. next set of features - see nice to haves

#### MVP
The MVP for this app will include a homepage, homeowner and business owner login. The homeowner should have the ability to request services. The business owner should be alerted of these request on login and be able to schedule request pushing automatically to a google cal. Business owner should be able to create an invoice. 

#### Nice To Haves
Each home should have it's own calendar so business owner can keep track of owner and guest stay dates.
A batch invoice proccess to generate monthly invoices to homeowners
Shopping list checklist available to the homeowner to request shopping services be done before an arrival. 
Tha ability to upload images of the home which can be attached to invoicing. 

#### Biggest Challenges
The biggest challenges will be stubbing the backend and implimenting the automation. 

#### Instructor Notes

Focus first on the business side, mock data on the front end using the initial state of the redux store, then look
towards back end db solutions (firebase).

#### Deliverables for next checkin:

- Working boilerplate with React, Router, and Redux set up. Should have idea of how additional containers/components
  will be added to the project.
- A working fetch method that can add an event to a google calendar.
