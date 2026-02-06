# Char-Chat
# TBD – Interactive Program Review Site 🌌

A web app for submitting program reviews with emoji ratings and optional comments, featuring a dynamic animated space background. Admins can log in to view all submitted reviews.  

---

## Features

- **Animated Space Background:** Stars, spinning planets, pulsing nebulas, and a moving black hole.  
- **Review Form:**  
  - Program Name (required)  
  - Ratings for: Design, Functionality, Character Response, Overall Feel (all required)  
  - Comment (optional)  
- **Emoji Ratings:** 😐, 🤔, 😊, 😍, 🤩  
- **Admin Dashboard:**  
  - Only visible to logged-in admins  
  - Displays all submitted reviews with timestamps  
- **Authentication:** Email/password login powered by Supabase (no Google account required).  

---

## Setup Instructions

### 1. Supabase Configuration
1. Go to [Supabase](https://supabase.com/) and create a free account using GitHub.  
2. Create a new project.  
3. Enable **Email/Password Authentication** in **Authentication → Sign In / Providers → Email**.  
4. Create an admin user in **Authentication → Users** with your chosen email/password.  
5. Create a database table called `reviews` with the following columns:
   - `id` → UUID, primary key  
   - `program_name` → text  
   - `ratings` → jsonb  
   - `comment` → text (optional)  
   - `created_at` → timestamp, default `now()`  

6. Copy your **Supabase URL** and **anon/public API key**; you’ll need them in `index.html`.

---

### 2. GitHub Pages Deployment
1. Create a GitHub repository.  
2. Add your `index.html` file (with Supabase credentials replaced).  
3. Go to **Settings → Pages**:  
   - Source: `main` branch, `/ (root)` folder  
   - Save → GitHub will provide your site URL.  

---

### 3. Admin Login
- Click the **Admin Login** button on the top-right.  
- Enter the email/password you created in Supabase.  
- Once logged in, the **review dashboard** appears.  

---

### 4. Submitting Reviews
- All rating categories are **required**.  
- Comment is optional.  
- Clicking **Submit Review** stores the review in Supabase.  
- Admins can see all reviews instantly in the dashboard.  

---

### 5. Notes
- The site is **fully static**, no server required.  
- Animated background is optimized for performance on desktops and mobile devices.  
- Supabase handles authentication and database; no Google login is required for the admin.  

---

### 6. Recommended Additions
- **.gitignore:** Exclude `.env`, `node_modules/`, and any sensitive local files.  
- **LICENSE:** Use MIT if you want to allow open-source sharing.  

---

Enjoy your cosmic review site! 🌠
