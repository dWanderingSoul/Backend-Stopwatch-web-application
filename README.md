# Backend-Stopwatch-web-application


This repository contains the backend code for a stopwatch web application.  While the core stopwatch functionality resides in the frontend (HTML, CSS, and JavaScript), this backend provides optional features like data persistence (saving lap times), user authentication, and real-time collaboration.

## Project Overview

This backend is designed to enhance a client-side stopwatch application with the following features (as needed):

* Saving lap times and other stopwatch data.
* User authentication.
* Real-time collaboration between multiple users.

## Features

* **Data Persistence:**
    * `/api/save`:  Endpoint to save stopwatch data (lap times, total time, user ID) via a POST request.
    * `/api/laps/:userId`: Endpoint to retrieve saved stopwatch data for a specific user via a GET request.
* **User Authentication:**  Implements user registration, login, and session management (or JWT) to associate stopwatch data with users.
* **Real-time Collaboration (Advanced):**  Uses WebSockets ( Socket.IO) to allow multiple users to view and interact with the same stopwatch in real-time.

## Technologies Used

* Node.js
* Express.js 
* Database  MongoDB
* Authentication library ( Passport.js) 
* WebSocket library; Socket.IO for real-time collaboration 

## Installation

1. Clone the repository: `git clone https://github.com/YOUR_USERNAME/YOUR_REPOSITORY.git`
2. Navigate to the project directory: `cd YOUR_REPOSITORY`
3. Install dependencies: `npm install`

## Usage

1. Configure the database connection and API keys (if needed) in the appropriate configuration files.
2. Start the server: `npm start` (or the command specified in your `package.json`).
3. The backend will be running on the specified port (e.g., `http://localhost:3000`).

## API Endpoints

* `/api/save`:  Saves stopwatch data.  Expects a JSON payload in the request body:

```json
{
  "userId": "user123", // Or however you identify users
  "lapTimes":, // Lap times in seconds
  "totalTime": 61.50 // Total time in seconds
}
