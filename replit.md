# Overview

This is an Iraqi educational platform called "تلجلج أكاديمي" (Taljalaj Academy) built for preparatory school students. The platform provides video lectures, teacher profiles, and subject materials in Arabic. It's a full-stack web application with a React frontend and Express.js backend, designed to help Iraqi students access educational content online.

# User Preferences

Preferred communication style: Simple, everyday language.

# System Architecture

## Frontend Architecture
- **Framework**: React 18 with TypeScript using Vite as the build tool
- **Styling**: Tailwind CSS with custom Arabic font (Tajawal) and RTL (right-to-left) layout support
- **UI Components**: Radix UI components with shadcn/ui design system for consistent, accessible UI elements
- **State Management**: TanStack React Query for server state management and caching
- **Routing**: Wouter for lightweight client-side routing
- **Forms**: React Hook Form with Zod validation for type-safe form handling

## Backend Architecture
- **Runtime**: Node.js with Express.js framework
- **Language**: TypeScript with ES modules
- **Database**: PostgreSQL with Neon serverless hosting and Drizzle ORM for type-safe database operations
- **Storage**: DatabaseStorage implementation connected to PostgreSQL with comprehensive CRUD operations
- **API Design**: RESTful API with proper error handling and request logging

## Database Schema
- **Subjects**: Educational subjects with Arabic and English names, teacher counts, icons, and color themes
- **Teachers**: Teacher profiles with avatar images, bio, experience, ratings, and review counts linked to subjects
- **Lectures**: Video lectures with episode numbers, thumbnails, metadata including duration, views, and timestamps
- **Relations**: Explicit foreign key relationships between subjects, teachers, and lectures using Drizzle relations

## Development Environment
- **Build System**: Vite for fast development and optimized production builds
- **Type Safety**: Comprehensive TypeScript configuration across frontend, backend, and shared code
- **Code Quality**: Consistent code organization with shared types and utilities
- **Development Tools**: Hot module replacement, error overlays, and development banners

## Key Features
- Arabic language support with RTL layout
- Subject browsing with visual cards and teacher counts
- Enhanced teacher profiles with avatar images, bio, ratings and experience
- Advanced video player with custom controls, volume, speed adjustment, and fullscreen mode
- Complete lecture series for Professor Haider Abdul A'ima (أ.د. حيدر عبد العائمة) with 15 episodes in Mathematics
- Authentic Iraqi teachers with proper Arabic names and academic credentials
- Video lecture system with view tracking and progress indicators
- Search functionality across subjects, teachers, and lectures
- Responsive design optimized for mobile and desktop
- Navigation tabs for different content types (subjects, teachers, classes, lectures)
- Purple color theme replacing the original blue design

