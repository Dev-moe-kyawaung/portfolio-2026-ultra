```markdown
# 🚀 Deployment Guide

## Quick Deploy Options

### 1. GitHub Pages (Recommended)

```bash
# Initialize Git
git init
git add .
git commit -m "Initial commit"
git branch -M main

# Add remote (replace with your repo)
git remote add origin https://github.com/Dev-moe-kyawaung/portfolio.git

# Push to GitHub
git push -u origin main

# Enable GitHub Pages in repo settings
# Settings → Pages → Source: main branch → Save
```

**URL:** https://moekyawaung.github.io/

### 2. GitLab Pages

```bash
# Add GitLab remote
git remote add gitlab https://gitlab.com/moekyawaung/portfolio.git
git push gitlab main

# GitLab automatically deploys from .gitlab-ci.yml
```

**URL:** https://moekyawaung.gitlab.io/

### 3. Cloudflare Pages

```bash
# Install Wrangler CLI
npm install -g wrangler

# Login to Cloudflare
wrangler login

# Deploy
wrangler pages deploy .
```

**URL:** https://moekyawaung.pages.dev/

### 4. Netlify

```bash
# Install Netlify CLI
npm install -g netlify-cli

# Login
netlify login

# Deploy
netlify deploy --prod
```

**URL:** https://moekyawaung-portfolio.netlify.app/

### 5. Vercel

```bash
# Install Vercel CLI
npm install -g vercel

# Login
vercel login

# Deploy
vercel --prod
```

**URL:** https://moekyawaung-portfolio.vercel.app/

### 6. Codeberg Pages

```bash
# Add Codeberg remote
git remote add codeberg https://codeberg.org/moekyawaung/portfolio.git
git push codeberg main

# Enable Pages in Codeberg repo settings
```

**URL:** https://moekyawaung.codeberg.page/

### 7. Bitbucket Pages

```bash
# Add Bitbucket remote
git remote add bitbucket https://bitbucket.org/moekyawaung/portfolio.git
git push bitbucket main

# Enable Pages in Bitbucket repo settings
```

**URL:** https://bitbucket.org/moekyawaung/portfolio/pages/

## SEO Submission

### Google Search Console

1. Go to https://search.google.com/search-console
2. Add property: https://moekyawaung.github.io/
3. Verify ownership (add HTML tag to index.html)
4. Submit sitemap: https://moekyawaung.github.io/sitemap.xml
5. Request indexing

### Microsoft Bing Webmaster

1. Go to https://www.bing.com/webmasters
2. Add your site
3. Verify ownership
4. Submit sitemap
5. Request indexing

### Yandex Webmaster

1. Go to https://webmaster.yandex.com/
2. Add site
3. Verify
4. Submit sitemap

### Baidu Webmaster

1. Go to https://ziyuan.baidu.com/
2. Add site
3. Verify (requires Chinese phone number)
4. Submit sitemap

## Performance Optimization

### Lighthouse Score

Run Lighthouse audit:

```bash
npm install -g lighthouse
lighthouse https://moekyawaung.github.io/ --view
```


### Image Optimization

```bash
# Install ImageMagick
# Optimize all images
for img in assets/images/*.{jpg,png}; do
    convert "$img" -quality 85 "assets/images/optimized/$(basename "$img")"
done
```


### CSS/JS Minification

```bash
# Install minifiers
npm install -g clean-css-cli uglify-js

# Minify CSS
cleancss -o css/main.min.css css/main.css

# Minify JS
uglifyjs js/main.js -o js/main.min.js
```


## Monitoring

### Uptime Monitoring

- **Uptime Robot:** https://uptimerobot.com/
- **Pingdom:** https://www.pingdom.com/
- **StatusCake:** https://www.statuscake.com/


### Analytics

- **Google Analytics:** Add GA4 tracking code to all pages
- **Microsoft Clarity:** Add Clarity tracking code
- **Cloudflare Analytics:** Enable in Cloudflare dashboard


## SSL Certificate

All platforms provide free SSL:

- GitHub Pages: Automatic HTTPS
- GitLab Pages: Automatic HTTPS
- Cloudflare: Automatic SSL
- Netlify: Automatic SSL
- Vercel: Automatic SSL


## Custom Domain

### Setup Custom Domain

1. Buy domain (Namecheap, GoDaddy, etc.)
2. Add DNS records:

```
Type: A
Name: @
Value: 185.199.108.153 (GitHub Pages)

Type: CNAME
Name: www
Value: moekyawaung.github.io
```

3. Add custom domain in hosting platform settings

## Troubleshooting

### 404 Errors

- Check file paths are correct
- Ensure files are in repository
- Clear cache and redeploy


### Build Failures

- Check .gitignore doesn't exclude needed files
- Verify package.json scripts
- Check CI/CD configuration files


### Slow Performance

- Optimize images
- Enable caching
- Use CDN (Cloudflare)
- Minify CSS/JS


## Support

Contact: moekyawaung@programmer.net
GitHub Issues: https://github.com/Dev-moe-kyawaung/portfolio/issues

---

**Good luck with your deployment! 🎉**

```
