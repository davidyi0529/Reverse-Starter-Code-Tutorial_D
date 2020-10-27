<img src="https://github.com/davidyi0529/Portfolio_D/blob/master/assets/images/logo.png?raw=true" alt="alt text" title="David Yi">

<br />

# Reverse-Starter-Code-Tutorial_D

Reverse-Starter-Code-Tutorial_D.

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

3. Create a new MySQL database and name it `passport_demo`. Don't create any tables.

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

6. Navigate to localhost:3000 in the browser.

<br />

7. Have fun adding your new burgers and devouring them.

<br />
<br />

---

<br />
<br />





