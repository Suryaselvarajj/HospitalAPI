# HospitalAPI

An API created using NodeJS for doctors to cater to the needs of the patients in the hospital during Covid-19.

## Run Locally

Clone the project

```bash
  git clone https://github.com/Suryaselvarajj/HospitalAPI.git
```

Go to the project directory

```bash
  cd HospitalAPI
```

Install dependencies

```bash
  npm install
```

Start the server

```bash
  npm start
```

## Documentation

Root Hosted Link - https://hospital-report-api-0vsl.onrender.com

Routes :

    a. /doctors/register - Registers a new Doctor.
    b. /doctors/login - Authenticates and returns the JWT token to be used.
    c. /patients/register - Allows a doctor to register a new patient (JWT Auth enabled).
    d. /patients/:id/create_report - Allows a doctor to create a patients report (JWT Auth enabled).
    e. /patients/:id/reports - Sends all the reports of a patient oldest to latest. (JWT Auth enabled).
    f. /reports/:status - List of all the reports of all patients with a specific status. (JWT Auth enabled).

Data that needs to be sent with a route :

    a. /doctors/register - name, email, password (Form type:x-www-form-urlencoded)
    b. /doctors/login - email, password (Form type:x-www-form-urlencoded).
    c. /patients/register - JWT Token (In Authorization ->choose bearer token & enter valid token), name, phone, age (Form type:x-www-form-urlencoded).
    d. /patients/:id/create_report - JWT Token (In Authorization ->choose bearer token & enter valid token), Patient's id , status (Form type:x-www-form-urlencoded). The :id can be copied from mongodb report
    e. /patients/:id/reports - JWT Token (In Authorization ->choose bearer token & enter valid token), Patient's id.
    the :id can be copied from mongodb report
    f. /reports/:status - JWT Token (In Authorization ->choose bearer token & enter valid token), status.

Folder Structure

    a. index.js - Server runs here
    b. model - Contains all the models for Doctor, Patient, Report.
    c. routes - Contains all the routes.
    d. controller - Contains all the controllers.
    e. config - Contains all the config files.
