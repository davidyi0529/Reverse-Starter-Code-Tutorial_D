# Reverse-Starter-Code-Tutorial_D

This tutorial will go into details of each file and how they are essential to each component of this application.

<br />

## Table of Contents

- [Config](#config)
- [models](#models)
- [Public](#public)
- [Routes](#routes)
- [server.js](#server.js)

<br />
<br />

---

<br />
<br />

## Config

<br />
<br />

Within the Config folder contains files needed for connectivity to the server and login authentication.

<br />

1. `Middleware` - This folder contains a file called `isAuthenticated.js` which restricts any user to accessing certain routes without a login authentication.

<br />

<img src="https://github.com/davidyi0529/Reverse-Starter-Code-Tutorial_D/blob/main/Images/isAuthenticated.png?raw=true" width="700" height="200">

isAuthenticated.js is using a function to let the application know that if the requested object is a user then to direct the user to the requested route.

However, if the user is not logged in the it will return and redirect the user to the login page.

<br />

2. `config.json` - Provides connection configurations to connect to the server.

<br />

<img src="https://github.com/davidyi0529/Reverse-Starter-Code-Tutorial_D/blob/main/Images/Config.png?raw=true" width="500" height="400">

<br />

Configurations are provided for handling multiple environments (Development, Test, or Production).

<br />

3. `passport.js` - Authentication with `Passport-local` to log in with an email address and password.

<br />

<img src="https://github.com/davidyi0529/Reverse-Starter-Code-Tutorial_D/blob/main/Images/passport.png?raw=true" width="500" height="700">

<br />

Passport.js requires passport and passport-local. Passport-local is a passport strategy for authenticating with a username and password.

The user will login in using an email address which we have assigned for the username field. The application will then run through a series of functions to check in the database if the user's email address and password are valid. If the email address or password are incorrect, the user will be prompted of the incorrect email/password.

To keep the authentication state across HTTP requests. `Passport.serializeUser` and `Passport.deserializeUser` are used.

`Passport.serializeUser` - Determines which data of the user object should be stored in the session which we have deemed as "User".

`Passport.deserializeUser` - Corresponds to the key of the user object that was given to the done function of `Passport.serializeUser`. 

<br />
<br />

---

<br />
<br />

## Models

<br />
<br />

Within the Models folder contains files needed for connectivity to the database to retrieve and create user data.

<br />

1. `index.js` - Connects to database and imports users data logs.

<br />

<img src="https://github.com/davidyi0529/Reverse-Starter-Code-Tutorial_D/blob/main/Images/indexjs.png?raw=true" width="700" height="500">

<br />

2. `user.js` - Creation of user information that is stored into the database. Uses `bcrypt` for password hashing which allows a more secure database.

<br />

<img src="https://github.com/davidyi0529/Reverse-Starter-Code-Tutorial_D/blob/main/Images/userjs.png?raw=true" width="600" height="500">

<br />

`Bcrypt` is required for password hashing which will be explained shortly. 

First the User model is created based off the user's input of email address and password. This function will look at the user's input and validate if it is a proper email and also not a

blank response.

`Bcrypt` is now used to compare if the user provided password matches a hashed password in the database. 

Also, in this case, `Bcrypt` is used to hash the password automatically before it is created.

<br />
<br />

---

<br />
<br />

## Public

<br />
<br />

Within the Public folder contains files needed for the front end of the application.

<br />

1. `js` - This folder contains validation for the login, members, and signup pages.

    - login.js - Login validation

    - members.js - Checks to see which user is logged in and updates the html page.

    - signup.js - New user creation validation

<br />

2. `stylesheets` - This folder contains CSS styling for the page layouts.

    - style.css - CSS styling

<br />

3. `login.html, members.html, signup.html` - Page layouts.

<br />
<br />

---

<br />
<br />

## Routes

<br />
<br />

Within the Routes folder contains files needed to correctly route the user's data and correct page to be displayed.

<br />

1. `api-routes.js` - Routes for logging in and getting users data to be displayed client side.

<br />

<img src="https://github.com/davidyi0529/Reverse-Starter-Code-Tutorial_D/blob/main/Images/apiroutes.png?raw=true" width="600" height="700">

<br />

Models and Passport will be required. 

`Passport.authenticate("local")` will check if the user has valid credentials to direct them to the members page.

`app.post("/api/signup")` function is used to for signing up a user. 

`app.get("/logout")` function used to log out the user.

`app.get("/api/user_data")` function is used to retrieve user data. If the user is not logged in, they will receive an empty object, otherwise, the user's email and id will be received.

<br />

2. `html-routes.js` - Routes to authenticate the user's login and re-direct the user to the correct html page.

<br />

<img src="https://github.com/davidyi0529/Reverse-Starter-Code-Tutorial_D/blob/main/Images/htmlroutes.png?raw=true" width="600" height="500">

<br />

Path is first required, then isAuthenticated is used to check if the user is logged in.

The following functions used is to properly direct the user to the correct page.

The `app.get("/")` function is used when the user has an account they will then be directed to the members page, if not then they will be directed to the signup page.

The `app.get("/login")` function is used when the user has an account they will then be directed to the members page, if not then they will be directed to the login page.

The `app.get("/members")` function will check if the user is logged in with their information before accessing the members page. If not, they will be re-directed to the signup page.

<br />
<br />

---

<br />
<br />

## Server.js

<br />
<br />

The server.js file requires packages, sets up PORTS, creates express, middleware, routes, and syncs the database. 

<br />

<img src="https://github.com/davidyi0529/Reverse-Starter-Code-Tutorial_D/blob/main/Images/serverjs.png?raw=true" width="700" height="700">

<br />

Requires the necessary NPM packages that are essential to running the application.

Setting up the port and syncing it to the models directory for the database.

Create an express app to configure middleware needed for the authentication.

`Express-sessions` is used to keep track of login status's.

Requiring the routes to the correspond to the correct file in the `Routes` folder.

And then providing console prompt to the user that they are synced with the database server.

<br />
<br />

---

<br />
<br />