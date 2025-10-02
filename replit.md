# Baking Maniac - Premium Bakery Landing Page

## Overview

Baking Maniac is a premium, dark-themed bakery landing page built with React and Express. The application showcases artisan baked goods through an elegant, luxury-focused e-commerce interface featuring professional product photography, smooth animations, and a sophisticated dark aesthetic with gold accents.

The application is a single-page website with sections for hero showcase, product specialties, about information, menu/portfolio, and contact forms. It includes shopping cart functionality and product browsing capabilities.

## User Preferences

Preferred communication style: Simple, everyday language.

## System Architecture

### Frontend Architecture

**Framework**: React 18 with TypeScript, using Vite as the build tool and development server.

**Routing**: Wouter for lightweight client-side routing (single route application with section-based navigation).

**State Management**: 
- TanStack Query (React Query) for server state management, caching, and data fetching
- Local React state (useState, useRef) for UI interactions and section navigation

**UI Component Library**: 
- shadcn/ui components built on Radix UI primitives
- Tailwind CSS for styling with custom dark theme configuration
- Custom design system following premium bakery aesthetic (defined in design_guidelines.md)

**Design System**:
- Dark mode primary theme with gold (#d4a574) accent colors
- Typography using Playfair Display (script font) and Poppins (sans-serif)
- Component-based architecture with reusable sections (Hero, Specialties, About, Menu, Portfolio, Contact)

### Backend Architecture

**Server Framework**: Express.js running on Node.js with TypeScript

**API Pattern**: RESTful API with JSON responses

**Session Management**: 
- express-session middleware for stateful sessions
- Session-based shopping cart (cart items tied to session ID)
- Cookie-based session storage with configurable security settings

**Storage Layer**: 
- In-memory storage implementation (MemStorage class)
- Interface-based design (IStorage) allowing future database integration
- Seeded product data for demonstration

**API Endpoints**:
- POST `/api/contact` - Submit contact form messages
- GET `/api/products` - Retrieve all products or filter by category
- GET `/api/products/:id` - Get single product details
- GET `/api/cart` - Retrieve cart items for current session
- POST `/api/cart` - Add item to cart
- PATCH `/api/cart/:id` - Update cart item quantity
- DELETE `/api/cart/:id` - Remove item from cart
- DELETE `/api/cart` - Clear entire cart

### Data Storage Solutions

**Current Implementation**: In-memory storage using JavaScript Maps for development/demo purposes

**Schema Definition**: Drizzle ORM schema defined for PostgreSQL migration path
- `contact_messages` table - Customer contact form submissions
- `products` table - Bakery product catalog
- `cart_items` table - Shopping cart entries with session tracking

**Validation**: Zod schemas generated from Drizzle schemas for runtime validation

**Future Database**: PostgreSQL with Neon serverless driver (configured but not currently active)

### Authentication and Authorization

**Current State**: No authentication system implemented

**Session Strategy**: Anonymous sessions using express-session with random UUID generation for cart tracking

### External Dependencies

**UI Framework**:
- Radix UI - Accessible component primitives (dialogs, dropdowns, navigation, etc.)
- Tailwind CSS - Utility-first CSS framework
- Lucide React & React Icons - Icon libraries

**Data Fetching**:
- TanStack Query - Async state management and caching
- Native fetch API for HTTP requests

**Form Handling**:
- React Hook Form - Form state management
- @hookform/resolvers - Zod validation integration

**Database (Prepared)**:
- Drizzle ORM - TypeScript ORM
- @neondatabase/serverless - PostgreSQL serverless driver
- connect-pg-simple - PostgreSQL session store (for production)

**Development Tools**:
- Vite - Build tool and dev server
- Replit plugins - Runtime error modal, cartographer, dev banner
- esbuild - Server bundle compilation

**Utilities**:
- date-fns - Date manipulation
- clsx & tailwind-merge - Conditional className utilities
- class-variance-authority - Type-safe variant styling
- nanoid - Unique ID generation

### Build and Deployment

**Development**: `npm run dev` - Runs Vite dev server with HMR and Express backend concurrently

**Production Build**: 
1. `vite build` - Builds client assets to dist/public
2. `esbuild` - Bundles server code to dist/index.js (ESM format)

**Production Server**: `npm start` - Runs compiled Express server serving static client assets

**Database Migrations**: `npm run db:push` - Pushes Drizzle schema to PostgreSQL (when database is provisioned)