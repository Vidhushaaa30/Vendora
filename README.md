# Vendora
Vendora: A Comprehensive Stock and Inventory Management System 🛍️
Vendora is a prototype for a web-based inventory and stock management system designed for small businesses. It features separate dashboards for employees and owners to streamline daily operations, including stock tracking, bill uploading, and reordering.

Key Features
Employee Dashboard (stocks.html):
-View real-time stock levels.
-Add new products to the inventory.
-Update stock quantities for existing items.
-See visual alerts for low stock and expiring items.

Employee Requests (requests.html, reschedule.html):
-Employees can send requests for new stock or to reschedule tasks.
-Owners can review and approve these requests from a centralized dashboard.

-Invoice Management (invoice.html, ownerinvoice.html):
-Employees can upload bills and invoices.
-The owner's dashboard provides a view of all uploaded invoices.
-A built-in fraud detection feature helps flag suspicious or duplicate invoices.

Owner Dashboard (ownerdash.html):
-Get quick insights into low-stock items and upcoming expirations.
-Manage reorder requests to vendors.


Technologies Used
Frontend: HTML, CSS, and JavaScript.
Styling: Tailwind CSS
Backend: Firebase Firestore, a cloud-hosted NoSQL database.
Icons: Font Awesome


Setup Guide
Follow these steps to get the Vendora project up and running locally.

1. Prerequisites
A modern web browser (like Chrome, Firefox, or Edge).
A text editor or code editor (like VS Code, Sublime Text, or Notepad++).
A free Firebase account.

2. Firebase Project Setup
This is the most critical step to connect the application to a working database.
Go to the Firebase Console and sign in.
Click "Add project" and follow the on-screen instructions to create a new project.
Once the project is created, click the "Web" icon (</>) to add a new web app.

Register your app and copy the firebaseConfig object. It will look like this:

JavaScript:

const firebaseConfig = {
            apiKey: "AIzaSyAA-0m6frTwFh712zJOQv2CcblX-7o6G9Q",
            authDomain: "vendora-9c567.firebaseapp.com",
            projectId: "vendora-9c567",
            storageBucket: "vendora-9c567.firebasestorage.app",
            messagingSenderId: "278942178451",
            appId: "1:278942178451:web:cc16ba00fc671058178166",
            measurementId: "G-Z59E9PHSYL"
        };
Enable Firestore: In the left-hand menu of your Firebase project, go to "Build" -> "Firestore Database". Click "Create database" and select "Start in test mode".
You will need to create the stocks and requests collections in Firestore to store your data.

3. Code Configuration
Open each of your HTML files (stocks.html, reschedule.html, requests.html) in your code editor.
Find the <script> tag at the top of the file that contains the firebaseConfig object.
Replace the existing firebaseConfig object with the one you copied from your Firebase console.
You must do this for all your HTML files that interact with the database.

4. Running the Project
Save all your changes.
Open any of the HTML files (stocks.html, ownerdash.html, etc.) in your web browser.
The application should now be connected to your new Firebase database. You can start adding stock items or test other features.
