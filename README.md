# URL Shortener

A full-stack URL shortener web application built with React, Tailwind CSS, Supabase, and Shadcn UI.

## Features
- *User Authentication*: Sign up, log in, and log out securely with Supabase Auth.
- *Shorten URLs*: Create short links for any long URL.
- *Custom Aliases*: Optionally set a custom alias for your short URL.
- *QR Code Generation*: Automatically generate and store a QR code for each short URL.
- *User Dashboard*: View, search, and manage all your shortened links in a personalized dashboard.
- *Click Analytics*: Track device type, city, and country for each link click.
- *Profile Pictures*: Upload and display user avatars, stored securely in Supabase Storage.
- *Responsive UI*: Modern, mobile-friendly interface using Tailwind CSS and Shadcn UI components.

## Getting Started

### 1. Clone the Repository
bash
git clone <your-repo-url>
cd url-shortener


### 2. Install Dependencies
bash
yarn install
# or
npm install


### 3. Set Up Environment Variables
Create a .env file in the project root with the following:

VITE_SUPABASE_URL=your-supabase-url
VITE_SUPABASE_KEY=your-supabase-anon-key


### 4. Supabase Setup
- Create a [Supabase](https://supabase.com/) project.
- Enable *Authentication* (email/password).
- Create two *Storage Buckets*:
  - profile-pic (for user avatars)
  - qrs (for QR code images)
- Set appropriate *Row Level Security (RLS) policies* for uploads and public read access.
- Create the following *tables*:
  - urls (for storing user links)
  - clicks (for analytics)

### 5. Run the App
bash
yarn dev
# or
npm run dev


## Folder Structure
- src/ — Main source code
  - components/ — UI and feature components
  - db/ — Supabase API logic
  - hooks/ — Custom React hooks
  - pages/ — Route pages (dashboard, auth, landing, etc.)
  - layouts/ — Layout components
  - lib/ — Utility functions
