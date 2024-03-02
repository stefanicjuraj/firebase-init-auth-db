# Firebase Initialization Authentication Database

This repository contains an initialization setup for a Firebase Authentication and Database web application.

## Setup

### Setup Prerequisites

- [Google](https://www.google.com/account/about/) & [Firebase](https://firebase.google.com/) accounts.
- [Firebase console](https://console.firebase.google.com/) to create a project and register an application.
- Set up Firebase Authentication and Database within your Firebase project.

## Installation

1. Create and navigate to your project root folder.
2. Initialize your project &rarr; `npm init`
3. Install Firebase tools &rarr; `npm i -D firebase-tools`
4. Login to Firebase &rarr; `npx firebase login --add`
5. Enable Firebase web frameworks usage &rarr; `npx firebase experiments:enable webframeworks`
6. Initialize Firebase &rarr; `npx firebase init hosting`, and follow the prompts to set up your Firebase project.
7. After project initialization, navigate to your project root folder &rarr; `cd (your project root folder)`
8. Install Firebase &rarr; `npm i firebase`
9. Install project dependencies &rarr; `npm install`
10. Start the development environment &rarr; `npm run dev`

## Initialization

```javascript
// Imports
import { initializeApp } from "firebase/app";
import { getFirestore } from "firebase/firestore";
import { getAuth } from "firebase/auth";

// Firebase configuration stored in an '.env' file
const firebaseConfig = {
  apiKey: process.env.API_KEY,
  authDomain: process.env.AUTH_DOMAIN,
  projectId: process.env.PROJECT_ID,
  storageBucket: process.env.STORAGE_BUCKET,
  messagingSenderId: process.env.MESSAGING_SENDER_ID,
  appId: process.env.APP_ID,
};

// Initialize application
const app = initializeApp(firebaseConfig);
// Initialize database
export const auth = getAuth(app);
// Initialize authentication
export const db = getFirestore(app);
```
