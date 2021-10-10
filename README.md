# BuNaO
Backend using Node and MongoDB. This project allows users to save information in a predefined format to a local non sql database, 
retrieve information from the database and update existing information. 

#Prerequisite
1) Postman: since the project only has node and mongo hence to send request to server we need Postman. It can be downloaded from here: https://www.postman.com/downloads/
2) MongoDB local database: To save, retrieve and information. Mongo can be downlaoded and setup using instructions from the following link: https://www.mongodb.com/try/download/community


When mongo DB driver is started it runs at this url:mongodb://localhost:27017/
Create a new database in Mongo

Following URL are accepted :

1) localhost:3000/dishes/  ( this query acts on all the dishes in the database)
2) localhost:3000/dishes/6161a9daca62782ce0223cb4    (after 'dishes/' is the dishiD. To act on a dish from database)

Methods supported:
1) GET
2) Post
3) Delete

Data is sent to the server in a particular format defined at location : 'models/dishes.js'. Data needs to be provided in this formet to be stored in database

Eg:

{
      "name": "Zucchipakoda",
      "image": "images/zucchipakoda.png",
      "category": "appetizer",
      "label": "",
      "price": "1.99",
      "featured": "false",
      "description": "Deep fried Zucchini coated with mildly spiced Chickpea flour batter accompanied with a sweet-tangy tamarind sauce",
      "comments": [
        {
          "rating": 5,
          "comment": "Imagine all the eatables, living in conFusion!",
          "author": "John Lemon",
          "date": "2012-10-16T17:57:28.556094Z"
        },
        {
          "rating": 4,
          "comment": "Sends anyone to heaven, I wish I could get my mother-in-law to eat it!",
          "author": "Paul McVites",
          "date": "2014-09-05T17:57:28.556094Z"
        },
        {
          "rating": 3,
          "comment": "Eat it, just eat it!",
          "author": "Michael Jaikishan",
          "date": "2015-02-13T17:57:28.556094Z"
        },
        {
          "rating": 4,
          "comment": "Ultimate, Reaching for the stars!",
          "author": "Ringo Starry",
          "date": "2013-12-02T17:57:28.556094Z"
        },
        {
          "rating": 2,
          "comment": "It's your birthday, we're gonna party!",
          "author": "25 Cent",
          "date": "2011-12-02T17:57:28.556094Z"
        }
      ]
    }


