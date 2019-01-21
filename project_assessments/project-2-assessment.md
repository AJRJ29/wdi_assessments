<img src="https://i.imgur.com/sX12DTc.png">

# Project 2 Assessment

## Introduction (By Instructor)

Students will be self-directed through this assessment. Please read the requirements in their entirety before beginning any work. 

### GOAL

The goal of this project assessment is to gauge your ability to develop a minimal full-stack web application using NodeJS and the Express framework, including your ability to:

- Set up GET and POST routes
- Install and use node modules
- Use an ORM
- Set up and properly use forms
- Deploy your app 

## Requirements

### Time Limit

You will be given 3 hours of class time to complete this assignment. No late work will be accepted.

### Resources

This is an open book test. You are welcome to use class notes, books, or any resource on the internet.

### Technology Requirements

In class, we've been using PostgreSQL, Sequelize, Node, Express, EJS, and Heroku, so by default, we'll assume that's what you're using for this assessment. However, you are welcome to use any framework, ORM, view engine, and cloud service you're comfortable with.

> Protip: Don't learn something new just for this assessment. Use something you already know.

### App Requirements

#### Routing

Make an Express app with the following routes:

| METHOD | PATH | PURPOSE |
| ---- | --------------- | ------------------------------------ |
| GET | / | Home Page |
| GET | /favorites | List of all favorite animals |
| POST | /favorites | Add a new favorite animal |
| GET | /favorites/new | A form for adding a new animal |

#### Database

Make an `animal` model using Sequelize with the following schema:

| COLUMN | TYPE |
| ----------------- | ---------------- |
| id | integer |
| species_name | string |
| scientific_name | string |
| image_url | string |
| description | text |
| extinct | boolean |
| createdAt | date |
| updatedAt | date |

#### Views

Your homepage can generally look however you'd like, but make sure there are visible links to your other two pages.

Your /favorites/new page should render a form that allows you to enter a new animal. This form should `post` to the /favorites route. There should be an input field for each value corresponding to the columns in your database schema. This will include:

* species_name
* scientific_name
* image_url
* description
* extinct

Your /favorites page contains a list showing each animal in your database. If the animal is extinct, show the species_name in red text. Otherwise show the species name in black text. The scientific_name should be shown in italic text beside or below the species_name. The image linked to by the image_url should be displayed at no larger than 300x300 pixels. The description should also be displayed somewhere.

#### Deployment

Please deploy your app on Heroku. Follow the class notes if you get lost or stuck. If you run into something truly weird that the class notes don't cover, the instructional team will render assistance, but this should be a much simpler task than deploying your project 2.

#### BONUS

You can do any number of things for bonus points including:

- Implement a /favorites/:id route for each animal
- Add a CSS framework or custom styling
- Make your site responsive
- Give your site a header and/or footer
- Make your add animal form really nicely styled
- Add a default image in case the user doesn't provide one
- Implement flash messages for form/data entry errors

## Turn-in

Put your heroku link into slack. This is all you need to do. After you are done with the test you are welcome to leave the room or sit quietly while others finish up. 

## Advice

Styling, for the most part is a bonus for this assessment. This thing does not need to be beautiful. Worry about functionality first and foremost. Priority one is that your routes work properly. Priority two is that your database works properly. Priority three is deployment. Get as far as you can within the allotted time frame.
