# Vercel Deployment Guide for MyAiPlug Studio

This guide explains how to deploy MyAiPlug Studio to Vercel.

## Prerequisites

- A [Vercel account](https://vercel.com/signup)
- GitHub repository connected to Vercel

## Deployment Options

### Option 1: Deploy via Vercel Dashboard

1. Go to [Vercel Dashboard](https://vercel.com/dashboard)
2. Click "Add New..." → "Project"
3. Import your GitHub repository
4. Vercel will automatically detect the configuration from `vercel.json`
5. Click "Deploy"

### Option 2: Deploy via Vercel CLI

1. Install Vercel CLI:
   ```bash
   npm install -g vercel
   ```

2. Login to Vercel:
   ```bash
   vercel login
   ```

3. Deploy from the root directory:
   ```bash
   vercel
   ```

4. For production deployment:
   ```bash
   vercel --prod
   ```

## Configuration

The `vercel.json` file includes:

- **Build Command**: `npm run build` - Builds all packages using Turbo
- **Output Directory**: `packages/app/studio/dist` - The built studio app
- **Node Version**: 20 - Compatible Node.js version
- **Headers**: Cross-Origin Isolation headers required for the app to function
- **Routing**: SPA routing that falls back to `index.html`

## Important Notes

1. **Node Version**: The project requires Node.js 20 or higher. Vercel will use Node 20 as specified in the configuration.

2. **Build Time**: The first build may take 2-3 minutes as it needs to build all packages in the monorepo.

3. **Environment Variables**: If you need to add environment variables, do so in the Vercel Dashboard under "Settings" → "Environment Variables".

4. **Cross-Origin Headers**: The app requires specific security headers to work properly. These are configured in `vercel.json`.

## Troubleshooting

### Build Fails

If the build fails, check:
- Node version compatibility
- All dependencies are properly installed
- Build logs in Vercel Dashboard for specific errors

### App Doesn't Load

If the deployed app doesn't load:
- Check browser console for CORS or header-related errors
- Verify that Cross-Origin headers are properly set
- Ensure all static assets are being served correctly

### 404 Errors on Routes

If you get 404 errors when navigating:
- Verify the rewrite rules in `vercel.json` are working
- Check that the SPA routing is properly configured

## Custom Domain

To add a custom domain:
1. Go to your project in Vercel Dashboard
2. Navigate to "Settings" → "Domains"
3. Add your domain and follow the DNS configuration instructions

## Support

For issues specific to:
- **Vercel deployment**: Check [Vercel Documentation](https://vercel.com/docs)
- **MyAiPlug Studio**: Open an issue in this repository
