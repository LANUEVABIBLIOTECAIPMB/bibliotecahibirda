# Library Management System

## Overview

This is a full-stack library management system built with React and Express.js. The application allows users to browse books, manage loans, and provides administrative features for library staff. It's designed for educational institutions, specifically referenced as "Instituto Padre Manuel Ballesteros" in the interface.

## System Architecture

### Frontend Architecture
- **Framework**: React 18 with TypeScript
- **Build Tool**: Vite for fast development and optimized builds
- **Styling**: Tailwind CSS with shadcn/ui component library
- **State Management**: TanStack Query (React Query) for server state management
- **Routing**: Wouter for client-side routing
- **Forms**: React Hook Form with Zod validation
- **UI Components**: Radix UI primitives with custom styling

### Backend Architecture
- **Runtime**: Node.js with Express.js server
- **Database**: PostgreSQL with Drizzle ORM (Active)
- **Database Provider**: Neon Database (@neondatabase/serverless)
- **Storage**: DatabaseStorage implementation with persistent data
- **API Design**: RESTful API with structured error handling
- **Session Management**: Express sessions with PostgreSQL storage
- **Development**: Hot module replacement with Vite integration

## Key Components

### Database Schema
The system uses three main entities:
- **Books**: Stores book information including title, author, ISBN, category, type (physical/digital), and availability status
- **Users**: Manages user accounts with roles (student, teacher, admin) and authentication
- **Loans**: Tracks book lending with due dates, return dates, and loan status

### API Endpoints
- `/api/books` - CRUD operations for books with search and filtering
- `/api/users` - User management and authentication
- `/api/loans` - Loan management and tracking
- `/api/statistics` - Dashboard metrics and reporting
- `/api/categories` - Book category management

### Frontend Pages
- **Catalog**: Browse and search books with filtering capabilities
- **Loans**: View active and historical loans with return functionality
- **Admin**: User management and system administration
- **Reports**: Statistics and analytics dashboard

## Data Flow

1. **User Authentication**: Session-based authentication with role-based access control
2. **Book Management**: CRUD operations with real-time status updates
3. **Loan Processing**: Automated loan creation with due date calculation
4. **Search & Filtering**: Real-time search with category and status filters
5. **Statistics**: Aggregated data for dashboard metrics

## External Dependencies

### Core Dependencies
- **@neondatabase/serverless**: PostgreSQL database connectivity
- **drizzle-orm**: Type-safe database ORM
- **@tanstack/react-query**: Server state management
- **@radix-ui/***: Accessible UI components
- **react-hook-form**: Form handling and validation
- **zod**: Schema validation
- **tailwindcss**: Utility-first CSS framework

### Development Tools
- **tsx**: TypeScript execution for development
- **esbuild**: Fast JavaScript bundler for production
- **vite**: Development server and build tool
- **@replit/vite-plugin-***: Replit-specific development enhancements

## Deployment Strategy

### Development
- Uses Vite dev server with HMR for fast development
- TypeScript compilation with strict type checking
- Environment variables for database configuration

### Production Build
- Vite builds the frontend to `dist/public`
- esbuild bundles the backend server to `dist/index.js`
- Static file serving integrated with Express

### Database
- PostgreSQL database with Drizzle migrations
- Schema defined in TypeScript with automatic type inference
- Connection pooling through Neon's serverless driver

## Changelog

```
Changelog:
- July 03, 2025. Initial setup
- July 03, 2025. Added landing page with custom Instituto Padre Manuel Ballesteros design
- July 03, 2025. Implemented Google Drive integration for file storage with local fallback
- July 03, 2025. Added file upload functionality for book covers and documents
- July 03, 2025. Fixed SelectItem component errors and improved form validation
- July 03, 2025. Enhanced user interface with professional branding
- July 03, 2025. Migrated from in-memory storage to PostgreSQL database
- July 03, 2025. Implemented DatabaseStorage with Drizzle ORM for persistent data
```

## Recent Features

### Landing Page
- Professional landing page with Instituto Padre Manuel Ballesteros branding
- Custom hero image showcasing the hybrid library concept
- Smooth navigation to main application

### File Storage System
- Google Drive integration for cloud storage of book covers and documents
- Automatic fallback to local storage when Drive is unavailable
- File upload support for images (JPG, PNG) and PDFs
- Secure file handling with 10MB size limits

### Enhanced UI/UX
- Fixed React component errors for better stability
- Improved form validation and error handling
- Professional color scheme matching institutional branding
- Responsive design for all device types

## User Preferences

```
Preferred communication style: Simple, everyday language.
```