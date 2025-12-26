# To-Do App Serverless

A serverless To-Do application built with AWS services, featuring user authentication, task management, and file attachments.

## Features

- **User Authentication**: Secure login and registration using Amazon Cognito
- **Task Management**: Create, read, update, and delete to-do items
- **File Attachments**: Upload and manage files associated with to-do items
- **Serverless Architecture**: Built with AWS Lambda, API Gateway, and DynamoDB
- **Responsive Frontend**: HTML/CSS/JavaScript based user interface

## Architecture

The application consists of:

- **Backend Services**:
  - Main Service: Handles core to-do operations (CRUD)
  - Attachments Service: Manages file uploads and downloads
- **Frontend**: Static web pages served via AWS services
- **Database**: Amazon DynamoDB for data storage
- **Authentication**: Amazon Cognito for user management

## Prerequisites

- AWS CLI configured with appropriate permissions
- Node.js and npm (for frontend dependencies)
- Python 3.8+ (for Lambda functions)
- AWS SAM CLI for deployment

## Setup and Deployment

### Backend Deployment

1. Navigate to the backend services:
   ```bash
   cd backend/main-service
   cd backend/attachments-service
   ```

2. Install dependencies and deploy using SAM:
   ```bash
   sam build
   sam deploy --guided
   ```

### Frontend Setup

1. The frontend consists of static HTML/CSS/JS files
2. Configure AWS services (Cognito User Pool, API Gateway URLs) in the JavaScript files
3. Deploy to AWS S3 or CloudFront for hosting

## Usage

1. Register/Login using the authentication pages
2. Create and manage your to-do items
3. Upload files as attachments to tasks
4. Mark tasks as complete or delete them

## Project Structure

```
├── backend/
│   ├── main-service/          # Core to-do operations
│   └── attachments-service/   # File attachment handling
├── frontend/                  # Static web interface
│   ├── css/
│   ├── js/
│   └── *.html
└── blog-post/                 # Documentation and diagrams
```

## Technologies Used

- **Backend**: AWS Lambda, API Gateway, DynamoDB
- **Frontend**: HTML5, CSS3, JavaScript
- **Authentication**: Amazon Cognito
- **Deployment**: AWS SAM
- **Storage**: Amazon S3 (for attachments)

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Submit a pull request

## License

This project is licensed under the MIT License.
