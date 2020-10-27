<img src="https://github.com/davidyi0529/Portfolio_D/blob/master/assets/images/logo.png?raw=true" alt="alt text" title="David Yi">

<br />

# Reverse-Starter-Code-Tutorial_D

Reverse-Starter-Code-Tutorial_D is a tutorial to provide a walk-through of the code with details on the functionality, which will allow the user to understand what each file does.

<br />

![Languages](https://img.shields.io/github/languages/top/davidyi0529/Reverse-Starter-Code-Tutorial_D )
<br />
![Last Commit](https://img.shields.io/github/last-commit/davidyi0529/Reverse-Starter-Code-Tutorial_D)
<br />
<br />

---

<br />
<br />

## Table of Contents

- [Application](#application)
- [Technologies](#technologies)
- [Installation](#installation)
- [Description](#description)
- [Support](#support)
- [License](#license)

<br />
<br />

---

<br />
<br />

## Application

<br />
<br />

This application allows the user to create an account with an email address and password. The user information is securely stored in a mysql database.

<br />
<br />

---

<br />
<br />

## Technologies

<br />
<br />

The following were used for this project.

- `bcryptjs` - provides password security
- `express` - Node.js web application framework
- `express-session` - creates a session middleware
- `mysql2` - MySQL client for Node.js
- `passport` - authentication middleware
- `passport-local` - authentication with a username and password
- `sequelize` - promise-based ORM

<br />
<br />

---

<br />
<br />

## Installation

<br />

1. To run the application, first clone this repository with the following command.

<br />

```bash
git clone https://github.com/davidyi0529/Reverse-Starter-Code-Tutorial_D.git
```

<br />

2. Next, install the application dependencies inside the Tutorial directory.

<br />

```bash
npm install
```

<br />

3. Create a new MySQL database and name it `passport_demo`.

<br />

<img src="https://github.com/davidyi0529/Reverse-Starter-Code-Tutorial_D/blob/main/Images/mysqldb.png?raw=true" width="300" height="300">

<br />
<br />

4. Open the `config` folder and update the `config.json` file's `development` object to match your own local MySQL database.

<br />

<img src="https://github.com/davidyi0529/Reverse-Starter-Code-Tutorial_D/blob/main/Images/Config.png?raw=true" width="300" height="300">

<br />
<br />

5. Start local host server with server.js.

<br />

```bash
node server.js
```
<br />

6. Navigate to your localhost in the browser.

<br />

<img src="https://github.com/davidyi0529/Reverse-Starter-Code-Tutorial_D/blob/main/Images/signuppage.png?raw=true" width="600" height="600">

<br />
<br />


7. Enjoy the app.

<br />
<br />

---

<br />
<br />

## Description

<br />
<br />

Below is explanation of the compilation of files used for this application.

- `config`
    - middleware
        - isAuthenticated.js
    - config.json
    - passport.js
- `models`
    - index.js
    - user.js
- `public`
    - js
        -login.js
        -members.js
        -signup.js
    - login.html, members.html, signup.html
- `routes`
    - api-routes.js
    - html-routes.js
- `package.json`
- `server.js`

<br />
<br />

---

<br />
<br />

## Support

<br />

Reach out to me at one of the following places!

> Linkedin @ <a href="www.linkedin.com/in/davidyi0529" target="_blank">`davidyi0529`</a> 

> Github @ <a href="https://github.com/davidyi0529" target="_blank">`davidyi0529`</a>

<br />
<br />

---

<br />
<br />

## License

<br />

![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)

<br />

Copyright &copy; All rights reserved.

Licensed under the [MIT](https://choosealicense.com/licenses/mit/) license.





