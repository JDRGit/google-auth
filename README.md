# Google Authentication with Firebase in React JS

This project demonstrates how to use Google Authentication with Firebase in a React JS application. We will focus on two separate ways to authenticate with Google:

- Sign in with a Google popup
- Redirect to Google Page

The logic for managing the authenticated state of the user will be stored in a React Context.

## How it works

I created an `AuthContext` using React's Context API. This context will store the authenticated user and provide functions to sign in and sign out.

The `AuthContextProvider` component wraps the application and provides the authentication context to all components in the app. It uses the `onAuthStateChanged` function from Firebase to listen for changes in the authentication state and update the user in our context accordingly.

The `googleSignIn` function triggers the Google sign-in process. You can choose to use either `signInWithPopup` or `signInWithRedirect` depending on your needs.

The `logOut` function allows the user to sign out.

Finally, the `UserAuth` hook allows any component in the app to access the user and the authentication functions.

## Notes
Before running this code, make sure that you have configured Firebase in your application and that you have enabled Google as a sign-in provider in your Firebase Authentication settings. You can find more information in the [Firebase documentation](https://firebase.google.com/docs/build?hl=en&authuser=0).


## Available Scripts

In the project directory, you can run:

### `yarn start`

Runs the app in the development mode.\
Open [http://localhost:3000](http://localhost:3000) to view it in your browser.

The page will reload when you make changes.\
You may also see any lint errors in the console.
