# Security Notice

## ⚠️ CRITICAL: MongoDB Credentials Were Exposed

**If you saw a security alert from GitHub, your MongoDB credentials have been exposed in the git history.**

### Immediate Actions Required:

1. **Rotate MongoDB Credentials Immediately**
   - Log into your MongoDB Atlas account
   - Go to Database Access
   - Delete the user `harshit26092004`
   - Create a new user with a strong password
   - Update your local `.env` file with the new credentials

2. **Update Connection String**
   - Get the new connection string from MongoDB Atlas
   - Update `MEDTECHWEBAPP_ML_Final-main/health/server/.env` file (this file is NOT tracked by git)
   
3. **Check for Unauthorized Access**
   - Review your MongoDB Atlas logs for any suspicious activity
   - Check if any unauthorized databases or collections were created

### Why This Happened

The MongoDB connection string was hardcoded in `health/server/utils/db.js` instead of using environment variables. This has now been fixed.

### Current Security Measures

✅ Credentials moved to `.env` file (which is in `.gitignore`)  
✅ Example configuration provided in `.env.example`  
✅ Code updated to use `process.env.MONGODB_URI`

### Setup Instructions for Developers

1. Copy the example environment file:
   ```bash
   cd MEDTECHWEBAPP_ML_Final-main/health/server
   cp .env.example .env
   ```

2. Edit `.env` and add your MongoDB credentials:
   ```
   MONGODB_URI=mongodb+srv://your_username:your_password@cluster.mongodb.net/your_database
   ```

3. **NEVER commit the `.env` file to git!**

### Best Practices

- Always use environment variables for sensitive data
- Never hardcode credentials in source code
- Keep `.env` files in `.gitignore`
- Rotate credentials immediately if exposed
- Use different credentials for development and production

## Reporting Security Issues

If you discover a security vulnerability, please email the repository owner directly rather than opening a public issue.
