## Deploying Firebase Cloud Function

**Purpose:** We used cloud function for sending push notification for user based on some triggers like new messages, group creation..etc

### Let's do setup.

Before doing firebase setup, we need to install firebase tools on your machine. To do that, please execute

    npm install -g firebase-tools

### Create new project & login to firebase

    mkdir fcf
    cd fcf
    firebase login
    firebase init functions

It might asks your few questions, please answer as followed

- Choose your firebase project
- Language: JavaScript
- EsLint: No
- Npm install: Yes

Then replace your newly created index.js with downloaded index.js

    cd ..
    firebase deploy --only functions

**Note:** You must be inside fcf/ (not inside fcf/functions) folder for deploying.