# Running the application


# Ai-text-validator and Health Information Checker

## Overview
This application allows users to check the trustworthiness of health-related information by entering text and receiving an analysis based on an external API response.

## Functionality
- **Input Section**: Users can input text related to health information.
- **Analyze Button**: Clicking the "Analyze" button triggers an analysis of the provided text.
- **Response Display**:
  - If the health information is trustworthy, a green response is displayed with related details from the API.
  - If the information is doubtful, a yellow response is shown with alternative references from the API.
  - For fake information, a red response is displayed with links to the referenced content from the API.
  - If no text is entered, a generic response displays the opinion of the LARGE LANGUAGE MODEL.
- **Result Section**: Different colored buttons indicate the analysis result in case we havn't entred anything yet.

## Setup

### **1. Clone the Repository**

Clone this repository to your local machine and navigate into the project directory:

```bash
git clone https://github.com/abdelaliichou/Ai-text-validator.git
cd ai-text-validator


### **2. Build and Run the Docker Container**

```bash
docker build -t frontend .
docker run -p 3000:3000 frontend

### **3. Access the Application**

```bash
Once the container is running, access the web application:
Local Access in the browser: http://127.0.0.1:3000


## Usage
1. Enter health-related information in the input field.
2. Click the "Check reliability" button to trigger the analysis.
3. Observe the displayed response and buttons indicating the trustworthiness of the information.

Feel free to check the CSS file and structure of components for better understading.


# **AI Text Validator Backend**

This repository contains the backend for the AI Text Validator application, built with Python Flask. The application is containerized using Docker for easy deployment and scalability.

---

## **Project Setup**

### **1. Clone the Repository**

Clone this repository to your local machine and navigate into the project directory:

```bash
git clone https://github.com/abdelaliichou/ai-text-validator-backend.git
cd ai-text-validator-backend

### **2. Configure Environment Variables**

```bash
Create a .env file in the root directory and add your API keys and other environment-specific variables. Use the following format:
API_KEY=your_openai_api_key


### **3. Build and Run the Docker Container**

```bash
docker build -t backend .
docker run --env-file .env -p 10000:10000 backend


### **4. Access the Application**

```bash
Once the container is running, access the Flask application:
Local Access: http://127.0.0.1:10000
