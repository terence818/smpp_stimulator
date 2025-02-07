🚀 SMPP Backend Server

📖 Overview

This is the backend server for the SMPP Web Portal, built using Node.js and Express. It provides a REST API to manage SMPP connections, send messages, conduct load tests, and log activities. The backend interacts with MongoDB for data storage and uses JWT authentication for security.

🛠️ Technologies Used

Backend: Node.js, Express

Database: MongoDB

Authentication: JWT

Messaging Protocol: SMPP (via smppService)

Logging: Winston Logger

🔧 Installation & Setup

📌 Prerequisites

Node.js (v16 or later recommended)

MongoDB (Local or Cloud)

An SMPP server

📥 Setup Steps

1️⃣ Clone the repository:

git clone <repository_url>
cd <project_directory>

2️⃣ Install dependencies:

npm install

3️⃣ Set up environment variables:

Create a .env file in the project root with the following variables:

MONGODB_URI=<your_mongodb_connection_string>
JWT_SECRET=<your_jwt_secret>
PORT=3004

4️⃣ Start the backend server:

node src/app.js

5️⃣ Start the SMPP simulator server:

node smpp-server.js

🔗 API Endpoints

🔑 Authentication

POST /api/register - Register a new user

POST /api/login - Authenticate user and get JWT token

⚙️ Configuration

POST /api/saveconfig - Save SMPP configuration (Requires authentication)

GET /api/getconfig - Retrieve SMPP configuration (Requires authentication)

📜 Logging

GET /api/getlog - Get system logs (Requires authentication)

🔌 SMPP Management

POST /api/connectsmpp - Connect to SMPP server (Requires authentication)

POST /api/disconnectsmpp - Disconnect from SMPP server (Requires authentication)

POST /api/txonlysmpp - Set SMPP to TX (transmitter) mode (Requires authentication)

POST /api/rxonlysmpp - Set SMPP to RX (receiver) mode (Requires authentication)

GET /api/smppConnection - Get SMPP connection status

✉️ Messaging

POST /api/send-message - Send an SMPP message (Requires authentication)

POST /api/submit-message - Submit a message through the REST API (Requires authentication)

🚀 Load Testing

POST /api/loadtest - Start an SMPP load test (Requires authentication)

POST /api/abortloadtest - Abort an ongoing SMPP load test (Requires authentication)

📜 Logging

Logs are managed through the logger utility and stored in MongoDB.

📜 License

This project is for internal use and is not publicly licensed.

📩 Contact

For any issues or feature requests, please contact the project maintainer.

