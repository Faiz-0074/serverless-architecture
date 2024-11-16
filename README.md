# Serverless Music Application

## Introduction

### Problem Statement
A company seeks to create a web-based music application enabling users to browse and manage music albums in a database. The application must complement an existing movie database application and leverage a serverless architecture to minimize the need for provisioning and managing servers.

### Objective
The objective of this project is to develop a web-based music application that allows users to:
- Browse music albums.
- Add, delete, and update music album entries in the database.  

The project employs a serverless architecture using **AWS Lambda**, **Amazon API Gateway**, **Amazon Cognito**, and **DynamoDB** to ensure scalability, cost-effectiveness, and efficiency.

---

## Background

The adoption of serverless architectures has grown due to their ability to handle unpredictable spikes in traffic, eliminate server management, and reduce operational costs. AWS Lambda provides a robust platform to implement this architecture.  

This project aims to expand the company’s offerings by building a music application with the following capabilities:
- Viewing, adding, deleting, and updating music albums.
- Securing access through user authentication and authorization.

---

## Technologies Used

### Core AWS Services
- **AWS Lambda**: For serverless backend logic to handle CRUD operations.
- **Amazon API Gateway**: For creating, managing, and securing APIs to interact with the backend.
- **Amazon DynamoDB**: For storing music album data in a scalable and serverless NoSQL database.
- **Amazon Cognito**: For user authentication and authorization.
- **Amazon S3**: For hosting the front-end website.

### Programming Languages & Tools
- **Python**: For developing Lambda functions.
- **HTML & JavaScript**: For creating the front-end interface.
- **AWS CLI**: For managing and uploading resources to AWS.

---

## Features
The application includes the following functionalities:
1. **View Albums**: Show all albums in the database or filter by genre.
2. **Add Album**: Allow users to add new album entries.
3. **Delete Album**: Allow users to remove albums from the database.
4. **Update Album**: Allow users to update non-key attributes of existing albums.
5. **User Authentication**: Secure the application with Amazon Cognito user pools for sign-up, login, and authorization.

---

## Methodology

### Step 1: Front-End Development
- Built a user interface using **HTML** and **JavaScript** for interacting with the music application.

### Step 2: Website Hosting
- Hosted the website on **Amazon S3** by:
  - Creating an S3 bucket configured for static website hosting.
  - Uploading website files using the **AWS CLI**.

### Step 3: User Authentication
- Configured **Amazon Cognito** for user authentication and authorization.
  - Enabled sign-up and sign-in functionalities with email verification.
  - Integrated Cognito authentication with the front-end.

### Step 4: Serverless Backend Development
- Developed backend logic using **AWS Lambda**:
  - Lambda functions written in **Python** for CRUD operations.
  - CRUD functionality includes:
    - `GET`: Retrieve all albums or filter by genre.
    - `POST`: Add a new album.
    - `PUT`: Update album details.
    - `DELETE`: Remove an album.

### Step 5: Database Setup
- Created a table in **DynamoDB** with attributes such as:
  - Artist Name
  - Genre
  - Album Name
  - Release Date
- Populated the table with sample data for testing.

### Step 6: API Integration
- Set up **Amazon API Gateway** endpoints to map HTTP methods (GET, POST, PUT, DELETE) to Lambda functions.
- Ensured seamless interaction between the front-end and back-end using REST APIs.

### Step 7: Deployment
- Deployed Lambda functions and API Gateway configurations using the AWS Lambda console.

### Step 8: Testing
- Conducted extensive testing to ensure the application meets functional requirements, including:
  - Front-end functionality.
  - Backend operations.
  - User authentication and authorization.

---

## Project Highlights

1. **Serverless Architecture**: Fully implemented using AWS services, eliminating the need for managing infrastructure.
2. **Scalability**: Dynamically handles varying loads with minimal latency.
3. **Cost-Effectiveness**: Pay-as-you-go pricing model reduces operational costs.
4. **User Security**: Robust authentication and authorization via Amazon Cognito.

---

## Folder Structure

```plaintext
.
├── frontend/
│   ├── index.html
│   ├── style.css
│   └── app.js
├── backend/
│   ├── lambda_functions/
│   │   ├── add_album.py
│   │   ├── delete_album.py
│   │   ├── update_album.py
│   │   └── get_albums.py
│   └── dynamodb/
│       └── table_schema.json
├── README.md
