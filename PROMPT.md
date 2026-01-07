# Hashman - Hashtag Generator Application

## Project Overview
Hashman is a modern, web-based hashtag generator application that allows users to create, save, and manage hashtag combinations for social media marketing. The application features a clean, dark-themed UI with a comprehensive authentication system and data persistence.

## Key Features

### Authentication & User Management
- User sign up with email validation and password strength requirements
- User login with session management
- Persistent user sessions across page reloads
- User data stored in localStorage (ready for backend integration)

### Hashtag Generation
- Multiple input categories (High/Mid/Low Volume Tags)
- Dynamic category management (add/remove categories)
- Word count tracking for each input
- Counter system that limits selection to available words
- Random hashtag combination generation
- Automatic "#" prefix for all generated hashtags
- Results displayed in a 2-column grid layout

### Results Management
- Save generated results with custom names
- View saved result sets in dashboard
- Delete saved sets
- Export results to CSV format
- Copy individual hashtags to clipboard
- Pagination for large result sets (10 results per page)

### User Interface
- Modern dark theme with gradient accents
- Responsive design optimized for mobile devices
- Sidebar navigation (appears after login)
- Header navigation (appears when logged out)
- Landing page with hero section, features, stats, and CTA
- Smooth animations and transitions
- ARIA accessibility standards

### Technical Stack
- Vanilla JavaScript (no frameworks)
- HTML5 with semantic markup
- CSS3 with custom properties (CSS variables)
- localStorage for data persistence
- Inter font family for typography
- SVG icons for UI elements

## File Structure
- `index.html` - Single-page application containing all HTML, CSS, and JavaScript
- `PROMPT.md` - This file, project documentation
- `LOGS.md` - Version history and changelog

## Current Version
v1.0.0 - Initial release with core features

## Future Enhancements
- Backend API integration for user authentication
- Cloud storage for saved results
- Advanced filtering and sorting options
- Hashtag analytics and insights
- Social media platform-specific optimizations
- Team collaboration features
