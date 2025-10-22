# Active Commerce Website Backend Setup

This backend handles form submissions from your "Get Admission Now" popup and sends the information to your email.

## Setup Instructions

### 1. Install Node.js
- Download and install Node.js from https://nodejs.org/
- Choose the LTS version

### 2. Install Dependencies
Open Command Prompt in the **backend** folder and run:
```bash
cd backend
npm install
```

### 3. Configure Email Settings
Edit `backend/server.js` and replace the following:

```javascript
// Replace these with your actual email credentials
user: 'your-email@gmail.com',     // Your Gmail address
pass: 'your-app-password'         // Your Gmail App Password (not regular password)
```

And also replace the recipient email:
```javascript
to: 'your-email@gmail.com',       // Email where you want to receive form submissions
```

### 4. Gmail App Password Setup
1. Go to your Google Account settings
2. Enable 2-Factor Authentication
3. Go to "App passwords" section
4. Generate a new app password for "Mail"
5. Use this 16-character password in the server.js file

### 5. Start the Server
From the backend folder:
```bash
cd backend
npm start
```

Your website will be available at: http://localhost:3000

## How It Works

1. When someone fills the "Get Admission Now" popup form
2. The form data is sent to your backend server
3. The server sends an email to your specified email address
4. You receive the student's information instantly

## Email Format
You'll receive emails with:
- Student Name
- Phone Number  
- Class/Course Interest
- Submission Timestamp

## Files Created
- `backend/server.js` - Main backend server
- `backend/package.json` - Dependencies configuration
- `README.md` - This setup guide

## Troubleshooting
- Make sure Node.js is installed
- Check that your Gmail app password is correct
- Ensure your firewall allows the application
- Check the console for any error messages

## Production Deployment
For live deployment, consider using:
- Heroku (free tier available)
- Vercel
- Railway
- DigitalOcean

Contact support if you need help with deployment!