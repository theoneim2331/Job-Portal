# Job Portal - Full Stack Application

A modern, full-featured job portal application built with React.js frontend and Node.js backend, featuring user authentication, job management, company profiles, and advanced search functionality.

## 🚀 Features

### For Job Seekers
- **User Registration & Authentication** - Secure signup/login system
- **Job Search & Filtering** - Advanced search with keyword, location, and industry filters
- **Category-based Browsing** - Quick access to jobs by categories
- **Job Applications** - Apply to jobs and track application status
- **Profile Management** - Update personal information and resume
- **Real-time Search** - Instant search results as you type

### For Recruiters
- **Company Management** - Create and manage company profiles with logos
- **Job Posting** - Post new jobs with detailed requirements
- **Applicant Management** - View and manage job applications
- **Job Analytics** - Track job performance and applications
- **User-specific Data** - Secure isolation of company and job data

### Technical Features
- **Responsive Design** - Works seamlessly on desktop and mobile
- **Real-time Updates** - Dynamic content updates without page refresh
- **Image Upload** - Cloudinary integration for company logos
- **State Management** - Redux Toolkit for consistent app state
- **Authentication Middleware** - Secure API endpoints
- **MongoDB Integration** - Robust data storage and retrieval

## 🛠️ Tech Stack

### Frontend
- **React.js** - Modern UI library
- **Redux Toolkit** - State management
- **React Router** - Client-side routing
- **Axios** - HTTP client for API calls
- **Tailwind CSS** - Utility-first CSS framework
- **Shadcn/UI** - Beautiful UI components
- **Vite** - Fast build tool and development server

### Backend
- **Node.js** - Server runtime
- **Express.js** - Web application framework
- **MongoDB** - NoSQL database
- **Mongoose** - MongoDB object modeling
- **JWT** - JSON Web Tokens for authentication
- **Bcrypt** - Password hashing
- **Multer** - File upload handling
- **Cloudinary** - Image storage and optimization

## 📁 Project Structure

```
JOB PORTAL/
├── Backend/
│   ├── controllers/        # Business logic
│   ├── models/             # Database schemas
│   ├── routes/             # API routes
│   ├── middlewares/        # Authentication & file upload
│   ├── utils/              # Utility functions
│   └── index.js            # Server entry point
│
├── Frontend/
│   ├── src/
│   │   ├── components/     # React components
│   │   │   ├── admin/      # Admin/Recruiter components
│   │   │   ├── ui/         # Reusable UI components
│   │   │   └── auth/       # Authentication components
│   │   ├── hooks/          # Custom React hooks
│   │   ├── redux/          # State management
│   │   ├── utils/          # Frontend utilities
│   │   └── lib/            # Library configurations
│   └── public/             # Static assets
│
└── README.md               # Project documentation
```

## 🚀 Getting Started

### Prerequisites
- Node.js (v14 or higher)
- MongoDB (local installation or MongoDB Atlas)
- Git

### Installation

1. **Clone the repository**
```bash
git clone https://github.com/yourusername/job-portal.git
cd job-portal
```

2. **Backend Setup**
```bash
cd Backend
npm install
```

3. **Environment Configuration**
Create a `.env` file in the Backend directory:
```env
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret_key
CLOUDINARY_CLOUD_NAME=your_cloudinary_cloud_name
CLOUDINARY_API_KEY=your_cloudinary_api_key
CLOUDINARY_API_SECRET=your_cloudinary_api_secret
PORT=8000
```

4. **Frontend Setup**
```bash
cd ../Frontend
npm install
```

5. **Start the Application**

Backend (Terminal 1):
```bash
cd Backend
npm run dev
```

Frontend (Terminal 2):
```bash
cd Frontend
npm run dev
```

The application will be available at:
- Frontend: `http://localhost:5173`
- Backend API: `http://localhost:8000`

## 📖 API Documentation

### Authentication Endpoints
- `POST /api/v1/user/register` - User registration
- `POST /api/v1/user/login` - User login
- `POST /api/v1/user/logout` - User logout
- `GET /api/v1/user/profile` - Get user profile
- `POST /api/v1/user/profile/update` - Update user profile

### Job Endpoints
- `GET /api/v1/job/get` - Get all jobs (with search)
- `GET /api/v1/job/getadminjobs` - Get recruiter's jobs
- `GET /api/v1/job/get/:id` - Get job by ID
- `POST /api/v1/job/create` - Create new job (Recruiter only)
- `PUT /api/v1/job/update/:id` - Update job (Recruiter only)

### Company Endpoints
- `GET /api/v1/company/get` - Get all companies
- `GET /api/v1/company/get/:id` - Get company by ID
- `POST /api/v1/company/register` - Register new company
- `PUT /api/v1/company/update/:id` - Update company

### Application Endpoints
- `GET /api/v1/application/get` - Get user's applications
- `GET /api/v1/application/:id/applicants` - Get job applicants
- `POST /api/v1/application/apply/:id` - Apply to job
- `POST /api/v1/application/status/:id/update` - Update application status

## 🎯 Key Features Implementation

### Search Functionality
- **Keyword Search**: Search across job titles, descriptions, and company names
- **Category Filtering**: Quick filter by predefined job categories
- **Location & Industry Filters**: Advanced filtering options
- **Real-time Search**: Instant results with debounced input

### User Authentication
- **Role-based Access**: Different interfaces for job seekers and recruiters
- **Secure Sessions**: JWT-based authentication with HTTP-only cookies
- **Protected Routes**: Frontend and backend route protection

### File Upload
- **Resume Upload**: PDF/DOC resume upload for job seekers
- **Company Logos**: Image upload with Cloudinary integration
- **File Validation**: Type and size restrictions for uploads

### State Management
- **Redux Toolkit**: Centralized state management
- **Persistent State**: User sessions and preferences
- **Real-time Updates**: Immediate UI updates on data changes

## 🧪 Testing

### Manual Testing Checklist

#### Authentication Flow
- [ ] User registration (job seeker/recruiter)
- [ ] User login with valid credentials
- [ ] User login with invalid credentials
- [ ] User logout and session cleanup
- [ ] Profile update functionality

#### Job Seeker Features
- [ ] Browse all jobs
- [ ] Search jobs by keyword
- [ ] Filter jobs by category
- [ ] Filter jobs by location/industry
- [ ] Apply to jobs
- [ ] View applied jobs
- [ ] Update profile and resume

#### Recruiter Features
- [ ] Create company profile
- [ ] Upload company logo
- [ ] Post new jobs with all fields
- [ ] View posted jobs
- [ ] View job applicants
- [ ] Update application status
- [ ] Edit company details

#### Search & Filtering
- [ ] Keyword search returns relevant results
- [ ] Category buttons filter correctly
- [ ] Location filter works
- [ ] Industry filter works
- [ ] Search clears properly
- [ ] No results message displays

#### Data Isolation
- [ ] Users only see their own companies
- [ ] Users only see their own posted jobs
- [ ] Application data is user-specific
- [ ] Logout clears all user data



## 👤 Author

**Sandeep Yadav**
- GitHub: [@10pie](https://github.com/10pie)
- LinkedIn: [Your LinkedIn](https://linkedin.com/in/sandeep-yadav-0b3758268)
- Email: theoneim31@gmail.com

## 🙏 Acknowledgments

- React.js community for excellent documentation
- Tailwind CSS for utility-first styling approach
- Shadcn/UI for beautiful component library
- MongoDB for flexible database solution
- Cloudinary for image management



---

**Happy Coding! 🎉**
