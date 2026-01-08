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
- **Supabase** for authentication and backend services
- localStorage for client-side data persistence
- Inter font family for typography
- SVG icons for UI elements

## File Structure
- `index.html` - Single-page application containing all HTML, CSS, and JavaScript
- `PROMPT.md` - This file, project documentation
- `LOGS.md` - Version history and changelog
- `SUPABASE_SETUP.md` - Supabase authentication setup guide

## Supabase Configuration
The application uses Supabase for authentication. To set up:
1. Create a Supabase project at https://supabase.com
2. Get your project URL and anon key from the Supabase dashboard
3. Update the configuration in `index.html`:
   ```javascript
   const SUPABASE_URL = 'YOUR_SUPABASE_URL';
   const SUPABASE_ANON_KEY = 'YOUR_SUPABASE_ANON_KEY';
   ```
4. See `SUPABASE_SETUP.md` for detailed setup instructions

## Current Version
v1.0.0 - Static HTML/JS implementation (Current)

## Version History
- **v1.0.0** - Static HTML/JS implementation with Supabase authentication
- **v1.1.0 (Next.js)** - Experimental Next.js version (removed)
  - Attempted migration to Next.js 16 with TypeScript
  - Included shadcn/ui components
  - Route protection with middleware
  - Profiles table integration
  - **Status: Removed - Returning to static implementation**

## Future Enhancements
- Backend API integration for user authentication
- Cloud storage for saved results
- Advanced filtering and sorting options
- Hashtag analytics and insights
- Social media platform-specific optimizations
- Team collaboration features
