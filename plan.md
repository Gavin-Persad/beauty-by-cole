# 🚀 Project Setup Plan

## 1. Set Up Repository ✅

- Create a new repository on GitHub for your project. ✅

## 2. Initialize Project ✅

- Set up a new React project using Vercel with TypeScript and Tailwind CSS. ✅

## 3. Hello World Setup ✅

- Clean up boilerplate code. ✅
- Create a simple “Hello World” page to confirm everything is working. ✅

## 4. Add Husky for Git Hooks

- Install Husky to manage Git hooks.
- Set up a pre-commit hook to ensure linting and build checks before committing.

---

## 🔐 Authentication & Admin Access

### 5. Basic Auth Options

#### Option A: Use Auth0 / Clerk / Firebase Auth

- Easy integration with React.
- Handles login, signup, and session state.
- Firebase also offers built-in database & storage.

#### Option B: DIY JWT Auth

- Create a login form (email + password).
- Backend verifies and issues a JWT.
- Store token securely (preferably HTTP-only cookie).
- Use the token to protect upload & booking endpoints.

---

## 🌐 Integrate S3 Bucket

### 6. Create S3 Bucket

- Go to AWS S3 and create a new bucket (enable public access if needed for image serving).

### 7. Configure Permissions

- Set appropriate CORS and bucket policies.
- Upload a few test images.

### 8. Link to React App

- Use pre-signed URLs or public URLs to fetch and display images.

### 9. Test Connectivity

- Ensure the app can successfully load images from the bucket.

---

## 🎨 Build Features

### 10. Landing Page

- Design and develop your landing page.
- Add a prominent "Book Now" call-to-action.

### 11. Booking System

- Plan key features (calendar, time slots, form, etc.).
- Implement a dynamic multi-step form with smooth transitions.

### 12. Review Feature

- Collect user reviews after a booking.
- Display selected reviews in a carousel or scrolling box on the landing page.

---

## 🗃️ Managing Gallery Uploads

- Only authenticated users can upload.
- Use pre-signed S3 URLs to securely manage uploads.

---

## 📆 Bookings Dashboard

- Create a secure `/dashboard` route.
- Display bookings, contact info, and admin actions.
- Only accessible after login.

---

## ✅ Bonus Tips

- Use role-based access (only "host" can upload/manage).
- Keep sessions short, store tokens securely (cookies > localStorage).
- Consider basic logging of changes/actions for accountability.
