# UniformHub

A full-stack web application for managing uniform inventory, orders, and distribution. Built with Node.js and Express, demonstrating RESTful API design, modular architecture, and production-ready backend practices.

## Value Proposition

UniformHub solves the operational challenge of tracking uniform inventory and orders for organizations. It showcases ability to design scalable backend services, implement secure authentication, handle file uploads, and structure a maintainable full-stack application—skills directly applicable to enterprise web development roles.

## Core Features

- User authentication with JWT or session-based strategy and role-based access control
- RESTful API endpoints for products, orders, inventory, and user management
- Product catalog with image upload support via Multer middleware
- Order processing workflow with status tracking and validation
- Inventory monitoring with low-stock alerts and update triggers
- Environment-based configuration for secure credential management
- Modular Express architecture with separated routes, models, and middleware

## Technical Architecture

Backend: Node.js, Express.js, Mongoose (or Sequelize for SQL)
Database: MongoDB or PostgreSQL (configurable via environment variables)
File Handling: Multer for secure image uploads with type/size validation
Authentication: JSON Web Tokens or Express sessions with secure cookie flags
Environment Management: dotenv for separating config from code
API Design: RESTful conventions with consistent error handling and status codes

## Project Structure

UniformHub/
├── backend/
│   ├── server.js           # Express server initialization and middleware setup
│   ├── routes/             # API route definitions with validation
│   ├── models/             # Database schemas and business logic
│   ├── middleware/         # Auth, error handling, and request validation
│   ├── config/             # Database connection and environment config
│   └── utils/              # Helper functions and shared utilities
├── frontend/
│   ├── index.html          # Entry point for client application
│   ├── css/                # Stylesheets with responsive design
│   ├── js/                 # Client-side logic with fetch/axios API calls
│   └── assets/             # Static images and icons
├── uploads/                # Secure directory for user-uploaded images
├── .env.example            # Template for environment variables
├── .gitignore              # Excludes node_modules, .env, and build artifacts
├── Procfile                # Heroku deployment configuration (if used)
├── package.json            # Dependencies, scripts, and project metadata
└── README.md               # Project documentation

## Setup Instructions

1. Clone the repository
   git clone https://github.com/JeffJamez/uniforms.git
   cd uniforms

2. Install backend dependencies
   cd backend
   npm install

3. Configure environment variables
   - Copy .env.example to .env
   - Add required values: PORT, DATABASE_URL, JWT_SECRET, etc.

4. Start the development server
   npm start

5. Access the API at http://localhost:3000/api

## API Endpoint Examples

GET    /api/products          # Retrieve all uniform items with pagination
POST   /api/products          # Create a new product (admin only)
GET    /api/orders            # List orders with filtering options
POST   /api/orders            # Submit a new uniform order
POST   /api/auth/login        # Authenticate user and receive token
POST   /api/upload            # Upload product image with validation

## Key Technical Decisions

- Implemented middleware pipeline for consistent error handling and logging
- Used environment variables to separate configuration from code, enabling secure deployment
- Designed RESTful endpoints with clear resource nouns and HTTP verb semantics
- Applied input validation at route level to ensure data integrity before database operations
- Structured project with feature-based modules to improve scalability and team collaboration

## Security and Best Practices

- Passwords hashed with bcrypt before storage
- JWT tokens signed with secret and set with appropriate expiration
- CORS configured to restrict unauthorized cross-origin requests
- File uploads validated by type and size to prevent malicious content
- Database queries parameterized to prevent injection attacks

## Why This Project Stands Out to Recruiters

- Demonstrates end-to-end understanding of building a production-capable backend service
- Shows proficiency with modern JavaScript/Node.js patterns, async operations, and modular design
- Highlights ability to implement security fundamentals critical for real-world applications
- Clean, documented code that follows community conventions and is easy to extend
- Solves a tangible business problem with a scalable architecture ready for feature expansion

## Contributing

1. Fork the repository
2. Create a feature branch: git checkout -b feature/YourFeature
3. Commit changes: git commit -m 'Add YourFeature'
4. Push to branch: git push origin feature/YourFeature
5. Submit a pull request with a clear description of changes and any new dependencies

## License

MIT License. See LICENSE file for details.

## Author

Jeff James
