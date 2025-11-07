# REACH UHC Website

A modern, responsive website for REACH UHC (Universal Health Coverage) built with HTML, CSS, and JavaScript. This is a temporary static site hosted on GitHub Pages.

## Features

- 🎨 Modern, clean design inspired by sormas.org
- 📱 Fully responsive (mobile, tablet, desktop)
- ⚡ Fast loading static site
- 🎯 Smooth scrolling navigation
- 📰 Latest news section
- 📊 Impact statistics
- 📧 Newsletter subscription form
- 🔍 SEO-friendly structure

## Project Structure

```
reach-uhc.org/
├── index.html          # Main HTML file
├── css/
│   └── style.css      # Stylesheet
├── js/
│   └── main.js        # JavaScript for interactivity
└── README.md          # This file
```

## Setup Instructions for GitHub Pages

### Step 1: Initialize Git Repository

If you haven't already, initialize a git repository in this directory:

```bash
git init
git add .
git commit -m "Initial commit: REACH UHC website"
```

### Step 2: Create GitHub Repository

1. Go to [GitHub](https://github.com) and sign in
2. Click the "+" icon in the top right corner
3. Select "New repository"
4. Name it `reach-uhc.org` (or any name you prefer)
5. **Do NOT** initialize with README, .gitignore, or license (since we already have files)
6. Click "Create repository"

### Step 3: Push to GitHub

```bash
# Add your GitHub repository as remote (replace YOUR_USERNAME with your GitHub username)
git remote add origin https://github.com/YOUR_USERNAME/reach-uhc.org.git

# Push to GitHub
git branch -M main
git push -u origin main
```

### Step 4: Enable GitHub Pages

1. Go to your repository on GitHub
2. Click on "Settings" tab
3. Scroll down to "Pages" in the left sidebar
4. Under "Source", select "Deploy from a branch"
5. Choose "main" branch and "/ (root)" folder
6. Click "Save"
7. Your site will be available at: `https://YOUR_USERNAME.github.io/reach-uhc.org/`

### Step 5: Configure Custom Domain (reach-uhc.org)

1. In the same GitHub Pages settings, scroll to "Custom domain"
2. Enter `reach-uhc.org` (and optionally `www.reach-uhc.org`)
3. Click "Save"

### Step 6: Configure DNS at Namecheap

1. Log in to your Namecheap account
2. Go to Domain List and click "Manage" next to reach-uhc.org
3. Go to "Advanced DNS" tab
4. Add the following DNS records:

   **For apex domain (reach-uhc.org):**
   - Type: `A Record`
   - Host: `@`
   - Value: `185.199.108.153`
   - TTL: Automatic
   
   - Type: `A Record`
   - Host: `@`
   - Value: `185.199.109.153`
   - TTL: Automatic
   
   - Type: `A Record`
   - Host: `@`
   - Value: `185.199.110.153`
   - TTL: Automatic
   
   - Type: `A Record`
   - Host: `@`
   - Value: `185.199.111.153`
   - TTL: Automatic

   **For www subdomain (www.reach-uhc.org):**
   - Type: `CNAME Record`
   - Host: `www`
   - Value: `YOUR_USERNAME.github.io`
   - TTL: Automatic

   > **Note:** Replace `YOUR_USERNAME` with your actual GitHub username

5. Save the changes
6. Wait 5-30 minutes for DNS propagation

### Step 7: Verify SSL Certificate

GitHub Pages will automatically provision an SSL certificate for your custom domain. This usually takes a few minutes to a few hours. You can check the status in the GitHub Pages settings.

## Local Development

To view the website locally:

1. Simply open `index.html` in your web browser, or
2. Use a local server:

```bash
# Using Python 3
python3 -m http.server 8000

# Using Node.js (if you have http-server installed)
npx http-server

# Using PHP
php -S localhost:8000
```

Then visit `http://localhost:8000` in your browser.

## Customization

### Colors

Edit the CSS variables in `css/style.css`:

```css
:root {
    --primary-color: #0066cc;
    --primary-dark: #0052a3;
    --secondary-color: #00a86b;
    /* ... */
}
```

### Content

- Edit `index.html` to update text, links, and structure
- Modify `css/style.css` to change styling
- Update `js/main.js` to add or modify functionality

## Future Migration

When you're ready to migrate to Drupal or WordPress:

1. Keep this static site as a reference for design and content
2. Export content structure and copy
3. Set up your CMS of choice
4. Recreate the design using the CMS theme system
5. Import content
6. Update DNS to point to your new hosting

## Support

For issues or questions:
- Email: info@reach-uhc.org
- GitHub Issues: Create an issue in this repository

## License

© 2025 REACH UHC. All rights reserved.

