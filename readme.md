# URL Shortener

## Table of Contents
- [Introduction](#introduction)
- [Features](#features)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Usage](#usage)
- [API Endpoints](#api-endpoints)
- [Contributing](#contributing)
- [License](#license)

## Introduction

This URL Shortener application is designed to help you learn how to create a web service that takes long URLs and generates shorter, more manageable links. This is achieved using Node.js for the server-side logic, Express for routing, and MongoDB for storing URL mappings.

## Features

- Shorten long URLs into more manageable links.
- Redirect shortened URLs to their original destinations.
- Simple and easy-to-understand codebase.
- Ideal for beginners and experienced developers looking to learn more about web development with Node.js, Express, and MongoDB.

## Prerequisites

Before you begin, ensure you have met the following requirements:
- Node.js and npm installed on your machine. You can download them from [Node.js](https://nodejs.org/).
- MongoDB installed and running. You can download it from [MongoDB](https://www.mongodb.com/try/download/community).

## Installation

1. Clone the repository:
    ```sh
    git clone https://github.com/saurin16/url-shortener.git
    cd url-shortener
    ```

2. Install the dependencies:
    ```sh
    npm install
    ```

3. Set up your environment variables. Create a `.env` file in the root directory and add the following:
    ```env
    MONGODB_URI=mongodb://localhost:27017/url-shortener
    PORT=8100
    BASE_URL=http://localhost:8100
    ```

## Usage

1. Start the MongoDB server if it is not already running:
    ```sh
    mongod
    ```

2. Start the application:
    ```sh
    npm start
    ```

3. Open your browser and navigate to `http://localhost:8100`.

## API Endpoints

- **POST /shorten**
    - Description: Create a shortened URL.
    - Request Body:
        ```json
        {
          "longUrl": "https://www.example.com"
        }
        ```
    - Response:
        ```json
        {
          "shortUrl": "http://localhost:8100/abc123"
        }
        ```

- **GET /:code**
    - Description: Redirect to the original URL based on the shortened code.
    - Response: Redirects to the original URL.

## Contributing

Contributions are welcome! Please fork this repository and submit pull requests.

1. Fork the Project.
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`).
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`).
4. Push to the Branch (`git push origin feature/AmazingFeature`).
5. Open a Pull Request.

