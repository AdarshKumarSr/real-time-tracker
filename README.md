# Real-Time Tracker

A real-time location tracking application that allows users to track and share their live location with others on an interactive map. This app uses **Socket.IO** for real-time communication and **Leaflet** for rendering the map.

## Features

- **Real-time location tracking**: Share your live location with others.
- **Interactive map**: View the locations of other users on a map using **Leaflet**.
- **Socket.IO**: Real-time communication between clients and server to broadcast location updates.
- **Geolocation**: Uses the browser's geolocation API to track and update your position on the map.

## Installation

1. **Clone the repository**:
   ```bash
   git clone https://github.com/AdarshKumarSr/real-time-tracker.git
   cd real-time-tracker
   ```

2. **Install dependencies**:
   Make sure you have **Node.js** and **npm** installed. If not, [download and install Node.js](https://nodejs.org/).

   Then, run the following command in the project directory to install the required dependencies:
   ```bash
   npm install
   ```

3. **Start the server**:
   After installing the dependencies, start the server with:
   ```bash
   npm start
   ```

   This will start the server on port 3000. You can access the app in your browser at `http://localhost:3000`.

## Project Structure

- `app.js`: The main server file that sets up the Express server and handles Socket.IO connections.
- `views/index.ejs`: The EJS template that serves the HTML page with the map.
- `public/js/script.js`: The client-side JavaScript file responsible for handling geolocation, Socket.IO events, and updating the map.
- `public/css/style.css`: Custom CSS for styling the map and the page.

## Technologies Used

- **Node.js**: JavaScript runtime used to run the server.
- **Express**: Web framework for Node.js.
- **Socket.IO**: Library for real-time communication between the server and client.
- **Leaflet**: JavaScript library for creating interactive maps.
- **EJS**: Templating engine for rendering dynamic HTML content.
- **Geolocation API**: Built-in browser API for getting the user's geographical location.

## How It Works

1. When the page is loaded, the map is centered at [0, 0] (global coordinates).
2. The browser fetches the user's current location using the **Geolocation API**.
3. The user's location is sent to the server via **Socket.IO**, and the server broadcasts this data to all other connected clients.
4. The map is updated with a marker for each user, showing their current location.
5. If a user disconnects, their marker is removed from the map.

## Future Improvements

- Add **user authentication** so that users can have unique IDs and track each other more easily.
- **Persist location data** in a database for tracking users over time.
- Add a **notification system** to notify users when others enter or leave their vicinity.
- Optimize the app for **mobile devices** for better performance and usability.
