# Professional Service Portfolio Application

## Overview

This is a full-stack web application for showcasing professional services, built with React, TypeScript, Express, and PostgreSQL. The application provides a modern, responsive interface for displaying services, portfolio items, and handling client inquiries. It includes both client-facing functionality and admin capabilities for content management.

## System Architecture

### Frontend Architecture
- **Framework**: React 18 with TypeScript
- **Styling**: Tailwind CSS with shadcn/ui components
- **State Management**: TanStack Query for server state management
- **Routing**: Wouter for lightweight client-side routing
- **Form Handling**: React Hook Form with Zod validation
- **Build Tool**: Vite for fast development and optimized builds

### Backend Architecture
- **Runtime**: Node.js with Express framework
- **Language**: TypeScript with ESM modules
- **Database**: PostgreSQL with Drizzle ORM
- **Database Provider**: Neon serverless PostgreSQL
- **File Uploads**: Multer for handling image uploads
- **Session Management**: Express sessions with PostgreSQL store

### UI Component System
- **Design System**: shadcn/ui components based on Radix UI
- **Theme**: "new-york" style with CSS variables for theming
- **Icons**: Font Awesome and Lucide React icons
- **Typography**: Inter font family via Google Fonts

## Key Components

### Database Schema
- **Services**: Stores service offerings with pricing, descriptions, and features
- **Portfolio Items**: Manages project showcases with categories and technologies
- **Contact Submissions**: Handles client inquiries and contact form data

### API Endpoints
- **Services CRUD**: Full management of service offerings
- **Portfolio CRUD**: Complete portfolio item management
- **Contact Management**: Form submission handling and retrieval
- **File Upload**: Image upload functionality with file type validation

### Client Components
- **Hero Section**: Landing page with call-to-action buttons
- **Services Section**: Dynamic display of available services
- **Portfolio Section**: Filterable project showcase
- **Contact Section**: Contact form with validation
- **Admin Modal**: Administrative interface for content management

## Data Flow

1. **Client Request Flow**:
   - User interacts with React components
   - TanStack Query manages API calls and caching
   - Express server processes requests
   - Drizzle ORM handles database operations
   - Responses flow back through the same chain

2. **Admin Management Flow**:
   - Admin accesses management modal
   - Form submissions trigger API calls
   - Server validates and processes data
   - Database updates occur via Drizzle ORM
   - Client state refreshes automatically

3. **File Upload Flow**:
   - Admin uploads images via forms
   - Multer middleware processes files
   - Images stored in server uploads directory
   - Database stores file paths and metadata

## External Dependencies

### Core Dependencies
- **@neondatabase/serverless**: Neon PostgreSQL connection
- **drizzle-orm**: Type-safe database operations
- **@tanstack/react-query**: Server state management
- **react-hook-form**: Form state management
- **@hookform/resolvers**: Form validation integration
- **zod**: Schema validation
- **multer**: File upload handling

### UI Dependencies
- **@radix-ui/***: Comprehensive UI component primitives
- **tailwindcss**: Utility-first CSS framework
- **class-variance-authority**: Component variant management
- **lucide-react**: Icon library
- **date-fns**: Date manipulation utilities

### Development Dependencies
- **vite**: Build tool and development server
- **typescript**: Type checking and compilation
- **tsx**: TypeScript execution for development
- **esbuild**: Fast bundling for production builds

## Deployment Strategy

### Development Environment
- **Development Server**: Vite dev server with HMR
- **Backend Server**: Express with tsx for TypeScript execution
- **Database**: Neon PostgreSQL with connection pooling
- **File Storage**: Local filesystem for uploads

### Production Build Process
1. **Frontend Build**: Vite builds React app to `dist/public`
2. **Backend Build**: esbuild bundles Express server to `dist/index.js`
3. **Database Migration**: Drizzle Kit pushes schema changes
4. **Static Assets**: Vite handles asset optimization and bundling

### Environment Configuration
- **Database**: PostgreSQL connection via `DATABASE_URL`
- **File Uploads**: Configurable upload directory
- **Session Management**: PostgreSQL-backed sessions
- **CORS**: Configured for cross-origin requests

## Changelog

```
Changelog:
- July 06, 2025. Initial setup
```

## User Preferences

```
Preferred communication style: Simple, everyday language.
```