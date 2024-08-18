# Combined Repository

This repository contains two submodules:

- [Server/API](https://github.com/shardaishwak/upstage-hack-api): Click here to go directly to the First Project repository to the API.
- [Client NextJS](https://github.com/KshitijGoyal2022/upstage-hack-client): Click here to go directly to the Second Project repository to the Client.

---

# Traventure

**Traventure** is a state-of-the-art travel application designed to revolutionize how you plan, book, and manage your trips. Whether you're traveling solo or with a group, Traventure provides an all-in-one platform for creating and managing detailed itineraries, booking accommodations and flights, and even handling communication in multiple languages. Leveraging AI-powered assistance and advanced APIs, Traventure simplifies every aspect of your travel experience, allowing you to focus on the journey itself.

## Table of Contents

- [Features](#features)
- [Getting Started](#getting-started)
- [Tech Stack](#tech-stack)
- [Installation](#installation)
- [Usage](#usage)
- [API Endpoints](#api-endpoints)
- [Architecture](#architecture)

## Features

- **User Authentication:** Secure and seamless authentication using Auth0.
- **Itinerary Management:** Effortlessly create, view, and manage personal or group travel itineraries.
- **Booking Management:** Manage bookings for flights, hotels, and activities, all in one place.
- **Passport Information Extraction:** Use OCR technology to extract and autofill passport details, speeding up the booking process.
- **AI-Powered Travel Assistance:** Engage with AI to receive tailored recommendations for flights, accommodations, and tourist attractions.
- **Multi-language Translation:** Real-time translation between English and Korean to assist with communication during your travels.
- **Interactive Maps:** Discover places to visit, hotels, restaurants, and entertainment using Mapbox-powered interactive maps.
- **Real-time Group Communication:** Users can create groups for itineraries and communicate with each other live using **Socket.io**, making trip planning collaborative and more efficient.
- **Seamless Integration:** Connects with multiple APIs, including Amadeus for flight information, Mapbox for place recommendations, and more.

## Getting Started

To get started with Traventure, follow the instructions below.

### Prerequisites

Ensure you have the following installed:

- Node.js 
- Yarn 
- A MongoDB instance (local or cloud)

### Tech Stack

- **Frontend:**
  - Next.js
  - React.js
  - Tailwind CSS for styling
  - Shadcn components for a modern and accessible UI
- **Backend:**
  - Node.js with Express.js
  - MongoDB for data storage
  - **Socket.io** for real-time group chat functionality
- **APIs:**
  - **Auth0:** Handles user authentication
  - **Upstage AI APIs:**
    - **Chat API:** AI-driven conversations for travel recommendations, including flights, hotels, and places to visit.
    - **Function Calling API:** Enables AI to retrieve real-time data about travel options by calling relevant APIs.
    - **Document OCR API:** Extracts passport and other travel document details to facilitate booking processes.
    - **Translation API:** Provides real-time translation between English and Korean.
  - **Amadeus Travel APIs:** Integrates flight search and booking functionalities.
  - **Mapbox API:** Powers the interactive maps for place recommendations, hotels, restaurants, entertainment, and more.
- **Other:**
  - Multer for file uploads
  - Axios for making HTTP requests

## Installation

### Clone the Repository

```bash
git clone https://github.com/shardaishwak/upstage-hack-api.git
git clone https://github.com/KshitijGoyal2022/upstage-hack-client.git
cd upstage-hack-api
cd upstage-hack client
```

### Install Dependencies and Run the Client

```bash
cd client
yarn
yarn dev
```

### Install Dependencies and Run the API

```bash
cd api
yarn
yarn dev
```

Your client application should now be running on `http://localhost:3000`, and your API server should be running on `http://localhost:5001`.

## Usage

### Itinerary Management

- **Create Itinerary:** Use the sidebar to create and manage itineraries. All itineraries are stored securely in MongoDB and can be accessed anytime.
- **View Itineraries:** A three-column layout allows you to navigate, manage bookings, and view itinerary details side by side.
- **Group Communication:** Utilize the integrated chat for discussing and coordinating plans within group itineraries.

### Real-time Group Communication

- **Live Chat with Socket.io:** Users can create groups for each itinerary and chat in real-time, discussing travel details, accommodations, or plans to proceed with the trip.
- **Collaborative Trip Planning:** The real-time chat functionality allows all members of a group to stay updated on the itinerary and make decisions together efficiently.

### Booking Management

- **View Bookings:** Access all your travel bookings via the booking sidebar.
- **Manage Bookings:** Click on a booking to view its details, make edits, or manage it as needed.

### Passport Information Extraction

- **Upload Passport:** Quickly upload your passport using the document upload feature.
- **Extract Information:** The OCR API extracts key details such as passport number, issuance date, and expiry date, which can then be reviewed and edited.

### AI-Powered Travel Assistance

- **Chat with AI:** Interact with an AI agent to get travel recommendations, including flights, accommodations, and places of interest.
- **Function Calling:** AI can directly interact with APIs to fetch real-time data about flights, hotels, and tourist attractions, enhancing your planning experience.

### Multi-language Translation

- **English-Korean Translation:** The Translation API facilitates real-time translation between English and Korean, making communication easier when traveling.

### Interactive Maps

- **Explore with Mapbox:** Discover and explore places to visit, hotels, restaurants, and entertainment using Mapbox-powered interactive maps integrated directly into the app.

  - **Place Recommendations:** Utilize Mapbox’s extensive geolocation data to find and explore nearby places of interest, including tourist attractions, restaurants, and entertainment venues.
  - **Hotel Search:** Search for and view hotels in your destination area with Mapbox’s detailed map features, including filters for price range, star ratings, and user reviews.
  - **Route Planning:** Plan your routes within the city, whether by foot, car, or public transportation, with Mapbox’s interactive mapping and direction services.

### Flight Search and Booking with Amadeus

- **Flight Search:** Seamlessly search for flights using the Amadeus Travel APIs, which provide comprehensive flight options based on your criteria such as destination, departure date, and number of passengers.
  
  - **Filtering Options:** Narrow down your search by airline, flight duration, number of stops, and price range.
  - **Real-Time Availability:** Get real-time flight availability and pricing to make informed booking decisions.

- **Booking Integration:** Directly book your selected flights through the application, with integration to Amadeus’s booking API, ensuring that your booking is secure and confirmed.

## API Endpoints

### Upstage AI APIs

- **Chat API**
  - **Description:** Engage users in AI-driven conversations to discuss and retrieve travel-related information.
  - **Functionality:** Provides tailored recommendations for flights, hotels, stays, and tourist attractions.

- **Function Calling API**
  - **Description:** Allows the AI to call specific APIs that provide real-time information about travel options.
  - **Functionality:** Connects chat interactions with backend services to pull up-to-date travel data.

- **Document OCR API**

    - **Description:** Upload a travel document (passport, ID card, visa) for OCR processing.
    - **Functionality:** Extracts and returns relevant details such as passport number, issuance country, and more.

- **Translation API**
  - **Description:** Facilitates real-time translation between English and Korean.
  - **Functionality:** Supports travelers by breaking down language barriers.

## Architecture

![Architecture Diagram](./public/architecture.svg)

For more detailed architecture planning and collaboration, visit our planning on [Excalidraw](https://excalidraw.com/#json=93V_lfHaprhUdDNqZ7hDo,bnOxTCY-qhXxyI7t2NkL_g).

