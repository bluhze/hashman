# Supabase Authentication Setup Guide

## Prerequisites
1. A Supabase account (sign up at https://supabase.com)
2. A Supabase project created

## Setup Steps

### 1. Create a Supabase Project
1. Go to https://supabase.com and sign in
2. Click "New Project"
3. Fill in your project details:
   - Project name: `hashman` (or your preferred name)
   - Database password: (choose a strong password)
   - Region: (choose closest to your users)
4. Click "Create new project"
5. Wait for the project to be set up (takes 1-2 minutes)

### 2. Get Your Supabase Credentials
1. In your Supabase project dashboard, go to **Settings** (gear icon)
2. Click on **API** in the left sidebar
3. You'll find:
   - **Project URL**: Copy this (e.g., `https://xxxxx.supabase.co`)
   - **anon/public key**: Copy this key (starts with `eyJ...`)

### 3. Configure Hashman Application
1. Open `index.html` in your code editor
2. Find the Supabase configuration section (around line 2515):
   ```javascript
   const SUPABASE_URL = 'YOUR_SUPABASE_URL';
   const SUPABASE_ANON_KEY = 'YOUR_SUPABASE_ANON_KEY';
   ```
3. Replace the placeholders:
   ```javascript
   const SUPABASE_URL = 'https://xxxxx.supabase.co';
   const SUPABASE_ANON_KEY = 'eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9...';
   ```
4. Save the file

### 4. Configure Supabase Authentication Settings
1. In your Supabase dashboard, go to **Authentication** > **Settings**
2. Under **Site URL**, add your application URL:
   - For local development: `http://localhost:3000` or your local port
   - For production: `https://yourdomain.com`
3. Under **Redirect URLs**, add:
   - `http://localhost:3000/**` (for local development)
   - `https://yourdomain.com/**` (for production)
4. Save the settings

### 5. Optional: Configure Email Templates
1. Go to **Authentication** > **Email Templates**
2. Customize the email templates if desired:
   - Confirm signup
   - Reset password
   - Magic link
   - Change email address

### 6. Test the Integration
1. Open your application in a browser
2. Try signing up with a new account
3. Check your email for the confirmation email (if email confirmation is enabled)
4. Try logging in with your credentials

## Security Best Practices

### 1. Environment Variables (Recommended for Production)
For production, consider using environment variables instead of hardcoding credentials:

```javascript
const SUPABASE_URL = process.env.SUPABASE_URL || 'YOUR_SUPABASE_URL';
const SUPABASE_ANON_KEY = process.env.SUPABASE_ANON_KEY || 'YOUR_SUPABASE_ANON_KEY';
```

### 2. Row Level Security (RLS)
If you plan to store user data in Supabase tables, enable Row Level Security:
1. Go to **Authentication** > **Policies**
2. Create policies to restrict access to user data
3. Users should only access their own data

### 3. Email Confirmation
Consider enabling email confirmation:
1. Go to **Authentication** > **Settings**
2. Enable "Enable email confirmations"
3. Users will need to verify their email before logging in

## Troubleshooting

### Issue: "Authentication service not configured"
- **Solution**: Make sure you've replaced `YOUR_SUPABASE_URL` and `YOUR_SUPABASE_ANON_KEY` with your actual credentials

### Issue: "Invalid login credentials"
- **Solution**: 
  - Check that the email and password are correct
  - Verify that email confirmation is not required (or confirm your email)
  - Check Supabase dashboard for any error logs

### Issue: "User already registered"
- **Solution**: The email is already in use. Try logging in instead or use a different email

### Issue: CORS errors
- **Solution**: 
  - Add your domain to the allowed origins in Supabase settings
  - Check that your Site URL and Redirect URLs are configured correctly

## Next Steps

After setting up authentication, you can:
1. Store user-specific data in Supabase tables
2. Set up Row Level Security policies
3. Add social authentication (Google, GitHub, etc.)
4. Implement password reset functionality
5. Add email verification

## Additional Resources
- [Supabase Auth Documentation](https://supabase.com/docs/guides/auth)
- [Supabase JavaScript Client](https://supabase.com/docs/reference/javascript/introduction)
- [Supabase Security Best Practices](https://supabase.com/docs/guides/auth/row-level-security)

