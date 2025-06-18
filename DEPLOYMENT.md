# 🚀 Vercel Deployment Guide

This guide walks you through deploying the Geographic Routing Performance Testing Tool to Vercel.

## 📦 Project Structure

Your project should have these files:
```
network-latency-tester/
├── index.html          # Main tool interface
├── docs.html           # Documentation page
├── package.json        # Project configuration
├── vercel.json         # Vercel deployment config
├── README.md           # Project documentation
└── DEPLOYMENT.md       # This deployment guide
```

## 🔧 Deployment Options

### Option 1: Direct GitHub Deployment (Recommended)

1. **Create a GitHub Repository**
   ```bash
   # Create a new repository on GitHub
   # Then clone it locally
   git clone https://github.com/ces0491/network-latency-tester.git
   cd network-latency-tester
   ```

2. **Add the Project Files**
   - Copy all the files (`index.html`, `docs.html`, `package.json`, `vercel.json`, `README.md`)
   - Commit and push to GitHub:
   ```bash
   git add .
   git commit -m "Initial commit: Geographic Routing Performance Testing Tool"
   git push origin main
   ```

3. **Deploy to Vercel**
   - Go to [vercel.com](https://vercel.com)
   - Sign in with your GitHub account
   - Click "New Project"
   - Import your GitHub repository
   - Vercel will automatically detect it's a static site
   - Click "Deploy"

### Option 2: Vercel CLI Deployment

1. **Install Vercel CLI**
   ```bash
   npm i -g vercel
   ```

2. **Login to Vercel**
   ```bash
   vercel login
   ```

3. **Deploy from Project Directory**
   ```bash
   # Navigate to your project directory
   cd network-latency-tester
   
   # Deploy
   vercel
   
   # Follow the prompts:
   # - Set up and deploy? Y
   # - Which scope? (your account)
   # - Link to existing project? N
   # - Project name? network-latency-tester
   # - Directory? ./
   ```

### Option 3: Drag and Drop Deployment

1. **Prepare Files**
   - Create a folder with all your project files
   - Ensure `index.html` is in the root

2. **Deploy via Vercel Dashboard**
   - Go to [vercel.com/new](https://vercel.com/new)
   - Drag and drop your project folder
   - Vercel will automatically deploy

## 🌐 Custom Domain Setup (Optional)

1. **Purchase/Configure Domain**
   - Buy a domain from your preferred registrar
   - Or use a subdomain of an existing domain

2. **Add Domain in Vercel**
   - Go to your project dashboard
   - Click "Domains"
   - Add your custom domain
   - Follow DNS configuration instructions

3. **Example DNS Setup**
   ```
   Type: CNAME
   Name: routing-tool (or @)
   Value: cname.vercel-dns.com
   ```

## 🔍 Environment Variables (If Needed)

If you need to add environment variables:

1. **In Vercel Dashboard**
   - Go to Project → Settings → Environment Variables
   - Add key-value pairs

2. **Via Vercel CLI**
   ```bash
   vercel env add VARIABLE_NAME
   # Enter the value when prompted
   ```

## 📊 Analytics and Monitoring

### Enable Vercel Analytics
1. Go to your project dashboard
2. Click "Analytics" tab
3. Enable Web Analytics
4. Analytics will be automatically added to your site

### Performance Monitoring
- Vercel provides automatic performance monitoring
- Check the "Functions" and "Analytics" tabs for insights
- Monitor Core Web Vitals and loading performance

## 🔧 Custom Build Commands (If Needed)

For this static site, no build commands are needed. However, if you want to add build steps:

```json
{
  "scripts": {
    "build": "echo 'Static site - no build needed'",
    "dev": "npx serve .",
    "start": "npx serve ."
  }
}
```

## 🚨 Troubleshooting

### Common Issues

1. **404 Errors**
   - Ensure `index.html` is in the root directory
   - Verify file names match exactly

2. **CORS Issues**
   - This is expected for some endpoints
   - The tool handles CORS gracefully
   - Users can use alternative endpoints

3. **Performance Issues**
   - Enable Vercel Analytics to monitor
   - Check browser console for errors
   - Verify network connectivity

### Debugging

1. **Check Deployment Logs**
   ```bash
   vercel logs
   ```

2. **Local Testing**
   ```bash
   npx serve .
   # Open http://localhost:3000
   ```

3. **Vercel Dev Server**
   ```bash
   vercel dev
   ```

## 🎯 Post-Deployment Checklist

- [ ] Tool loads correctly at your domain
- [ ] Documentation page is accessible at `/docs`
- [ ] All preset scenarios work properly
- [ ] Export functionality works
- [ ] Mobile responsiveness is good
- [ ] Test with actual routing endpoints
- [ ] Share with your team for feedback

## 🔄 Updates and Maintenance

### Updating the Deployment

1. **Via GitHub (Automatic)**
   - Push changes to your GitHub repository
   - Vercel automatically redeploys

2. **Via CLI**
   ```bash
   # From your project directory
   vercel --prod
   ```

### Monitoring
- Check Vercel dashboard regularly
- Monitor analytics for usage patterns
- Update endpoints based on user feedback

## 🎉 Success!

Your Geographic Routing Performance Testing Tool should now be live at:
- **Main Tool**: `https://network-latency-tester-jo9sk9am6-cesaires-projects.vercel.app/`
- **Documentation**: `https://network-latency-tester-jo9sk9am6-cesaires-projects.vercel.app/docs`

## 📞 Support

If you encounter issues:
- Check the [Vercel Documentation](https://vercel.com/docs)
- Review the project [README](README.md)