# Proj 31 Backend API

A Node.js backend API with MongoDB integration for managing data.

## Features

- Express.js REST API
- MongoDB database with Mongoose ODM
- CORS enabled for frontend integration
- Environment variable configuration
- Flexible data schema

## Setup

1. Install dependencies:
```bash
npm install
```

2. Configure environment variables:
   - The `.env` file is already configured with your MongoDB connection string
   - You can modify `PORT` if needed (default: 5000)

3. Start the development server:
```bash
npm run dev
```

Or for production:
```bash
npm start
```

## API Endpoints

### Base URL
`http://localhost:5000`

### Endpoints

- **GET /** - Welcome message and API info
- **GET /api/data** - Get all data from the database
- **GET /api/data/:id** - Get a single data item by ID
- **POST /api/data** - Create a new data entry
- **DELETE /api/data/:id** - Delete a data item by ID

## Example Usage

### Get all data
```bash
curl http://localhost:5000/api/data
```

### Create new data
```bash
curl -X POST http://localhost:5000/api/data \
  -H "Content-Type: application/json" \
  -d '{"title":"Sample","description":"Test data"}'
```

## Project Structure

```
Proj 31/
├── config/
│   └── db.js           # MongoDB connection configuration
├── models/
│   └── Data.js         # Mongoose data model
├── routes/
│   └── dataRoutes.js   # API route handlers
├── .env                # Environment variables
├── .gitignore          # Git ignore file
├── package.json        # Project dependencies
├── server.js           # Main server file
└── index.html          # Frontend file
```

## Technologies Used

- Node.js
- Express.js
- MongoDB
- Mongoose
- dotenv
- CORS