## Recent Changes (August 10, 2025)
- ✓ Fixed database connection and initialization issues  
- ✓ Successfully removed all teachers, classes, and lectures from database
- ✓ Database is now clean and ready for new authentic educational content
- ✓ Fixed foreign key constraint issues in teacher deletion process
- ✓ Updated teacher count in subjects to reflect current state (0 teachers per subject)
- ✓ Application is running properly with empty teacher roster
- ✓ Completely redesigned and enhanced admin control panel with Arabic UI
- ✓ Fixed all default subject IDs to use correct Mathematics ID (e8b93e09-53ba-4473-ad04-c4baeb5547e2)
- ✓ Implemented comprehensive CRUD operations for teachers, classes, and lectures
- ✓ Added advanced form validation and error handling with Arabic messaging
- ✓ Enhanced UI with proper loading states, confirmation dialogs, and user feedback
- ✓ Tested all API endpoints and database constraints - working correctly
- ✓ Ready for authentic Iraqi educational content creation
- ✓ Completely rewrote video player with universal platform support (YouTube, Vimeo, Dropbox, Google Drive, OneDrive)
- ✓ Added iframe embedding for YouTube and Vimeo videos with native controls
- ✓ Fixed all video playback issues with enhanced error handling and retry mechanisms
- ✓ Removed "Educational Series" section and streamlined lecture display with mobile-optimized interface
- ✓ Added permanent back button visible outside video player for better navigation
- ✓ Enhanced video URL processing for automatic platform detection and conversion
- ✓ Changed class capacity from student count to lecture count (default 10 lectures)
- ✓ Updated all UI labels and database schema to reflect capacity as number of lectures
- ✓ Modified default capacity values throughout the admin panel interface
- ✓ Fixed missing POST /api/classes endpoint that was preventing class creation
- ✓ Updated subject selection component to show "عدد المحاضرات" instead of "السعة: طالب"
- ✓ Created ClassesGrid component and activated the classes tab in main navigation
- ✓ All CRUD operations for classes now working properly through admin panel and main interface
- ✓ Enhanced header with profile dropdown menu containing Gmail login and technical support links
- ✓ Profile menu integrates Telegram technical support bot and Gmail authentication
- ✓ Added comprehensive login dialog with Google OAuth and email login options
- ✓ Implemented user authentication system with database schema for users and sessions
- ✓ Created proper error handling for missing Google OAuth credentials with Arabic messages
- ✓ Enhanced security with bcrypt password hashing for user authentication
- ✓ Replaced all hardcoded subject IDs with dynamic default subject selection
- ✓ Converted all alert() notifications to modern toast notification system
- ✓ Improved error handling and user experience with Arabic toast messages
- ✓ Hidden pink/rose navigation header when entering subject pages for better focus
- ✓ Removed classes and lectures tabs from main navigation (August 10, 2025)
- ✓ Updated technical support to use Telegram bot: https://t.me/Talajlujbot?start=17dccbca4aa7ce89694fa2944fad2d7c9325714
- ✓ Simplified profile edit page by removing phone, bio, birth date, website, location, and occupation fields (August 10, 2025)
- ✓ Added Instagram profile link (https://www.instagram.com/7_yw2?igsh=MjM5cG9iMWt2Mzl6) to profile sidebar (August 10, 2025)
- ✓ Fixed login authentication issue - password hashing and comparison working correctly (August 10, 2025)
- ✓ Enhanced page navigation with smooth animations and transitions (August 10, 2025)
- ✓ Added "forgot password" functionality with backend endpoint support (August 10, 2025)
- ✓ Fixed database connection issues and created new PostgreSQL database with all tables (August 11, 2025)
- ✓ Fixed PostCSS syntax error in CSS file that was preventing application startup (August 11, 2025)
- ✓ Fixed API endpoint mismatch: corrected `/api/auth/signup` to `/api/auth/register` (August 11, 2025)
- ✓ Enhanced admin panel validation by replacing alert() with modern toast notifications (August 11, 2025)
- ✓ Verified all authentication functionality working: user registration, login, and session management (August 11, 2025)
- ✓ Confirmed admin panel fully functional: teacher creation, file uploads, and form validation working (August 11, 2025)
- ✓ Fixed classes display issue by re-adding classes tab to navigation and enabling ClassesGrid component (August 11, 2025)
- ✓ Fixed runtime plugin error by restarting the application - plugin overlay issue resolved (August 11, 2025)
- ✓ Enhanced video player controls for mobile devices with improved button sizing and spacing (August 11, 2025)
- ✓ Removed duplicate play button from video controls - kept only the central play button (August 11, 2025)
- ✓ Moved progress bar to bottom of video player and added click-to-toggle controls functionality (August 11, 2025)
- ✓ Added playback speed control (1x, 1.25x, 1.5x, 2x, 4x) with cycling button (August 11, 2025)
- ✓ Hidden interactive welcome section on mobile devices to improve video player focus (August 11, 2025)
- ✓ Restored welcome section visibility and removed classes tab from main navigation (August 11, 2025)
- ✓ Fixed video player controls and navigation structure (August 11, 2025)
- ✓ Enhanced video control bar positioning and styling - moved to bottom with improved design (August 11, 2025)
- ✓ Replaced central play button with improved play indicator and moved play button to control bar (August 11, 2025)
- ✓ Enhanced page transitions with smoother animations and better user experience (August 11, 2025)
- ✓ Added elegant Arabic-friendly page transitions with 3D effects and blur animations (August 11, 2025)
- ✓ Implemented staggered card animations for subjects and teachers grid (August 11, 2025)
- ✓ Fixed slideshow images upload functionality with integrated API endpoint (August 11, 2025)
- ✓ Temporarily added and removed classes tab from main navigation per user request (August 11, 2025)
- ✓ Resolved all API issues related to classesTable imports and references (August 11, 2025)
- ✓ Implemented comprehensive language switching system between Arabic and English (August 11, 2025)
- ✓ Added welcome back toast notifications for registered users returning to platform (August 11, 2025)
- ✓ Created multilingual support with RTL/LTR text direction switching (August 11, 2025)
- ✓ Enhanced user experience with personalized return visit detection and greeting system (August 11, 2025)

# External Dependencies

## Database and ORM
- **Neon Database**: Serverless PostgreSQL database hosting (@neondatabase/serverless)
- **Drizzle ORM**: Type-safe database toolkit with PostgreSQL dialect
- **Drizzle Kit**: Database migration and schema management tools

## UI and Styling
- **Radix UI**: Comprehensive set of accessible React components
- **Tailwind CSS**: Utility-first CSS framework with custom theming
- **Class Variance Authority**: Utility for creating variant-based component APIs
- **Lucide React**: Icon library for consistent iconography

## Development and Build Tools
- **Vite**: Fast build tool with React plugin and development server
- **TypeScript**: Static type checking across the entire codebase
- **ESBuild**: Fast JavaScript bundler for production builds

## State Management and Data Fetching
- **TanStack React Query**: Server state management with caching and synchronization
- **React Hook Form**: Form state management with validation
- **Hookform Resolvers**: Integration between React Hook Form and validation libraries

## Utilities and Helpers
- **Date-fns**: Date manipulation and formatting library
- **clsx**: Utility for constructing className strings
- **Zod**: TypeScript-first schema validation library
- **Nanoid**: URL-safe unique ID generator