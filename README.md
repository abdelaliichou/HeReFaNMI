# Running the complete application ( Front + Back) :

1. git clone https://github.com/abdelaliichou/HeReFaNMI.git
2. cd HeReFaNMI
3. docker compose up --build


# Overview
This application allows users to check the trustworthiness of health-related information by entering text and receiving an analysis based on an external API response.
The This repository contains also backend for the AI Text Validator application, built with Python Flask. The application is containerized using Docker for easy deployment and scalability.


## Functionality
- **Input Section**: Users can input text related to health information.
- **Analyze Button**: Clicking the "Analyze" button triggers an analysis of the provided text.
- **Response Display**:
  - If the health information is trustworthy, a green response is displayed with related details from the API.
  - If the information is doubtful, a yellow response is shown with alternative references from the API.
  - For fake information, a red response is displayed with links to the referenced content from the API.
  - If no text is entered, a generic response displays the opinion of the LARGE LANGUAGE MODEL.
- **Result Section**: Different colored buttons indicate the analysis result in case we havn't entred anything yet.


## Usage
1. Enter health-related information in the input field.
2. Click the "Check reliability" button to trigger the analysis.
3. Observe the displayed response and buttons indicating the trustworthiness of the information.

Feel free to check the CSS file and structure of components for better understading.


# Running only the Front-end :

1. git clone https://github.com/abdelaliichou/HeReFaNMI.git
2. cd HeReFaNMI
3. cd Frontend
4. docker build -t frontend .
5. docker run -p 3000:3000 frontend

### Access the Application :

Once the container is running, access the web application:
Local Access in the browser: http://127.0.0.1:3000


# Running only the Back-end :

1. git clone https://github.com/abdelaliichou/HeReFaNMI.git
2. cd HeReFaNMI
3. cd Backend

### Configure Environment Variables :

Create a .env file in the root directory and add your API keys and other environment-specific variables. Use the following format:

    API_KEY=your_openai_api_key
    FIREBASE_KEY=
    DATABASE_URL=

### Build and Run the Docker Container :

1. docker build -t backend .
2. docker run --env-file .env -p 10000:10000 backend

### Access the Application :

Once the container is running, access the Flask application:
Local Access: http://127.0.0.1:10000
