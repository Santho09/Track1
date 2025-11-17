# Environment Variables Setup

This document explains the environment variables needed for the backend.

## Required Environment Variables

### For Production Deployment

1. **JWT_SECRET** (Required)
   - A secure random string used to sign JWT tokens
   - Generate one using:
     ```bash
     node -e "console.log(require('crypto').randomBytes(32).toString('hex'))"
     ```
   - Or use an online generator: https://randomkeygen.com/

2. **FRONTEND_URL** (Required for production)
   - The URL of your frontend application
   - Example: `https://your-app.vercel.app`
   - Used for CORS configuration

3. **MONGO_URI** (Required)
   - Connection string for your MongoDB database (Atlas or self-hosted)
   - Example (MongoDB Atlas):
     ```env
     MONGO_URI=mongodb+srv://<username>:<password>@cluster0.xxxxx.mongodb.net/ecommerce_auth?retryWrites=true&w=majority
     ```
   - Example (local MongoDB):
     ```env
     MONGO_URI=mongodb://127.0.0.1:27017/ecommerce_auth
     ```

### Optional Environment Variables

4. **PORT** (Optional)
   - Server port number
   - Defaults to `3000` if not set
   - Most hosting platforms (Railway, Render, etc.) set this automatically

5. **NODE_ENV** (Optional)
   - Set to `production` for production deployments
   - Defaults to `development` if not set

## Setting Environment Variables

### Local Development

Create a `.env` file in the `backend/` directory:

```env
JWT_SECRET=your-secret-key-here
MONGO_URI=your-mongodb-connection-string-here
PORT=3000
NODE_ENV=development
FRONTEND_URL=http://localhost:8000
```

### Production Platforms

#### Railway
1. Go to your project settings
2. Click on "Variables" tab
3. Add each variable

#### Render
1. Go to your service settings
2. Click on "Environment" tab
3. Add each variable

#### Vercel
1. Go to project settings
2. Click on "Environment Variables"
3. Add each variable

#### VPS/Server
Create a `.env` file in the `backend/` directory or use system environment variables.

## Security Notes

- **Never commit `.env` files to Git** (already in `.gitignore`)
- Use different `JWT_SECRET` values for development and production
- Keep your `JWT_SECRET` secure and never share it publicly

