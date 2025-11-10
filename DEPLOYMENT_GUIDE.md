# Deployment Guide

## 🚀 GitHub Repository Setup

### 1. Create GitHub Repository

1. Go to [GitHub.com](https://github.com)
2. Click the "+" icon in the top right corner
3. Select "New repository"
4. Name your repository (e.g., "sports-person-classifier")
5. Make it public (for free Vercel hosting)
6. Don't initialize with README (we already have one)
7. Click "Create repository"

### 2. Push Code to GitHub

After creating your repository, you'll see commands like these. Run them in your terminal:

```bash
# Add your GitHub repository as remote origin
git remote add origin https://github.com/YOUR_USERNAME/sports-person-classifier.git

# Push your code to GitHub
git branch -M main
git push -u origin main
```

Replace `YOUR_USERNAME` with your actual GitHub username.

## 🌐 Vercel Deployment

### Option 1: Vercel Dashboard (Recommended)

1. Go to [Vercel.com](https://vercel.com)
2. Sign up/login with your GitHub account
3. Click "New Project"
4. Import your GitHub repository
5. Vercel will auto-detect it's a Python Flask app
6. Click "Deploy"

### Option 2: Vercel CLI

1. **Install Vercel CLI**
   ```bash
   npm i -g vercel
   ```

2. **Deploy from terminal**
   ```bash
   vercel
   ```

3. **Follow the prompts:**
   - Link to your GitHub repository
   - Use default settings
   - Deploy

## 🔧 Configuration Notes

### Vercel Configuration
The `vercel.json` file is already configured for Python Flask deployment:

```json
{
  "version": 2,
  "builds": [
    {
      "src": "main.py",
      "use": "@vercel/python",
      "config": {
        "maxLambdaSize": "15mb"
      }
    }
  ],
  "routes": [
    {
      "src": "/(.*)",
      "dest": "main.py"
    }
  ]
}
```

### Environment Variables (if needed)
If you need to add environment variables:
1. Go to your Vercel dashboard
2. Select your project
3. Go to Settings > Environment Variables
4. Add any required variables

## 📋 Post-Deployment Checklist

- [ ] GitHub repository created
- [ ] Code pushed to GitHub
- [ ] Vercel project created
- [ ] Application deployed successfully
- [ ] Test the live application
- [ ] Update README with live URL
- [ ] Share your project! 🎉

## 🐛 Troubleshooting

### Common Issues

1. **Build fails**: Check Python version compatibility
2. **Model loading issues**: Ensure model files are in correct paths
3. **CORS errors**: Flask-CORS is already configured
4. **Large files**: Model files might need to be hosted elsewhere

### Getting Help

- Check Vercel deployment logs
- Review GitHub Actions (if enabled)
- Test locally first: `python main.py`

## 🎯 Success!

Once deployed, your Sports Person Classifier will be live on the internet! You can:
- Share the URL with friends
- Add it to your portfolio
- Continue improving the model
- Add more features

Happy coding! 🚀