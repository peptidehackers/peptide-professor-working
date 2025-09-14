# Peptide Professor - Research Platform

## Overview
Peptide Professor is a comprehensive research platform providing educational content about peptides, research tools, and safety information. The platform features a React frontend with a FastAPI backend, serving over 47 research peptides with detailed information, professional calculators, and medical oversight from Dr. Sheraz Ahmad, M.D.

## User Preferences
Preferred communication style: Simple, everyday language.

## System Architecture

### Frontend Architecture
- **Technology Stack**: React 18.2 with Create React App 5.0.1
- **Styling**: Tailwind CSS for responsive design
- **Routing**: React Router for single-page application navigation
- **State Management**: React Context API for global state (DataContext)
- **Build System**: Create React App with react-scripts
- **Static Generation**: react-snap for prerendering (conditional for Vercel)

### Backend Architecture
- **Framework**: FastAPI with Python
- **Server**: Uvicorn ASGI server
- **Database**: MongoDB with Motor async driver
- **Authentication**: JWT tokens with bcrypt password hashing
- **API Structure**: RESTful endpoints with comprehensive error handling
- **Security**: Rate limiting, CORS validation, request logging

### Data Storage Solutions
- **Primary Database**: MongoDB for dynamic content (peptides, blog posts, team members)
- **Fallback Data**: Static JSON files in frontend for offline functionality
- **Session Storage**: localStorage for calculator inputs and user preferences
- **Content Delivery**: Static files served via Vercel deployment

### Authentication and Authorization
- **User Authentication**: JWT-based authentication system
- **Password Security**: bcrypt hashing for password storage
- **API Security**: Rate limiting (60 requests/minute per IP)
- **CORS Protection**: Origin validation with allowlist
- **Security Headers**: CSP, X-Frame-Options, and other security headers

## External Dependencies

### Third-Party Services
- **Email Service**: Resend API for newsletter subscriptions and contact forms
- **Deployment**: Vercel for both frontend and serverless backend
- **Monitoring**: PostHog analytics for user behavior tracking
- **Medical Verification**: CMS NPI Registry API for doctor credential verification

### APIs and Integrations
- **Backend API**: Custom FastAPI server with endpoints for peptides, calculators, contact forms
- **Newsletter API**: Double opt-in email workflow with confirmation
- **Calculator APIs**: BMI, GLP-1 dosing, and peptide reconstitution calculators
- **Health Monitoring**: API health checks with cron monitoring

### Database Collections
- **Peptide Categories**: 13 categories with 47+ research peptides
- **Blog Posts**: 9 comprehensive articles with medical authorship
- **Team Members**: Leadership profiles with medical credentials
- **User Data**: Newsletter subscriptions and contact form submissions

### Development Dependencies
- **Testing**: Playwright for end-to-end testing
- **Build Tools**: Babel, TypeScript support
- **Code Quality**: ESLint for code linting
- **Package Management**: npm/yarn with package-lock.json