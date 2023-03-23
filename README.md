# Getting Started with Create React App

This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

## Steps to create a new React App:

1. `npx create-react-app ReactApp-ExpenseTracker`
2. `cd ReactApp-ExpenseTracker`
3. `npm start`

## Available Scripts

In the project directory, you can run:

### `npm start`

Runs the app in the development mode.\
Open [http://localhost:3000](http://localhost:3000) to view it in your browser.

The page will reload when you make changes.\
You may also see any lint errors in the console.

### `npm test`

Launches the test runner in the interactive watch mode.\
See the section about [running tests](https://facebook.github.io/create-react-app/docs/running-tests) for more information.

### `npm run build`

Builds the app for production to the `build` folder.\
It correctly bundles React in production mode and optimizes the build for the best performance.

The build is minified and the filenames include the hashes.\
Your app is ready to be deployed!

See the section about [deployment](https://facebook.github.io/create-react-app/docs/deployment) for more information.

## Deploying React app on github pages:
Considering app has been created and has been pushed to a repository, follow these steps:

### 1. Install the [`gh-pages`](https://github.com/tschaub/gh-pages) npm package and designate it as a [development dependency](https://nodejs.dev/learn/npm-dependencies-and-devdependencies):
 
    ```shell
    $ npm install gh-pages --save-dev
    ```
    
### 2. Add a [`homepage`]() property to the `package.json` file
   - Open the `package.json` file in a text editor.
   
   - Add a `homepage` property in this format\*: `https://{username}.github.io/{repo-name}`

      ```diff
       {
      "name": "my-app",
      "version": "0.1.0",
      "homepage": "https://heismanish.github.io/ReactApp-ExpenseTracker",
          "private": true,

      ```
      At this point, the React app's `package.json` file includes a property named `homepage`.

### 3. Add deployment scripts to the `package.json` file

    - Add a `predeploy` property and a `deploy` property to the `scripts` object:
    
      ```diff
      "scripts": {
      +   "predeploy": "npm run build",
      +   "deploy": "gh-pages -d build",
          "start": "react-scripts start",
          "build": "react-scripts build",
      ```
      At this point, the  React app's `package.json` file includes deployment scripts.
      
### 4. Commit all the changes ot the repository and deploy.
     - Deploy the app from Branch :`gh-pages`
