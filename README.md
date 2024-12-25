# Social Media Application (MERN Stack)

## Overview
The **Social Media Application** is a platform built using the MERN stack (MongoDB, Express.js, React.js, Node.js) that allows users to connect, share, and interact with each other. The app includes features such as user authentication, posting updates, commenting, and liking posts, along with real-time notifications.

## Features

- **User Authentication**: Sign up and log in using email and password.
- **Post Creation**: Create, edit, and delete posts.
- **Likes and Comments**: Engage with posts by liking and commenting.
- **Real-Time Notifications**: Receive updates for likes, comments, and new followers.
- **User Profiles**: View and edit user profiles.
- **Follow/Unfollow**: Connect with other users by following them.
- **Search Functionality**: Search for users and posts.

## Tech Stack

- **Frontend**: React.js, Redux (for state management)
- **Backend**: Node.js, Express.js
- **Database**: MongoDB
- **APIs**: Cloudinary (for image uploads)
- **Authentication**: JWT (JSON Web Token)

## Installation

### Prerequisites
Ensure you have the following installed on your system:
- Node.js (v14 or higher)
- MongoDB (local or cloud-based, e.g., MongoDB Atlas)

### Steps

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/yourusername/social-media-app.git
   cd social-media-app
   ```

2. **Install Dependencies**:
   Navigate to both the `client` and `server` directories to install dependencies:
   ```bash
   cd client
   npm install
   cd ../server
   npm install
   ```

3. **Set Up Environment Variables**:
   Create a `.env` file in the `server` directory with the following keys:
   ```env
   PORT=5000
   MONGO_URI=your-mongodb-connection-string
   JWT_SECRET=your-jwt-secret
   CLOUDINARY_CLOUD_NAME=your-cloudinary-cloud-name
   CLOUDINARY_API_KEY=your-cloudinary-api-key
   CLOUDINARY_API_SECRET=your-cloudinary-api-secret
   ```

4. **Run the Application**:
   - Start the backend server:
     ```bash
     cd server
     npm start
     ```
   - Start the frontend client:
     ```bash
     cd client
     npm start
     ```

5. **Access the App**:
   Open your browser and navigate to `http://localhost:3000`.

## Folder Structure

```
social-media-app/
│
├── client/                # Frontend code
│   ├── public/            # Static files
│   ├── src/               # React app source code
│   │   ├── components/    # Reusable components
│   │   ├── pages/         # Pages for the app
│   │   ├── redux/         # Redux setup
│   │   └── App.js         # Root component
│
├── server/                # Backend code
│   ├── models/            # MongoDB models
│   ├── routes/            # API routes
│   ├── controllers/       # Route handlers
│   └── server.js          # Entry point
│
└── README.md              # Documentation
```

## API Endpoints

### User Authentication
- **POST /api/auth/register**: Register a new user
- **POST /api/auth/login**: Log in an existing user

### Post Management
- **POST /api/posts**: Create a new post
- **GET /api/posts**: Fetch all posts
- **GET /api/posts/:id**: Fetch a specific post
- **PUT /api/posts/:id**: Update a post
- **DELETE /api/posts/:id**: Delete a post

### User Profiles
- **GET /api/users/:id**: Fetch user profile
- **PUT /api/users/:id**: Update user profile

### Engagement
- **POST /api/posts/:id/like**: Like a post
- **POST /api/posts/:id/comment**: Comment on a post

## Contributing
Contributions are welcome! Please follow these steps:
1. Fork the repository.
2. Create a new branch (`feature/your-feature-name`).
3. Commit your changes.
4. Push to the branch.
5. Submit a pull request.

## License
This project is licensed under the [MIT License](LICENSE).

## Acknowledgements
- Cloudinary for image hosting.
- Open-source libraries and tools that made this project possible.
