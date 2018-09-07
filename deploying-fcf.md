## Deploying Firebase Cloud Function

**Purpose:** We used cloud function for sending push notification for user based on some triggers like new messages, group creation..etc

### Let's do setup.

Before doing firebase setup, we need to install firebase tools on your machine. To do that, please execute

    npm install -g firebase-tools

### Step 1: Create new project & login to firebase

    mkdir fcf
    cd fcf
    firebase login
    firebase init functions

It might asks your few questions, please answer as followed

- Choose your firebase project
- Language: JavaScript
- EsLint: No
- Npm install: Yes

### Step 2: Installing Required dependencies

Then, we need to follow these steps,

    cd functions
    npm install --save firebase-admin
    npm install --save firebase-functions
    npm install --save request


### Step 3: Updating Files
After installation, we need to replace newly generated index.js file with downloaded index.js;

![updating service account]( https://github.com/codesundar/firebase-chat-ionic/blob/master/img/gauth3.png "updating service account")

- Rename downloaded files to ``service-account-key.json``
- Copy your ``service-account-key.json`` to ``fcf/functions/``

### Step 4: Deploying FCF
    cd ..
    firebase deploy --only functions

**Note:** You must be inside fcf/ (not inside fcf/functions) folder for deploying.

### Step 5: Updating CustomAuth URL

After deployment, you can see URL on console, which you need to update with your ``project/src/settings.ts``