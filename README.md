


2. **Backend Setup**:
    ```bash
    cd server
    npm install
    ```

    - Create a `.env` file in the `server` directory with the following environment variables:
      ```bash
      PORT=5000
      MONGO_URI=<your_mongo_db_connection_string>
      ```

    - Start the backend server:
      ```bash
      npm start
      ```

3. **Frontend Setup**:
    ```bash
    cd ../client
    npm install
    ```

    - Create a `.env` file in the `client` directory with the following environment variables:
      ```bash
      REACT_APP_FIREBASE_API_KEY=<your_firebase_api_key>
      REACT_APP_FIREBASE_AUTH_DOMAIN=<your_firebase_auth_domain>
      REACT_APP_FIREBASE_PROJECT_ID=<your_firebase_project_id>
      REACT_APP_FIREBASE_STORAGE_BUCKET=<your_firebase_storage_bucket>
      REACT_APP_FIREBASE_MESSAGING_SENDER_ID=<your_firebase_messaging_sender_id>
      REACT_APP_FIREBASE_APP_ID=<your_firebase_app_id>
      ```

    - Start the frontend development server:
      ```bash
      npm start
      ```



### Authentication

- **Register User**: `POST /api/auth/register`
- **Login User**: `POST /api/auth/login`

### Students

- **Add Student**: `POST /form/insert`
  - **Request Body**:
    ```json
    {
        "Name": "John Doe",
        "Register_number": "12345",
        "Year_of_studying": "2",
        "Branch_of_studying": "CSE",
        "Date_of_Birth": "2000-01-01",
        "Gender": "Male",
        "Community": "General",
        "Minority_Community": "No",
        "Blood_Group": "O+",
        "Aadhar_number": "123456789012",
        "Mobile_number": "9876543210",
        "Email_id": "john.doe@example.com"
    }
    ```

- **Get Student**: `GET /remove/getStudent/:registerNumber`
  - **Response**:
    ```json
    {
        "_id": "60d1f5c8d6e5d435c8763e1a",
        "Name": "John Doe",
        "Register_number": "12345",
        "Year_of_studying": "2",
        "Branch_of_studying": "CSE",
        "Date_of_Birth": "2000-01-01",
        "Gender": "Male",
        "Community": "General",
        "Minority_Community": "No",
        "Blood_Group": "O+",
        "Aadhar_number": "123456789012",
        "Mobile_number": "9876543210",
        "Email_id": "john.doe@example.com"
    }
    ```

- **Delete Student**: `DELETE /remove/delete/:registerNumber`
  - **Response**:
    ```text
    Student removed successfully
    ```

### Attendance

- **Record Attendance**: `POST /attendance`
  - **Request Body**:
    ```json
    {
        "attendanceData": [
            {
                "studentId": "60d1f5c8d6e5d435c8763e1a",
                "attendance": "present"
            },
            {
                "studentId": "60d1f5c8d6e5d435c8763e1b",
                "attendance": "absent"
            }
        ]
    }
    ```


### Students

- **Get All Students**: `GET /read`
  - **Response**:
    ```json
    [
      {
          "_id": "60d1f5c8d6e5d435c8763e1a",
          "Name": "John Doe",
          "Register_number": "12345",
          "Year_of_studying": "2",
          "Branch_of_studying": "CSE",
          "Date_of_Birth": "2000-01-01",
          "Gender": "Male",
          "Community": "General",
          "Minority_Community": "No",
          "Blood_Group": "O+",
          "Aadhar_number": "123456789012",
          "Mobile_number": "9876543210",
          "Email_id": "john.doe@example.com"
      },
      ...
    ]
    ```

## Folder Structure

```
attendance-management-system/
│
├── client/                # React frontend
│   ├── public/
│  

 └──

 src/
│       ├── components/
│       ├── pages/
│       ├── App.js
│       ├── index.js
│       └── ...
│
├── server/                # Node.js backend
│   ├── models/
│   ├── routes/
│   ├── index.js
│   └── ...
│
├── .gitignore
├── README.md 
└── ...
```

## Contributing

Contributions are welcome! Please open an issue or submit a pull request.

## Contact

For any questions or suggestions, please reach out to:


---

Feel free to further customize the README according to your project's requirements and structure.

Happy coding 

**Cheers Gc**
 