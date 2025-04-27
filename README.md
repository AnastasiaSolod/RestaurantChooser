# Restaurant Chooser

## Overview

The Restaurant Chooser app helps groups of people decide where to eat by randomly selecting a restaurant while allowing for preferences and vetoes. It consists of three main screens:
- People Screen: Manage the list of people who can participate in decisions
- Restaurants Screen: Manage the list of potential restaurants
- Decision Screen: The core functionality for choosing a restaurant

## Prerequisites

Before running the app, ensure you have the following installed:
- Node.js (v14 or later)
- npm
- Expo CLI (`npm install -g expo-cli`)
- Android Studio (for Android emulator) or Xcode (for iOS simulator)

## Installation

1. Clone the repository:
`git clone [repository-url]`
`cd RestaurantChooser`
2. Install dependencies:
`npm install`
3. Install required Expo modules:
`npx expo install expo-constants expo-checkbox react-native-screens react-native-safe-area-context react-native-gesture-handler react-native-pager-view`
4. Install React Navigation dependencies:
`npm install @react-navigation/native @react-navigation/native-stack @react-navigation/material-top-tabs`

## Running the App

1. Start the development server:
`npx expo start`
2. Run on an emulator:
- For Android:
`npm run android`
- For iOS:
`npm run ios`
3. Alternatively, scan the QR code with the Expo Go app on your physical device.

## App Structure

The app follows this directory structure:

RestaurantChooser/
├── assets/            # Contains all images and icons
├── components/        # Custom components (CustomButton, CustomTextInput)
├── screens/           # All application screens
│   ├── PeopleScreen.js
│   ├── RestaurantsScreen.js
│   └── DecisionScreen.js
├── App.js             # Main application entry point
├── app.json           # Expo configuration
└── package.json       # Project dependencies

## Key Features

1. People Management:
- Add and delete people who can participate in restaurant decisions
- Store first name, last name, and relationship
2. Restaurant Management:
- Add and delete restaurants
- Store comprehensive restaurant details (name, cuisine, rating, etc.)
- Input validation for all fields
3. Decision Making:
- Select participants
- Apply filters (cuisine type, price, rating, delivery)
- Random restaurant selection with veto capability
- Final decision display

## Custom Components

The app uses two main custom components:
- CustomButton: A reusable button component with consistent styling
- CustomTextInput: An enhanced text input with label support and validation features

## Validation

The app includes comprehensive validation for:
- Restaurant names (minimum length, character restrictions)
- Phone numbers (format validation)
- Addresses (basic format checking)
- Website URLs (protocol and domain validation)
- Person names (basic validation)

## Navigation

The app uses React Navigation with:
- Material Top Tabs for main navigation (People, Decision, Restaurants)
- Stack Navigation for sub-screens (Add/List views)
- Modal components for decision popups

## Notes

- The app uses AsyncStorage for persistent data
- Platform-specific styling is implemented for consistent UI across iOS and Android
- All images are stored locally in the assets folder

Enjoy using the Restaurant Chooser app to simplify your group dining decisions!