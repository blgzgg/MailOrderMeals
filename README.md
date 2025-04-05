# Mail Order Meals 
Implemented a mobile order system for ordering boxes of specific varieties of foods. The
system allows customers to order these foods and stores those subscription-orders in a database.
The system will also retrieve data on the order so the user can see what they’ve ordered and the
details for that order, similar to the concept of a receipt.

An order placed by a customer can either be a one-time purchase or a subscription. The
subscription details can be set by the user, such as the frequency of delivery and size of the box
accounting for the varying amounts of people it will be serving. A utility for managing a user’s
subscription will also be provided.

Within the backend there were 2 main files that were used. Server.js encapsulated the
implementation of Express and Mongoose (for use with MongoDB). It connected to the database
and created routes for the front end and the queries.js file to use. Queries.js contains queries to
the mongoDB database (such as login and signup) to be used throughout the application. For the
backend, we had to install cors and mongoose and node dependencies to avoid issues running the
frontend and backend concurrently and connecting to the database.

There were numerous new React components we had to build for this application. As any
application with a user functionality, there needed to be a login and signup page, both of which
were separate components that interacted with the backend and the database to authenticate
users. The home page encapsulated the component “Product List” in order to hide the
functionality of the app unless the user was logged/signed in. The subscription and orders
components were used to let the user add a subscription and see their orders respectively. The
subscription page hit an api endpoint that created a new entry into the subscription database in
our MongoDB cluster. The orders page hit the same endpoint but with a get request to see the
orders that a given user had made. Finally the profile page displays the information about the
user and allows the functionality to logout of the application. On the frontend, we opted to use
the bootstrap framework as it seemed like the most simple and widely used. It made it very easy
to create the structure of our navigation bar and other styling.

# Getting Started with Create React App

This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

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

### `npm run eject`

**Note: this is a one-way operation. Once you `eject`, you can't go back!**

If you aren't satisfied with the build tool and configuration choices, you can `eject` at any time. This command will remove the single build dependency from your project.

Instead, it will copy all the configuration files and the transitive dependencies (webpack, Babel, ESLint, etc) right into your project so you have full control over them. All of the commands except `eject` will still work, but they will point to the copied scripts so you can tweak them. At this point you're on your own.

You don't have to ever use `eject`. The curated feature set is suitable for small and middle deployments, and you shouldn't feel obligated to use this feature. However we understand that this tool wouldn't be useful if you couldn't customize it when you are ready for it.

## Learn More

You can learn more in the [Create React App documentation](https://facebook.github.io/create-react-app/docs/getting-started).

To learn React, check out the [React documentation](https://reactjs.org/).

### Code Splitting

This section has moved here: [https://facebook.github.io/create-react-app/docs/code-splitting](https://facebook.github.io/create-react-app/docs/code-splitting)

### Analyzing the Bundle Size

This section has moved here: [https://facebook.github.io/create-react-app/docs/analyzing-the-bundle-size](https://facebook.github.io/create-react-app/docs/analyzing-the-bundle-size)

### Making a Progressive Web App

This section has moved here: [https://facebook.github.io/create-react-app/docs/making-a-progressive-web-app](https://facebook.github.io/create-react-app/docs/making-a-progressive-web-app)

### Advanced Configuration

This section has moved here: [https://facebook.github.io/create-react-app/docs/advanced-configuration](https://facebook.github.io/create-react-app/docs/advanced-configuration)

### Deployment

This section has moved here: [https://facebook.github.io/create-react-app/docs/deployment](https://facebook.github.io/create-react-app/docs/deployment)

### `npm run build` fails to minify

This section has moved here: [https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify](https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify)
