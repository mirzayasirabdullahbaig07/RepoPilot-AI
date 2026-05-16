# 🚀 Deploying RepoPilot AI to Netlify

This guide will help you deploy RepoPilot AI to Netlify in minutes.

## 📋 Prerequisites

- A [Netlify account](https://app.netlify.com/signup) (free)
- A [GitHub account](https://github.com/signup) (if deploying via Git)
- Your Groq API key

## 🎯 Deployment Methods

### Method 1: Deploy via GitHub (Recommended)

This method enables automatic deployments when you push changes.

#### Step 1: Push to GitHub

```bash
# Initialize git repository (if not already done)
git init

# Add all files
git add .

# Commit
git commit -m "Initial commit - RepoPilot AI"

# Add your GitHub repository as remote
git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPO_NAME.git

# Push to GitHub
git branch -M main
git push -u origin main
```

#### Step 2: Connect to Netlify

1. Go to [Netlify](https://app.netlify.com)
2. Click **"Add new site"** → **"Import an existing project"**
3. Choose **"Deploy with GitHub"**
4. Authorize Netlify to access your GitHub account
5. Select your repository
6. Configure build settings:
   - **Build command**: Leave empty (no build needed)
   - **Publish directory**: `.` (current directory)
7. Click **"Deploy site"**

#### Step 3: Configure Environment (Optional)

If you want to use environment variables instead of hardcoding the API key:

1. Go to **Site settings** → **Environment variables**
2. Add variable: `GROQ_API_KEY` with your key
3. Update `index.html` to read from environment (requires build step)

### Method 2: Deploy via Netlify CLI

Quick deployment from your local machine.

#### Step 1: Install Netlify CLI

```bash
npm install -g netlify-cli
```

#### Step 2: Login to Netlify

```bash
netlify login
```

#### Step 3: Deploy

```bash
# Deploy to a draft URL for testing
netlify deploy

# When ready, deploy to production
netlify deploy --prod
```

### Method 3: Drag & Drop Deploy

Fastest method for quick testing.

1. Go to [Netlify Drop](https://app.netlify.com/drop)
2. Drag and drop your project folder
3. Your site will be live in seconds!

**Note**: This method doesn't support automatic updates. You'll need to manually redeploy for changes.

## ⚙️ Post-Deployment Configuration

### 1. Custom Domain (Optional)

1. Go to **Site settings** → **Domain management**
2. Click **"Add custom domain"**
3. Follow the instructions to configure DNS

### 2. HTTPS

Netlify automatically provisions SSL certificates. Your site will be available via HTTPS within minutes.

### 3. Configure API Key

**Important**: Make sure to configure your Groq API key!

**Option A**: Edit `index.html` before deployment
- Find line 438: `const GROQ_API_KEY = 'PASTE_YOUR_GROQ_KEY_HERE';`
- Replace with your actual key
- Commit and push changes

**Option B**: Users enter key in browser
- Users can paste their API key in the app
- It will be saved in localStorage

### 4. Environment Variables (Advanced)

For better security, you can use Netlify Functions to proxy API calls:

1. Create a `netlify/functions` directory
2. Add a serverless function to handle Groq API calls
3. Store API key in Netlify environment variables
4. Update frontend to call your function instead of Groq directly

## 🔧 Configuration Files

Your project includes these Netlify configuration files:

- **`netlify.toml`**: Main configuration with headers and redirects
- **`_redirects`**: Fallback routing rules
- **`.gitignore`**: Files to exclude from Git

## 📊 Monitoring & Analytics

### Enable Netlify Analytics

1. Go to **Site settings** → **Analytics**
2. Enable analytics (paid feature)
3. View traffic, performance, and more

### Check Deploy Logs

1. Go to **Deploys** tab
2. Click on any deploy to see logs
3. Debug any issues

## 🐛 Troubleshooting

### Issue: Site shows 404 error

**Solution**: Check that `_redirects` file is present and contains:
```
/*    /index.html   200
```

### Issue: API calls fail

**Solution**: 
- Verify Groq API key is correct
- Check browser console for CORS errors
- Ensure API key has proper permissions

### Issue: Styles not loading

**Solution**:
- Clear browser cache
- Check that `index.html` is in the root directory
- Verify publish directory is set to `.` in Netlify

### Issue: Deploy fails

**Solution**:
- Check deploy logs in Netlify dashboard
- Ensure all files are committed to Git
- Verify `netlify.toml` syntax is correct

## 🔄 Continuous Deployment

Once connected to GitHub, Netlify will automatically:
- Deploy when you push to `main` branch
- Create preview deployments for pull requests
- Run deploy previews for branches

### Deploy Contexts

Configure different settings for different contexts in `netlify.toml`:

```toml
[context.production]
  # Production-specific settings

[context.deploy-preview]
  # Preview-specific settings

[context.branch-deploy]
  # Branch-specific settings
```

## 🎉 Success!

Your RepoPilot AI is now live on Netlify! 

**Next Steps**:
1. Share your site URL
2. Test all features
3. Monitor performance
4. Gather user feedback

## 📚 Additional Resources

- [Netlify Documentation](https://docs.netlify.com/)
- [Netlify CLI Documentation](https://cli.netlify.com/)
- [Netlify Community Forum](https://answers.netlify.com/)
- [Netlify Status](https://www.netlifystatus.com/)

## 💡 Tips

- Use **Deploy Previews** to test changes before going live
- Enable **Branch Deploys** for feature testing
- Set up **Build Hooks** for automated deployments
- Use **Split Testing** to A/B test features
- Configure **Form Handling** if you add contact forms

---

**Need Help?** Check the [Netlify Support](https://www.netlify.com/support/) or open an issue on GitHub.