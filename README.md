# fs
# Digital E Gram Panchayat

A web application to manage citizen services for a Gram Panchayat, developed using HTML, CSS, JavaScript, and Firebase. This project aims to streamline various services provided at the Gram Panchayat level, such as registration and application tracking.

## Table of Contents
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Services](#services)

## Features
- **User Registration:** Citizens can register for services.
- **Application Tracking:** Users can track the status of their applications.
- **Admin Panel:** Admins can manage all applications and approve them.
- **Service Management:** Includes various services like birth registration, marriage registration, caste certificates, and more.
  

## Installation

To run this project locally, follow these steps:

1. Clone the repository:
    ```bash
    git clone https://github.com/yourusername/fs.git
    ```

2. Navigate to the project directory:
    ```bash
    cd digital-e-gram-panchayat
    ```

3. Open the `MAININDEX.html` file in your browser.

4. Make sure to set up Firebase and include your configuration in the project.

## Usage

1. Register an account to access services.
2. Apply for any service from the user portal.
3. Track the status of your application on the status page.
4. Admins can log in to manage applications and approve them.
5. users can login with the process of register with email and password.
6. staff portal can be accessed by the members of staff only. so for that authenticated user id must be used means a user need to authenticate the email and password from realtime database manaually.
7. admin portal can be accessed by the admin only. so for that authenticated user id must be used means a user need to authenticate the email and password from realtime database manaually.
 

## Services

The following services are currently available:

- **Birth Registration**
- **Marriage Registration**
- **Caste Certificate**
- **EWS Certificate**
- **Income Certificate**
- **Pension Applications**
- **Land Applications**







## Firebase Setup

1. Go to the [Firebase Console](https://console.firebase.google.com/).
2. Create a new project or select an existing one.
3. Click on "Add App" and select your platform (Web).
4. Copy your Firebase configuration details.
5. Create a `.env` file in the root directory of the project and add the following lines with your Firebase configuration:

    ```plaintext
    FIREBASE_API_KEY=your_api_key
    FIREBASE_AUTH_DOMAIN=your_project_id.firebaseapp.com
    FIREBASE_DATABASE_URL=https://your_project_id.firebaseio.com
    FIREBASE_PROJECT_ID=your_project_id
    FIREBASE_STORAGE_BUCKET=your_project_id.appspot.com
    FIREBASE_MESSAGING_SENDER_ID=your_messaging_sender_id
    FIREBASE_APP_ID=your_app_id
    ```

6. Review Firebase Rules
Check your Firebase Realtime Database security rules. If the rules are too restrictive, they might be preventing the read operation. Ensure that the rules allow read access to the relevant data paths for authenticated users.
Example of a permissive rule (for testing only):
json
Copy code
{
  "rules": {
    ".read": "auth != null",
    ".write": "auth != null"
  }
}
Make sure to adjust these rules according to your application's security needs.
To implement Admin and Staff login functionality using Firebase's Realtime Database for your Digital E Gram Panchayat project, you can follow these steps. Firebase Authentication will handle user logins, and the Realtime Database will store user roles (Admin or Staff) to differentiate access levels.

1. Set up Firebase Authentication
Firebase Authentication will manage user logins, while the Realtime Database will manage user roles.

Steps:
Go to your Firebase console.
Enable Email/Password Authentication in the Authentication section.
2. Set Up Realtime Database for Roles
You’ll use Firebase's Realtime Database to store and manage user roles (Admin or Staff).

Database Structure Example:
json
Copy code
{
  "users": {
    "userID1": {
      "email": "admin@example.com",
      "role": "admin"
    },
    "userID2": {
      "email": "staff@example.com",
      "role": "staff"
    },
    "userID3": {
      "email": "user@example.com",
      "role": "user"
    }
  }
}
Each user in the database will have a role field that determines whether they are an admin, staff, or a regular user.



## Usage

After setting up Firebase, you can run the project locally and connect to your own Firebase database.


