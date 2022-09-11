# Video Demo Link

[`Watch it on youtube`](https://youtu.be/_QZgKq77978)


# `NOTE`
If you're planning to run this app locally, YOU MUST SETUP YOUR POSTGRESQL SERVER AND UPDATE URL IN IN .ENV FILE. OTHERWISE IT SIMPLY WON'T RUN. THE SCHEMA FOR DB TABLE IS IN QUERY FILE.


# 🧭 Table of contents

- [Introduction](#Introduction)
- [🚀 Quick Start](#Quick-Start)
- [🚀 How this works](#How-this-works)
- [What this App Uses](#What-this-App-uses)
	- [`Frontend`](#Frontend)
	- [`Backend`](#Backend)
	- [`Database`](#Database)
- [Where is this Deployed](#Where-is-this-App-deployed)
- [Future Plans](#Future-Aspirations-for-this-App)
- [FAQs](#FAQ)


# Introduction

This is our Project for Submission in the Hackathon `HackOdisha 2.0`.

This is a web-App(App), which will help anyone(especially womens) to send SOS signal to others in any case of emergency and get immediete backup.

# Quick Start

📄 Clone or fork this repo and change current directory to `women-security`:

```sh
git clone https://github.com/anuragnotfound/women-security.git
```

💿 Install all dependencies:

```sh
cd women-security
npm install
```

✏ Rename `.env.example` to `.env` in the project folder and provide your `EMAIL`, `PASS`, `DATABASE_URL`. 
Example:

```jsx
SECRET_KEY = xxxx-xxxx-xxxx-xxxx
```

🚴‍♂️ Run your App:

```sh
npm start
```

# How this works

In order to use this App, Users must create an account by filling up the [Signup form](https://safety-for-women.herokuapp.com/new-user) followed by [Login](https://safety-for-women.herokuapp.com/).

### Login and Signup

Signup requires users to fill the following fields:
 - First Name (Required)
 - Last Name
 - Email (Required, Unique)
 - Password (Required)
 - Username (Required, Unique)
 - Referral Code (Required)

After Login User's will be redirected to Dashboard.

### Dashboard

At Dashboard, users can use all features of this App which includes:

- Send SOS
- Send Emergency Message
- Realtime text Chat
- Realtime Voice Chat
- Sending Location to Others
- See other online Users
- Wait for being rescued
- etc.

### Send SOS

This is a Big Red button, which when pressed, Send Distress Message to All the linked Email addresses and Telegram Channel.

The Message includes:

- User's name
- User's Location (if allowed)
- Rescue Button

### Rescue Button

when pressed, A response is sent to the person in distress that, this particular user has got your message and is coming to rescue you.

### Emergency Message

This is an Input Field, located just below the Big Red SOS button. 

When User Send a message through this endpoint, This is send to Telegram Channel and Linked Emails. The message contains:

- User's Name
- message
- Last location or Current Location (if available)
- Rescue Button

### Live Chat

Online User's can chat with each other through Text messages and VoiceChat (mic permission required). 
Chat Messages are not stored in Database and are restricted to Sessions only.
All the Chats disappear when current Active Browser Tab is closed.

### See Who else is online

Users can See Who is Online through the Online Section at bottom of the ChatBox.

# What this App uses

### This App has three main parts 
- [`Frontend`](#Frontend)
- [`Backend`](#Backend)
- [`Database`](#Database)


# Frontend

This App uses `HTML`,`CSS` and `Javascript` at its core for frontend applications.
This App runs on and rendered by  a `Nodejs` server.

# Backend

At the `Backend` of this App , A `Nodejs` server is running, which manages all the `requests` and `responses` from the user. 

This App Uses Some Node_Modules in order to work properly which includes:
- `socket.io`
  - Maintain active connection between Client and Server
  - Tranfer Text and voice Messages b/w Users and Server
  - Realtime Authentication
- `pg`
  - Connect to Database
  - Perform DB queries
  - perform DB I/O
- `Node-mailer`
  - Required to send Emails
- `BCryptJS`
  - Encrypt Passwords before storing in DB
  - Match Passwords on Login
- `jsonwebtoken`
  - Sign auth cookies
  - Verify cookies on each request
  - validate user login credentials
  - set expiry on Login Cookies
- `Telegraf`
  - Manage Telegram Bot
  - Send Messages in Telegram Channel via a Controlled Bot
- `Express`
  - create a web-server
  - handles request and response
- `multer`
  - handle images


# Database

This app uses `PostgreSQL` for all its database needs. This App uses DB to:
 
 - Store User Information
 - Implement Login, Signup and auth
 - Maintain an active mailing list
 - Implement mail-Unsubscribe features

# Where is this App deployed

Currently this dApp is deployed on Heroku as  [https://safety-for-women.herokuapp.com](https://safety-for-women.herokuapp.com).

# Future Aspirations for this App

There are some features which can be added in future:
 - Private Channels
 - Permanent Chats
 - Integration with Maps Services (google maps, etc)
 - Video Chat via webRTC
 - connection with other Social medias, most probably Discord.
 - Login via Face-Recognition
 - etc.
 

# FAQ

### Q1. Why this webApp uses Cookies ?

This App uses cookies to store encrypted AuthToken, which is required for Authentication,

### Q2. Why do you need Mic and Location Permissions ?

- Location permussions is required while sending your GPS coords along with SOS.
- Microphone permissions is required for voice chat features.

### Q3. Are my Voice, Text and Location secure ?

All the information are handled safely and can be verified by looking at the source code.

### Q4. What is Referral code ?

Referral Code is required while Creating a new Account. This is required to prevent bogus accounts and allow only valid persons to create an account.

### Q5. Why My SOS button is not working ?

make sure your browser allows 3rd party to store and manage cookies.

### Q6. I need more guidance. What can I do ?

Contact us through our EMAIL and SOCIAL-MEDIA if you have any other queries.

# ⭐️ `Star us`

If this repo helped you in any possible ways - please star this project, every star makes us very happy!

# 🤝 `Need help?`

If you need help with setting up the boilerplate or have other questions - don't hesitate to write to us on our [email](mailto:tachyonanurag@gmail.com) or social media  and we will check asap. [our Telegram Channel](https://t.me/safetyforwomen).




