# Deployment Guide

## Quick Deployment Options

### Option 1: GitHub Pages (Free & Easy)

1. **Create a GitHub Repository**
   - Go to github.com and create a new repository
   - Name it: `your-username.github.io` (for main site) or any name

2. **Upload Your Files**
   ```bash
   git init
   git add .
   git commit -m "Initial portfolio commit"
   git branch -M main
   git remote add origin https://github.com/your-username/your-repo.git
   git push -u origin main
   ```

3. **Enable GitHub Pages**
   - Go to repository Settings > Pages
   - Select branch: `main`
   - Select folder: `/ (root)`
   - Click Save

4. **Access Your Site**
   - Your site will be live at: `https://your-username.github.io/repo-name/`

---

### Option 2: Netlify (Free with Custom Domain)

1. **Sign Up**: Go to netlify.com and sign up
2. **Drag & Drop**: Simply drag your project folder to Netlify
3. **Deploy**: Netlify will automatically deploy your site
4. **Custom Domain** (optional): Add your own domain in site settings

**OR use Netlify CLI:**
```bash
npm install -g netlify-cli
netlify deploy
```

---

### Option 3: Vercel (Free & Fast)

1. **Sign Up**: Go to vercel.com
2. **Import Project**: Click "New Project"
3. **Deploy**: Connect your GitHub repo or upload files
4. **Done**: Your site is live instantly

---

### Option 4: Traditional Web Hosting

1. **Get Hosting**: Purchase hosting from providers like:
   - Hostinger
   - Bluehost
   - SiteGround
   - GoDaddy

2. **Upload via FTP**:
   - Use FileZilla or any FTP client
   - Upload all files to `public_html` or `www` folder

3. **Access**: Your site will be live at your domain

---

## Before Deployment Checklist

- [ ] Test all links work correctly
- [ ] Check mobile responsiveness
- [ ] Optimize images (compress for faster loading)
- [ ] Update meta tags (title, description)
- [ ] Test contact form (if added)
- [ ] Add favicon.ico
- [ ] Check browser compatibility
- [ ] Add Google Analytics (optional)

---

## Performance Optimization

1. **Compress Images**
   - Use TinyPNG or ImageOptim
   - Convert to WebP format

2. **Minify CSS/JS**
   - Use online tools or build tools

3. **Enable Caching**
   - Add .htaccess rules for Apache servers

4. **Use CDN**
   - Load Google Fonts via CDN
   - Consider Cloudflare for static assets

---

## Custom Domain Setup

### For GitHub Pages:
1. Buy domain from Namecheap/GoDaddy
2. Add CNAME file with your domain
3. Update DNS records:
   - Type: A
   - Value: 185.199.108.153 (GitHub IP)

### For Netlify/Vercel:
- Follow their custom domain setup wizard
- Update nameservers or add DNS records

---

## Continuous Deployment (Advanced)

**GitHub Pages**: Auto-deploys on push to main branch

**Netlify/Vercel**: 
- Connect your GitHub repo
- Auto-deploy on every commit
- Preview deployments for pull requests

---

## Support

For deployment issues:
- GitHub Pages: docs.github.com/pages
- Netlify: docs.netlify.com
- Vercel: vercel.com/docs
