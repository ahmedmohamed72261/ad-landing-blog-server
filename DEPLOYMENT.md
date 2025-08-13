# Vercel Deployment Guide

## 🚀 Your Blog Server is Ready for Vercel Deployment!

### Files Added/Modified:
- ✅ `vercel.json` - Vercel configuration file
- ✅ `index.js` - Renamed from server.js (Vercel entry point)
- ✅ `package.json` - Updated scripts and main entry point
- ✅ Added deployment success messages

### Deployment Steps:

1. **Install Vercel CLI** (if not already installed):
   ```bash
   npm install -g vercel
   ```

2. **Deploy to Vercel**:
   ```bash
   vercel
   ```

3. **Set Environment Variables** in Vercel Dashboard:
   - `MONGODB_URI` - Your MongoDB connection string
   - `JWT_SECRET` - Your JWT secret key
   - `CLIENT_URL` - Your frontend URL
   - `NODE_ENV` - Set to "production"

### Environment Variables Required:
- `MONGODB_URI` - MongoDB Atlas connection string
- `JWT_SECRET` - Secret key for JWT tokens
- `CLIENT_URL` - Frontend application URL
- `CLOUDINARY_CLOUD_NAME` - (if using Cloudinary)
- `CLOUDINARY_API_KEY` - (if using Cloudinary)
- `CLOUDINARY_API_SECRET` - (if using Cloudinary)

### After Deployment:
- Visit your Vercel URL to see the welcome message
- Test the health endpoint: `your-vercel-url/api/health`
- Your API endpoints will be available at: `your-vercel-url/api/`

### Success Messages:
When deployed successfully, you'll see:
- 🎉 Welcome message at the root URL
- 🚀 Health check with deployment status
- ✅ MongoDB connection confirmation in logs

### Troubleshooting:
- Ensure all environment variables are set in Vercel dashboard
- Check Vercel function logs for any errors
- Verify MongoDB Atlas allows connections from anywhere (0.0.0.0/0)