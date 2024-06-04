# FinalProject-
Final Project React and Node

PetExpress

PetExpress is a full-stack web application for managing and showcasing pet-related cards. Users can create, edit, delete, and like cards, as well as filter and search through their collection. It also includes features such as adding cards to a cart and handling phone calls related to the cards.
Table of Contents

    Project Structure
    Installation
    Usage
    Features
    Frontend
        Components
        Hooks
        Routes
        Context
        Toast Notifications
    Backend
        API Endpoints
        Database Schema
    Contributing
    License

Node Project Structure:

The project follows a well-organized structure to maintain clean and scalable code. Below is an overview of the main folders in the project:

bin
This folder contains the server startup script, typically www, which initializes and starts the Node.js application.

build
Contains the compiled version of the code if you're using a build tool to transpile your code (e.g., Babel or TypeScript).

controllers
Holds the logic for handling requests and responses. Each controller corresponds to a specific route or set of related routes.

initialData
Includes scripts or JSON files to populate the database with initial or seed data.

loggers
Contains configurations and utilities for logging. This helps in debugging and keeping track of application activities.

middlewares
Includes custom middleware functions used to process requests before they reach the controllers. Common tasks include authentication, validation, and error handling.

model
Contains the database schemas and models, defining the structure of the data used in the application.

normalize
Includes functions to normalize data, ensuring consistency in the format of the data being used or returned by the API.

public
Holds static files such as images, stylesheets, and client-side JavaScript that need to be served to the client.

routes
Defines the routes for the application, linking URL paths to specific controllers and their methods.

token
Contains utilities and configurations related to token generation and validation, typically for authentication purposes.

utils
Utility functions and helpers used across the application for various tasks.

validation
Includes schemas and functions for validating incoming request data, ensuring it meets the required formats and constraints.

env
Holds environment configuration files that define environment-specific settings and variables.
Installation



React Project structure:

The project is organized to maintain a clean and scalable codebase. Below is an overview of the main folders in the project:

build
Contains the production-ready version of the code, created after running the build process (e.g., with Webpack or Create React App).

public
Holds static files that need to be served directly by the web server, such as index.html, images, and other assets. These files are not processed by Webpack.

assets
Includes static assets like images, fonts, and other media files used throughout the application.

components
Contains reusable React components, which are the building blocks of the user interface. Each component typically has its own folder with related CSS and test files.

css
Stores global CSS files and style-related utilities. This can include stylesheets for theming, global resets, and common mixins.

guard
Includes higher-order components or utility functions for route protection and authorization logic, ensuring that only authenticated users can access certain routes.

