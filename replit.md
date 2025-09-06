# Overview

This is a personal portfolio website for Manjunath S Giraddi, a Full Stack Developer and Co-founder of Goblin Infotech. The application is built as a modern single-page application featuring a professional portfolio with sections for home, about, skills, projects, and contact. It includes interactive animations, a contact form with backend processing, and a comprehensive design system using shadcn/ui components.

# User Preferences

Preferred communication style: Simple, everyday language.

# System Architecture

## Frontend Architecture
The frontend is built using **React 18** with **TypeScript** for type safety. The application uses a component-based architecture with:

- **Vite** as the build tool for fast development and optimized production builds
- **Wouter** for lightweight client-side routing instead of React Router
- **Framer Motion** for smooth animations and transitions throughout the interface
- **Tailwind CSS** with custom CSS variables for consistent theming and responsive design
- **shadcn/ui** component library providing a comprehensive set of accessible UI components

The application follows a modular structure with reusable components, custom hooks for common functionality, and a centralized styling system using CSS custom properties for dark mode theming.

## Backend Architecture
The backend is built with **Express.js** using TypeScript and ESM modules. Key architectural decisions:

- **RESTful API** design with dedicated routes for contact form handling
- **In-memory storage** for development with an interface-based storage abstraction that can be easily swapped for database implementations
- **Zod validation** for runtime type checking and API request validation
- **Session-based architecture** prepared for future authentication features

The server integrates seamlessly with Vite in development mode, providing hot module replacement and serving both API routes and static assets.

## Data Layer
The application uses **Drizzle ORM** with **PostgreSQL** for production data persistence:

- **Type-safe database queries** with full TypeScript integration
- **Schema-first approach** with shared types between frontend and backend
- **Migration support** through Drizzle Kit for database version control
- **Neon Database** integration for serverless PostgreSQL hosting

The schema defines users and contacts tables with proper relationships and constraints, using UUID primary keys and timestamps for audit trails.

## Styling and Design System
The application implements a comprehensive design system:

- **Dark mode by default** with CSS custom properties for easy theme switching
- **Responsive design** with mobile-first approach using Tailwind's responsive utilities
- **Custom animations** using Framer Motion for enhanced user experience
- **Accessible components** from shadcn/ui ensuring WCAG compliance
- **Consistent spacing and typography** through design tokens

## Development and Build Process
The project uses modern development tools:

- **TypeScript** with strict configuration for type safety across the entire codebase
- **ESM modules** throughout both frontend and backend for modern JavaScript practices
- **Path mapping** for clean imports using @ aliases
- **Vite plugins** for development enhancements including error overlays and cartographer integration

# External Dependencies

## UI and Styling
- **@radix-ui/react-*** - Comprehensive collection of accessible UI primitives for building the component library
- **tailwindcss** - Utility-first CSS framework for rapid UI development
- **framer-motion** - Animation library for smooth transitions and interactive elements
- **class-variance-authority** - Utility for creating variant-based component APIs

## Data Management
- **@tanstack/react-query** - Server state management with caching, synchronization, and background updates
- **react-hook-form** - Form library with validation and efficient re-rendering
- **@hookform/resolvers** - Integration between react-hook-form and validation libraries

## Backend and Database
- **drizzle-orm** - TypeScript ORM for type-safe database operations
- **@neondatabase/serverless** - Serverless PostgreSQL database driver
- **zod** - TypeScript-first schema declaration and validation library
- **express** - Web application framework for Node.js

## Development Tools
- **vite** - Fast build tool with hot module replacement
- **typescript** - Static type checking for JavaScript
- **@replit/vite-plugin-*** - Replit-specific development enhancements

## Form and Validation
- **zod** - Runtime type validation for API requests and form data
- **drizzle-zod** - Integration between Drizzle ORM and Zod for schema validation

The application is designed to be easily deployable on Replit with built-in support for development tooling and production builds.