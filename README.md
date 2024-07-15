# QuantumBot-Core

- **Introduction**
This project entails setting up a development environment for Firebase functions and creating services such as a chatbot. The following points outline the setup process, folder structure, API creation, testing, and final submission.
  

- **Setting Up Development Environment**
  Install Node.js
Go to the Node.js website and download the installer.
Make sure to select npm during the installation.
Verify Node.js Installation
Open the VS Code terminal.
Run node --version to check if the installation was successful.
Install Firebase Tools
Run npm install -g firebase-tools to install the Firebase CLI.
Log in to Firebase
Run firebase login to authenticate your Firebase account.
Create Firebase Project
Go to the Firebase Console.
Create a new project or select an existing one.
Copy the Project ID from the Firebase console.
Configure Firebase Project
Update the .firebaserc file with your Project ID.
Modify firebase.json to include necessary Firebase features like functions and Firestore.
Initialize Firebase
Run firebase init.
Select Firestore and Functions.
Follow the prompts to complete the initialization.
Create Firestore Database
In Firebase Console, go to Build > Firestore Database.
Create a database in test mode.
  

- **Setting Up Firestore Collection and API Endpoint**
Create Firestore Collections
In the Firebase Console, create a collection named chats.
Add a sub-collection called messages.
Create API Endpoint
Define an HTTPS function in functions/api/addMessage.js.
Validate the request fields: text and userID.
Construct message data with text, userID, and a timestamp.
Add the message to the Firestore messages sub-collection.
Return a success or error response.
Deploy API Endpoint
Upgrade your Firebase plan to Blaze (pay-as-you-go).
Run firebase deploy --only functions to deploy the function.


- **Testing API Endpoint with Postman**
  - Create Workspace
    - Create a new workspace in Postman named `Chatbot`.
  - Test API Endpoint
    - Create a new HTTP POST request.
    - Set the endpoint URL from Firebase function.
    - Add headers: `Content-Type: application/json`.
    - Set request body to JSON format with appropriate data.
    - Send the request and verify the response.
    - Check Firestore database for the new message entry.

 **Screenshots**

 ![Screenshot 2024-07-14 235335](https://github.com/user-attachments/assets/9bb08c82-a54f-4d7d-84bf-5724b756bb3f)

 ![Screenshot 2024-07-14 235400](https://github.com/user-attachments/assets/4b6fbf4c-e101-49df-bb21-68679737ec8d)
 


