# Project Name: TBD - reading coach

### Check In: #1

# Project Pitch: 

### User: 
My friend’s second grade classroom (all of her students)
### User problem: 
Being a proficient reader by the 3rd grade is important milestone for students. 3rd grade is the time when students transition from learning to read  - to reading to learn. For students from low-income communities often don’t have access to enough books at home to spend the time with books that they need to become readers. The Obama administration started an initiative to access the publishing rights to open thousands of books to be free and open for students in Title 1 schools (low-income communities). With the administration change, the project has stalled out and I wanted to contribute if I could. Right now there is an app that has titles. Also students in younger grades who are just learning to read don’t just need titles, they need help with reading and to get regular feedback on their reading to become strong readers.

### Solution: 
I’d like to build a mobile app (or a web app if we’re not allowed to do mobile) that would pull these open book titles. I’d then like to build an interface where students can sign in, save their favorite books and see their book shelf. Once they’ve selected a text to read, they will be able to highlight or tap on a sentence from a story and read it aloud to the app. Then using the Watson natural language speech to text API, students will get feedback about their reading. The app will compare a students speech to the actual text and will tell them if they missed a word. The app will give them feedback (using the Watson text to speech API) from a menu of options (‘Good job’, ‘Let’s try to sound this word out’, ‘You said dog, the word is dug’).

If there is time, I’d like to implement ‘sight words’. These are words that every student should have memorized and shouldn’t need to ‘sound out’ (words like the, to, a, and). If a student missed a sight word, i’d like to store the word in local storage to create a set of flash cards from the books that a student is reading.


### Deliverables:

### Stack:
Javascript
React
Redux
unsure about data management and storage

### APIs:
Watson natural language API - speech to text: https://www.ibm.com/watson/developercloud/speech-to-text/api/v1/
Watson natural language API - text to speech: https://www.ibm.com/watson/services/text-to-speech/

Digital Public Library Association database: https://dp.la/info/developers/codex/ (for potential books) - still waiting to hear back

### Wireframes
### Waffle & Github
### Order Of Attack
### MVP
### Nice To Haves
### Biggest Challenges
### Instructor Notes
# Deliverables for next checkin:
