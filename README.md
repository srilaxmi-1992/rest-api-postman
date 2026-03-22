# 🚀 Reqres API Automation (Postman + Newman)

This project demonstrates **end-to-end REST API testing** using
**Postman** with:

-   API Key Authorization\
-   Environment Variables\
-   Request Chaining\
-   Data-Driven Testing (CSV)\
-   Pre-request Scripts & Test Scripts\
-   Newman CLI execution

------------------------------------------------------------------------

## 📁 Project Structure

    project-root/
    │
    ├── collection/
    │   └── reqres_postman_collection.json
    │
    ├── environments/
    │   └── reqres_environment.json
    │
    ├── data/
    │   └── users.csv
    │
    └── README.md

------------------------------------------------------------------------

## 🔑 Features Covered

### 1. API Key Authorization

All requests use:

    x-api-key: {{api_key}}

------------------------------------------------------------------------

### 2. Environment Variables

-   baseUrl
-   userId
-   name
-   job
-   api_key

------------------------------------------------------------------------

### 3. Request Chaining

-   GET Users → extracts userId
-   CREATE User → updates userId
-   Used across all requests

------------------------------------------------------------------------

### 4. Data-Driven Testing (CSV)

Sample:

    name,job
    John,QA Engineer
    Alice,Developer
    Bob,Manager

------------------------------------------------------------------------

### 5. API Coverage

```bash
  Method   Endpoint        Description
  -------- --------------- -----------------
  GET      /users?page=1   Get all users
  POST     /users          Create user
  GET      /users/{id}     Get single user
  PUT      /users/{id}     Update user
  PATCH    /users/{id}     Partial update
  DELETE   /users/{id}     Delete user

``` 
------------------------------------------------------------------------

## ▶️ Run in Postman

1.  Import collection & environment\
2.  Select environment\
3.  Run collection\
4.  Upload CSV for data-driven tests

------------------------------------------------------------------------

## ⚡ Run Using Newman

### Install

    npm install -g newman

### Run
```bash

    newman run collection/reqres_postman_collection.json -e environments/reqres_environment.json -d data/users.csv

``` 

### HTML Report

```bash

    npm install -g newman-reporter-htmlextra

    newman run collection/reqres_postman_collection.json -e environments/reqres_environment.json -d data/users.csv -r htmlextra
```    

------------------------------------------------------------------------

## 🧪 Validations

-   Status codes
-   Response schema
-   Field validation
-   Dynamic variables
-   Logging

------------------------------------------------------------------------

## 📌 Highlights

-   Covers all HTTP methods\
-   Shows request chaining\
-   Demonstrates data-driven testing\
-   CLI execution using Newman

------------------------------------------------------------------------

## 👩‍💻 Author

Srilaxmi Amaraneni
