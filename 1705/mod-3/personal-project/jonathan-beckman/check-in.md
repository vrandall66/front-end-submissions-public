## Project Name:

   * DocSwap

 #### Check In: 1

 #### Project Pitch

   * An app that takes an image of a document, grabs the content and translates it into another language

 ### Deliverables

 #### Stack:
   * React
   * React-Router
   * or React-Native
   * possibly Firebase

 #### APIs:

   * [Optical Content Reader](https://ocr.space/ocrapi)

 #### Wireframes
   * [WireFrames](https://github.com/jbexx/DocSwap/blob/master/README.md)

 #### Waffle & Github

  * [Github](https://github.com/jbexx/DocSwap)
  * [Waffle](https://waffle.io/jbexx/DocSwap)

 #### Order Of Attack

   * setup boilerplate
   * get routes setup
   * build out HTML and CSS
   * build out functionality
 #### MVP

   * able to upload doc
   * language recognition
   * upload to api for translation
   * choose langauge you want final doc in

 #### Nice To Haves

   * dictionary implimentation
   * flash cards for words
   * upload document from file
   * include user profile if needing to save document translations and flash cards

 #### Biggest Challenges

   * possibly setting up backend
   * camera usage
   * all the things I don't know

 #### Instructor Notes

 #### Deliverables for next checkin:


# Teacher Notes:

Jonathan:

Name: Doc Swap, Translation Something

Description:
* App that allows users to translate documents by uploading an image and receiving a translation in your preferred language
* How can this be a learning tool?!?!

MVP:
* Ability to upload a document or take a picture
* Ability to upload to API for translation
    * API may take care of identifying source language
* App will return translated verbiage for whatever language user selects
    * User can change output language
* Ability to define unknown words
    * Either dictionary definition or thesaurus feature to offer up similar words
    * EXT: Possibility to add to a “flash cards set”
* Add user and profile to save document translations (and possibly flash cards)

Backend:
* Firebase if applicable
    * Authorization
    * Database

Auth:
* TBD - if saving data, then yes

API:
* OCR - Optical Content Reader

Extensions:
* Flash cards
* Works on mobile

Deliverables:
* API Chosen
* First two screens built out (styling not necessary)
    * Clicking home screen takes you to next view w/ 2 options
    * Clicking to take picture accesses camera
    * Clicking load image access images on phone
* Make first API request and get text back
