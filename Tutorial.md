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

Within the Config folder contains files needed for connectivity and login authentication.

<br />

1. `Middleware` - This folder contains a file called `isAuthenticated.js` which restricts any user to accessing certain routes without a login authentication.

<br />

<img src="https://github.com/davidyi0529/Reverse-Starter-Code-Tutorial_D/blob/main/Images/isAuthenticated.png?raw=true" width="700" height="200">

isAuthenticated.js is using a function to let the application know that if the requested object is a user then to direct the user to the requested route.

However, if the user is not logged in the it will return and redirect the user to the login page.

<br />

2. `config.json` - Provides connection configurations to connect to the server.

<img src="https://github.com/davidyi0529/Reverse-Starter-Code-Tutorial_D/blob/main/Images/Config.png?raw=true" width="500" height="400">

<br />

Configurations are provided for handling multiple environments (Development, Test, or Production).

<br />
<br />

---

<br />
<br />



- `config`

    - middleware
        - isAuthenticated.js - Restricts the user to access certain routes without login authentication. If the user is logged in, then it will continue with the users route request.
    
    - config.json - Connection configurations to connect to the server.

    - passport.js - Authentication with `Passport` to log in with an email address and password.

- `models`

    - index.js - Connects to database and imports users data logs.

    - user.js - Creation of user information that is stored into the database. Uses `bcrypt` for password hashing which allows a more secure database. 

- `public`
    - js
        - login.js - Login validation

        - members.js - Checks to see which user is logged in and updates the html page.

        - signup.js - New user creation validation

    - login.html, members.html, signup.html - Page layouts

- `routes`

    - api-routes.js - Routes for logging in and getting users data to be displayed client side.

    - html-routes.js - Routes to authenticate the user's login and re-direct the user to the correct html page.

- `package.json` - Contains all package information.

- `server.js` - Requires packages, sets up PORTS, creates express, middleware, routes, and syncs the database.