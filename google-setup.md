## Google Login Setup

This article, we're going to setup Google+ authentication.

## step 1: Enable Google login on Firebase

- Navigate to your firebase project
- Navigate to Authentication -> SignIn Method
- Enable Google Authentication
- Here you can see "WebClientId"
- Save It

![updating config]( https://github.com/codesundar/firebase-chat-ionic/blob/master/img/gauth1.png "updating config")


## Step 2: Updating Config files


- `project/config.xml` with **REVERSE webClientID**
![reverse client id]( https://github.com/codesundar/firebase-chat-ionic/blob/master/img/gauth3.png "reverse client id")


- Open your `project/src/settings.ts` & `project/package.json` update your **webClientId**

![gauth package]( https://github.com/codesundar/firebase-chat-ionic/blob/master/img/gauth-package.png "gauth package")


