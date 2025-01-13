# Simple CRUD Store with React, Express, MongoDB, and Node.js 🚀

## Table of Contents

- [Project Description](#project-description)
- [Technology Stack](#technology-stack)
- [Features](#features)
- [Screenshots](#screenshots)
- [Setup Instructions](#setup-instructions)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
  - [Running the Application Locally](#running-the-application-locally)
- [API Documentation](#api-documentation)
- [License](#license)

---

## Project Description

This project is a simple CRUD (Create, Read, Update, Delete) application for managing a store's inventory. Users can add, view, update, and delete items in the store. The application is built with a modern tech stack and provides an intuitive user interface.

---

## Technology Stack

- **Frontend**: React with Chakra UI for styling
- **Backend**: Express.js
- **Database**: MongoDB (MongoDB Atlas for cloud storage)
- **Language**: JavaScript

---

## Features

- Add new items to the store.
- View a list of all items in the store.
- Update details of existing items.
- Delete items from the store.
- Responsive and user-friendly UI.

---

## Screenshots

1. **Homepage**
   ![Homepage](/frontend/scereen_shot/1.png)
2. **Create Page**
   ![Create Page](/frontend/scereen_shot/2.png)
3. **Edit Modal**
   ![Edit Modal](/frontend/scereen_shot/3.png)

---

## Setup Instructions

### Prerequisites

- Node.js and npm installed.
- MongoDB Atlas account and connection string (already configured in `.env`).
- Git installed (optional for cloning the repository).

### Installation

1. Clone the repository:

   ```bash
   git clone <repository-url>
   cd <repository-folder>
   ```

### Build and Start the Application

1. To run the production build locally:

```bash
npm run build
npm run start
```

3. Open the application in your browser at `http://localhost:5000`.

---

## API Documentation

### Base URL

`http://localhost:5000/api`

### Endpoints

1. **Create an Item**

   - **POST** `/items`
   - **Request Body**:
     ```json
     {
       "name": "Item Name",
       "price": 100,
       "description": "Item Description"
     }
     ```
   - **Response**:
     ```json
     {
       "message": "Item created successfully",
       "data": { ... }
     }
     ```

2. **Retrieve All Items**

   - **GET** `/items`
   - **Response**:
     ```json
     [
       { "_id": "...", "name": "..." },
       { "_id": "...", "name": "..." }
     ]
     ```

3. **Update an Item**

   - **PUT** `/items/:id`
   - **Request Body**:
     ```json
     {
       "name": "Updated Name",
       "price": 120
     }
     ```
   - **Response**:
     ```json
     {
       "message": "Item updated successfully"
     }
     ```

4. **Delete an Item**
   - **DELETE** `/items/:id`
   - **Response**:
     ```json
     {
       "message": "Item deleted successfully"
     }
     ```

---

## License

This project is licensed under the MIT License. Feel free to use, modify, and distribute it as you see fit.