hook
Custom hooks for encapsulating reusable logic that can be shared across multiple components. This helps in maintaining DRY (Don't Repeat Yourself) principles.

layout
Contains layout components that define the structure of the pages, such as headers, footers, sidebars, and navigation components.

pages
Each folder corresponds to a route in the application. These folders typically contain a main page component and any sub-components related to that specific page.

routes
Defines the routing logic of the application, mapping URL paths to specific components or pages. This often includes route configuration files and helper components for nested routes.

services
Includes modules that handle data fetching, API calls, and other interactions with external services. This layer abstracts away the details of data handling from the components.

store
Contains the state management logic, including Context store configuration, slices, actions, and reducers. This folder centralizes the application's state and logic.

validation
Includes schemas and functions for validating form inputs and other data structures used within the application, ensuring that data meets the required formats and constraints.



Install the dependencies:
npm install
PORT=3001


Start the backend server:
    npm start

Install the dependencies:
npm install
port 3030

Start the development server:
    npm run dev

!important .env file and set up the following environment variables in:
EXAMPLE.env file 
Usage

Once both the backend and frontend servers are running, you can access the application in your browser at http://localhost:3001.



Login and Authentication

    Users can log in to access personalized features such as managing their own cards and liking cards.
    The login state is managed using a context provider (LoginContext).

Managing Cards

    Users can create new cards, edit existing cards, delete cards, and like cards.
    Cards can be filtered and searched based on their titles.

Cart Management

    Users can add cards to their cart for easy reference.

Features

    Create, Edit, and Delete Cards: Manage your pet cards with ease.
    Like Cards: Like cards to add them to your favorites.
    Cart Functionality: Add cards to your cart and manage them.
    Filter and Search: Easily filter and search through cards.
    Toast Notifications: Receive feedback on your actions with toast notifications.

Frontend
Components

    MyCardComponent: Represents individual cards with actions like edit, delete, like, and add to cart.
    CardComponent: A component used to display cards in the cart.
    MyCards: Displays a list of cards created by the user.

Hooks
useMyCreatedCards

This custom hook manages the state and actions related to the user's created cards.

    State:
        dataFromServer: Stores the data fetched from the server.
        visibleItem: Controls the number of visible items.
    Actions:
        handleLoadMore: Loads more cards.
        handleDeleteCard: Deletes a card.
        handleEditCard: Navigates to the edit card page.
        handlePhoneCard: Simulates a phone call action.
        handleLikeCard: Likes a card.
        handleCartCard: Adds a card to the cart.
        handleMoveCard: Navigates to the card details page.

Routes

    Home: / - The home page of the application.
    About: /about - The about page of the application.
    How Autoship Works: /how-autoship-works - Information on how the autoship feature works.
    Order Prescriptions: /order-prescriptions - Order prescriptions for your pets.
    Register: /register - Register a new user.
    Login: /login - User login page.
    Edit Card: /edit-card - Edit a specific card.
    Create Card: /create-card - Create a new card.
    My Cards: /my-cards - Displays the user's created cards.
    Favorite Cards: /favorite-cards - Displays the user's favorite cards.
    Read Card: /read-card - Read the details of a specific card.
    Edit Profile: /edit-profile - Edit the user's profile.
    Update: /update - Update user information.
    Sandbox: /sandbox - A sandbox page for testing.
    Liked Count: /liked-count - Displays the count of liked items.
    Login Form: /login-form - User login form.
    Forgot Password: /forgot-password - Page for resetting password.
    Reset Password: /reset-password - Reset password page.
    Toy: /toy - Toys category page.
    Treat: /treat - Treats category page.
    Under 15: /under-15 - Products under $15 page.
    Food Deal: /food-deal - Food deals page.
    Exclusive to PetExpress: /exclusive-to-petexpress - Exclusive products to PetExpress.
    Dog: /dog - Dog category page.
    Cat: /cat - Cat category page.
    Bird: /bird - Bird category page.
    Small Pet: /small-pet - Small pet category page.
    Fish: /fish - Fish category page.
    Dog Food: /dog-food - Dog food category page.
    Cat Food: /cat-food - Cat food category page.
    Bird Food: /bird-food - Bird food category page.
    Small Pet Food: /small-pet-food - Small pet food category page.
    Fish Food: /fish-food - Fish food category page.
    Callback: /callback - Callback page for handling redirects.
    Cart: /cart - Displays the user's cart.

Context
LoginContext

Manages the login state and provides it to the rest of the application.
Toast Notifications

Toast notifications are used to provide feedback to the user on various actions such as creating, editing, deleting, and liking cards. The notifications are handled using react-toastify.


Backend
API Endpoints

User Routes

    GET /users/: Fetches all users. (Protected: Admin)
    POST /users/forgotPassword: Sends a password reset email.
    POST /users/resetPassword/
    : Resets the password using a token.
    POST /users/login: Logs in a user.
    POST /users/register: Registers a new user.
    GET /users/
    : Fetches a user by ID. (Protected: Admin or Own User)
    PUT /users/
    : Updates a user's information. (Protected: Admin or Own User)
    PATCH /users/
    : Updates a user's business status. (Protected: Admin or Own User)
    DELETE /users/
    : Deletes a user. (Protected: Admin or Own User)

Card Routes

    GET /cards/: Fetches all cards.
    GET /cards/categories: Fetches the list of categories.
    GET /cards/products/
    : Fetches cards by category.
    GET /cards/my-cards: Fetches the user's created cards. (Protected)
    GET /cards/
    : Fetches a card by ID.
    POST /cards/: Creates a new card. (Protected: Business User)
    PUT /cards/
    : Updates a card by ID. (Protected: Admin or Business User)
    PATCH /cards/
    : Likes a card or adds it to the cart. (Protected)
    PATCH /cards/biz-number/
    : Updates the business number of a card. (Protected: Admin)
    DELETE /cards/
    : Deletes a card by ID. (Protected: Admin or Business User)

Example Usage

// Fetch user's created cards
axios.get("/cards/my-cards")
  .then(({ data }) => {
    setDataFromServer(normalizeHome(data));
  })
  .catch((err) => {
    // Handle error
  });

// Like a card or add it to the cart
axios.patch(`/cards/${id}`)
  .then(({ data }) => {
    // Update state with new data
  })
  .catch((err) => {
    // Handle error
  });

// Delete a card
axios.delete(`/cards/${id}`)
  .then(({ data }) => {
    // Update state after deletion
  })
  .catch((err) => {
    // Handle error
  });

Database Schema

The application uses MongoDB to store data. Below is an example of the schema for the cards:

import mongoose from "mongoose";
import Image from "./Image.js";
import Address from "./Address.js";
import phoneRegex from "../../../utils/phoneRegex.js";
import { DEFAULT_REQUIRED_STRING_VALIDATION } from "../helper/defaultStringValidation.helper.js";
import emailRegex from "../../../utils/emailRegex.js";
import webRegex from "../../../utils/webRegex.js";
import priceRegex from "../../../utils/priceRegex.js";

export const categories = [
  "cat-food",
  "cat-toy",
  "dog-food",
  "dog-toy",
  "small-pet-food",
  "bird-food",
  "fish-food",
];

const CardSchema = new mongoose.Schema({
  title: DEFAULT_REQUIRED_STRING_VALIDATION,
  subtitle: DEFAULT_REQUIRED_STRING_VALIDATION,
  category: {
    type: String,
    required: true,
    enum: categories,
  },
  price: {
    type: Number,
    required: true,
    match: RegExp(priceRegex),
  },
  description: {
    ...DEFAULT_REQUIRED_STRING_VALIDATION,
    maxLength: 1024,
  },
  phone: {
    type: String,
    required: true,
    match: RegExp(phoneRegex),
  },
  email: {
    type: String,
    required: true,
    trim: true,
    match: RegExp(emailRegex),
  },
  web: {
    type: String,
    match: RegExp(webRegex),
    required: false,
  },
  image: Image,
  address: Address,
  bizNumber: {
    type: Number,
    minLength: 7,
    maxLength: 7,
    required: true,
  },
  category: {
    type: {
      name: {
        type: String,
        enum: categories,
      },
    },
    required: true,
  },
  likes: [String], // Array of user IDs who liked the card
  createdAt: {
    type: Date,
    default: Date.now,
  },
  cartItems: {
    type: [mongoose.Schema.Types.ObjectId],
    ref: "User",
    default: [],
  },
  user_id: {
    type: mongoose.Schema.Types.ObjectId,
  },
});

const Card = mongoose.model("card", CardSchema);

export default Card;

This schema includes various fields to store card information, such as title, subtitle, category, price, description, phone, email, web, image, address, bizNumber, likes, createdAt, cartItems, and user_id.
