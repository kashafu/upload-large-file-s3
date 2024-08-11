
# Uploading Large Files to AWS-S3 with Lightning Fast Speed - Parallel Chunk Upload

## Upload API vs Presigned

### Presigned Multipart Upload
When It’s Easier:
* Client-Side Uploads: If you want to allow clients (e.g., browsers or mobile apps) to upload files directly to S3 without needing to handle AWS credentials on the client side, presigned URLs are easier to implement.
* Avoiding AWS Credentials: If you prefer not to expose AWS credentials to clients and want to delegate the upload process to them, presigned URLs offer a secure way to do this.


### Multipart Upload API
When It’s Easier:
* Server-Side Control: If you want complete control over the upload process, including handling large files, managing parts, and retrying failed uploads, then using the Multipart Upload API directly on the server side might be more straightforward.
* Server-Based Environments: If you have a backend server or application that can manage AWS credentials securely, implementing the Multipart Upload API is usually easier because you handle the entire process on the server.


This project demonstrates two techniques for uploading large files to AWS-S3: one where chunks are created on the frontend and uploaded using the AWS multipart API, and another where chunks are created on the backend and uploaded using the AWS SDK 3 upload parallel technique.

## Technique 1:

Creating Chunks on Frontend, then sending them to Backend and uploading to S3 bucket using AWS multipart upload API.

### Backend Code

Backend Folder: backend

To run this code: Install the required npm modules, by running the below command.
```
npm install
```

Create a .env file by copying the sample.env file and updating the necessary values.

Finally run the code using below command
```
npm start
```
  
### Frontend Code

Folder Folder: frontend

To run this code:

Install http-server globally using npm by running `npm install -g http-server`

Navigate to the frontend folder.

Start the server by running `http-server`

Open the provided URL in your web browser.


## Technique 2:

Uploading complete file from frontend then Creating Chunks on Backend and doing parallel upload using AWS SDK 3


### Backend Code

Backend Folder: backend2

To run this code: Install the required npm modules, by running the below command.
```
npm install
```

Create a .env file by copying the sample.env file and updating the necessary values.

Finally run the code using below command
```
npm start
```
  
### Frontend Code

Folder Folder: frontend2

To run this code:

Install http-server globally using npm by running `npm install -g http-server`

Navigate to the frontend folder.

Start the server by running `http-server`

Open the provided URL in your web browser.


## Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.
