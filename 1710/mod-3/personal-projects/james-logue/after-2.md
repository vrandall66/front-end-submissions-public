## Project Name:

#### Check In: 1

#### Progress made?

Front end can fetch to backend, which passes text POST to Watson, then passes response to front end. Added cleaning functions to dataHelper in front end to process data and sort relevant info. Strongest tone is currently displayed per sentence in text block using font color, but needs to be developed so that I can represent the primary and secondary tones of individual sentences. All current functions and components are tested, with the exception of the BE post to watson, which uses their SDK.

#### What deliverables still need to be completed from your last checkin?
I still need more polished styling, at the moment it is basic, though the correct feedback is being displayed. 

#### Next Steps?
Polish stying and display of information, develop text content and context. Build out page flow so that data is presented usefully. Potentially use D3 or other data visualization library to augment tone scores display.

#### What are your concerns (if any)
How should I test the BE endpoint which calls Watson? The post to watson responds into a callback of the function used to pass params, and I can't return out of it, so I am currently delivering the response to the front end from within that callback. 

#### Deliverables for next checkin:
