# Store Product Management Web Application

## Introduction

This is a web application developed for a store where users can create product icons by adding the product name, price, and an image. These products are then displayed on the homepage in boxes. Users can also update or delete products as needed. The application is built using the MERN stack (MongoDB, Express.js, React, Node.js), and Chakra UI is used for building a responsive frontend.

## Features
- User can add products with name, price, and image.
- Products are displayed on the homepage in a grid of boxes.
- Users can update or delete products.
- Built with the MERN stack (MongoDB, Express.js, React, Node.js).
- Chakra UI for responsive and modern UI components.

## Technology Stack

### Backend
- **Node.js** - Runtime environment
- **Express.js** - Web framework
- **MongoDB** - NoSQL database
- **Mongoose** - MongoDB object modeling
- **dotenv** - Environment variable management
- **Nodemon** - Development server with auto-reload

### Frontend
- **React** - JavaScript library for building UI
- **Vite** - Build tool and development server
- **Chakra UI** - Component library for responsive design
- **React Router DOM** - Client-side routing
- **Zustand** - State management
- **React Icons** - Icon library
- **Framer Motion** - Animation library

## Prerequisites

Before you begin, ensure you have the following installed on your system:

- **Node.js** (v14 or higher) - [Download here](https://nodejs.org/)
- **npm** (comes with Node.js) or **yarn**
- **MongoDB** - You can use:
  - [MongoDB Atlas](https://www.mongodb.com/cloud/atlas) (Cloud-based - Recommended for beginners)
  - [Local MongoDB installation](https://www.mongodb.com/docs/manual/installation/)
- **Git** - [Download here](https://git-scm.com/downloads)

## Installation

Follow these steps to set up and run the application locally:

### 1. Clone the Repository

```bash
git clone https://github.com/RavijaDul/Store-Product-Management-Web-Application.git
cd Store-Product-Management-Web-Application
```

### 2. Install Backend Dependencies

```bash
npm install
```

### 3. Install Frontend Dependencies

```bash
cd frontend
npm install
cd ..
```

### 4. Configure Environment Variables

Create a `.env` file in the root directory of the project:

```bash
touch .env
```

Add the following environment variables to the `.env` file:

```env
MONGO_URL=your_mongodb_connection_string
PORT=5000
```

**Getting your MongoDB connection string:**

- **For MongoDB Atlas (Cloud):**
  1. Create a free account at [MongoDB Atlas](https://www.mongodb.com/cloud/atlas)
  2. Create a new cluster
  3. Click "Connect" and choose "Connect your application"
  4. Copy the connection string and replace `<password>` with your database user password
  5. Example: `mongodb+srv://username:password@cluster0.xxxxx.mongodb.net/store-products?retryWrites=true&w=majority`

- **For Local MongoDB:**
  - Use: `mongodb://localhost:27017/store-products`

## Running the Application

### Option 1: Run Backend and Frontend Separately

#### Start the Backend Server

From the root directory:

```bash
npm run dev
```

The backend server will start on `http://localhost:5000`

#### Start the Frontend Development Server

Open a new terminal window and run:

```bash
cd frontend
npm run dev
```

The frontend will start on `http://localhost:5173` (or another port if 5173 is in use)

### Option 2: Run Both Concurrently

You can open two terminal windows and run both commands simultaneously as described in Option 1.

## Using the Application

1. Open your browser and navigate to `http://localhost:5173`
2. You'll see the homepage where products are displayed
3. Click on "Create Product" or the "+" button to add a new product
4. Fill in the product name, price, and image URL
5. Click "Add Product" to save
6. View your products on the homepage
7. Use the edit icon to update a product
8. Use the delete icon to remove a product

## Project Structure

```
Store-Product-Management-Web-Application/
├── backend/
│   ├── config/
│   │   └── db.js              # Database configuration
│   ├── controllers/
│   │   └── product.controller.js  # Product business logic
│   ├── models/
│   │   └── product.model.js   # Product schema
│   ├── routes/
│   │   └── product.route.js   # API routes
│   └── server.js              # Backend entry point
├── frontend/
│   ├── src/
│   │   ├── components/        # Reusable components
│   │   ├── pages/             # Page components
│   │   ├── store/             # State management
│   │   ├── App.jsx            # Main App component
│   │   └── main.jsx           # Frontend entry point
│   ├── public/                # Static assets
│   └── vite.config.js         # Vite configuration
├── .env                       # Environment variables (create this)
├── .gitignore
├── package.json               # Backend dependencies
└── README.md
```

## API Endpoints

- `GET /api/products` - Get all products
- `POST /api/products` - Create a new product
- `PUT /api/products/:id` - Update a product
- `DELETE /api/products/:id` - Delete a product

## Development

### Backend Development

The backend uses Nodemon for auto-reloading during development. Any changes to the backend code will automatically restart the server.

### Frontend Development

The frontend uses Vite's hot module replacement (HMR) for instant updates during development.

### Linting

To run the frontend linter:

```bash
cd frontend
npm run lint
```

## Building for Production

### Build Frontend

```bash
cd frontend
npm run build
```

The production-ready files will be in the `frontend/dist` directory.

### Preview Production Build

```bash
cd frontend
npm run preview
```

## Troubleshooting

### Common Issues

1. **Port already in use:**
   - Change the PORT in your `.env` file
   - Or kill the process using the port

2. **MongoDB connection error:**
   - Verify your MongoDB connection string in `.env`
   - Ensure your IP address is whitelisted in MongoDB Atlas
   - Check if MongoDB service is running (for local installation)

3. **Dependencies not installing:**
   - Delete `node_modules` and `package-lock.json`
   - Run `npm install` again

4. **Frontend not connecting to backend:**
   - Ensure the backend is running on port 5000
   - Check the proxy configuration in `frontend/vite.config.js`

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is open source and available under the [MIT License](LICENSE).

## Author

Developed by [RavijaDul](https://github.com/RavijaDul)
