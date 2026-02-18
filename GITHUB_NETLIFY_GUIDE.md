# Deploy to GitHub & Netlify - Step by Step

This guide will get your L.A.B Rat Tattoos web app live on the internet in about 5 minutes.

## Step 1: Create a GitHub Repository

1. Go to [github.com](https://github.com)
2. Log in to your account
3. Click the **"+"** icon in the top right → **"New repository"**
4. Name it: `lab-rat-tattoos-web`
5. Description: `L.A.B Rat Tattoos stencil creator and loyalty rewards app`
6. Choose **"Public"** (so it's accessible)
7. Click **"Create repository"**

## Step 2: Get Your Repository URL

After creating the repo, you'll see a page with instructions. Look for:
```
https://github.com/YOUR-USERNAME/lab-rat-tattoos-web.git
```

Copy this URL - you'll need it in the next step.

## Step 3: Push Code to GitHub

I've already prepared your code locally. Now you need to push it to GitHub:

1. Open your terminal/command prompt
2. Navigate to the project folder:
   ```bash
   cd /home/ubuntu/lab-rat-tattoos-web
   ```

3. Add your GitHub repository as the remote:
   ```bash
   git remote add origin https://github.com/YOUR-USERNAME/lab-rat-tattoos-web.git
   ```
   (Replace `YOUR-USERNAME` with your actual GitHub username)

4. Push the code to GitHub:
   ```bash
   git branch -M main
   git push -u origin main
   ```

5. Enter your GitHub credentials when prompted

That's it! Your code is now on GitHub.

## Step 4: Deploy to Netlify

1. Go to [netlify.com](https://netlify.com)
2. Log in (or sign up if you don't have an account)
3. Click **"Add new site"** → **"Import an existing project"**
4. Choose **"GitHub"**
5. Authorize Netlify to access your GitHub account
6. Select the repository: `lab-rat-tattoos-web`
7. Click **"Deploy site"**

Netlify will automatically:
- Build your app
- Deploy it to a live URL
- Give you a link like `https://your-app-name.netlify.app`

## Step 5: Share Your Live App

Once deployed, you'll get a public URL. Share it with your customers!

They can now:
✅ Create stencils from images
✅ Sign up for the loyalty program
✅ Earn and redeem rewards in ZAR

## Optional: Custom Domain

To use your own domain (like `labrattatoos.com`):

1. In Netlify dashboard, go to **"Domain settings"**
2. Click **"Add custom domain"**
3. Enter your domain
4. Update your domain's DNS settings (Netlify will provide instructions)
5. Wait 24-48 hours for DNS to propagate

## Troubleshooting

### "Build failed" error
- Make sure you pushed all files to GitHub
- Check that `package.json` is in the root folder
- Netlify will show build logs - check them for errors

### "Page not found" after deployment
- Clear your browser cache
- Try in an incognito window
- Check the Netlify build logs

### Need to make changes
1. Edit files locally
2. Commit and push to GitHub:
   ```bash
   git add .
   git commit -m "Your change description"
   git push
   ```
3. Netlify automatically redeploys when you push!

---

**Questions?** Check Netlify docs at [docs.netlify.com](https://docs.netlify.com)
