# Digital Heritage Platform

A MERN-based web application for creating a digital space for Indian heritage through crowdsourced description writing, image collection, and image annotation workflows.

## Overview

This project was built to provide a common digital platform for collecting, organizing, and describing digitized Indian heritage content. It supports a job-based workflow where providers create tasks, clients complete them, and admins manage available job types.

The platform currently supports three types of jobs:
- Writing description
- Adding images
- Annotating images

The annotation workflow reuses the CROWDANN editor developed in a previous project and stores annotation coordinates in JSON format.

## Features

- User registration and login
- Role-based access for Admin, Provider, and Client
- JWT-based authentication using session storage
- Dynamic job-type management through the admin portal
- Job posting and solution submission workflows
- Image upload and storage support
- Annotation editor integration using HTML5 Canvas
- Downloadable annotation results in JSON format

## User Roles

### Admin
- Add or delete job types
- Access user and job lists
- View submitted jobs
- View submission details for users

### Provider
- Create jobs from available job types
- Post image- and metadata-based tasks
- View submitted solutions
- Download annotation outputs in JSON format
- View submitter details

### Client
- Complete assigned jobs
- Write descriptions for images
- Upload images for collection tasks
- Annotate images using the editor
- View new and completed jobs through a toggle-based client page

## Job Types

### Writing Description
The provider uploads an image and title, and the client writes a description for that image.

### Adding Images
The provider specifies the requested image collection, and the client uploads multiple images.

### Annotating Images
The provider uploads an image and title, and the client annotates the image using the integrated editor. The annotations are stored as pixel coordinates and can be downloaded by the provider in JSON format.

## Tech Stack

- MongoDB
- Express.js
- React
- Node.js
- Mongoose
- Multer
- HTML5 Canvas
- CSS
- JavaScript

## Architecture

The project consists of three main layers:

1. Frontend  
   Built with React, CSS, and HTML5 Canvas for the user interface and annotation editor.

2. REST APIs  
   Built with Node.js and Express for authentication, job management, and submission handling.

3. Database  
   Uses MongoDB with Mongoose for storing users, job types, jobs, solutions, and metadata.

The application runs on two ports:
- Frontend server
- Backend REST API server

JWT tokens are issued during login, stored in session storage, and sent with requests for authentication.

## Storage and Data Handling

- MongoDB is used for storing structured application data
- Mongoose is used for schema modeling and database interaction
- Multer is used for image storage and upload handling
- Annotation data is stored as coordinates and can be exported in JSON format

## Workflow

1. A user registers as either a Provider or a Client.
2. The user logs in and receives a JWT token.
3. Providers create jobs based on available job types.
4. Clients browse and complete jobs.
5. Submitted solutions are saved in the database.
6. Providers review and download results, including annotation data where applicable.
7. Admins can create new job types that automatically appear in the provider workflow.

## Screens and Modules

- Authentication and registration
- Provider dashboard
- Client dashboard
- Admin dashboard
- Job type management
- Annotation editor
- Job submission and review

## Future Work

- Deploy the web application
- Add more job types
- Improve scalability
- Expand the annotation workflow and digital collection features

## Credits

Developed as a B.Tech. project at IIT Jodhpur.

Contributors:
- Manish Kumar (B17CS032)
- Manisha (B17CS033)

Supervisor:
- Dr. Suman Kundu
