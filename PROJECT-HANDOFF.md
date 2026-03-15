# PROJECT HANDOFF - Zentra Web Design Auto Shop Template

## 🎯 Mission: Build Custom Websites for Auto Shops → Make Money

---

## 📁 Project Structure

### Main Directories:
- **Production Site:** `/Users/rasulabdullayev/clawd-webdesign/southwood-pitch/`
  - Live site for Southwood Automotive
  - Connected to GitHub: `zentra-web-design/southwood-automotive-pitch`
  - Live URL: https://zentra-web-design.github.io/southwood-automotive-pitch/

- **Template (Desktop):** `~/Desktop/auto-shop-template/`
  - Reusable template for new clients
  - Copy this for each new project
  - Includes README and generator script

---

## 🏢 Zentra Web Design Setup

### GitHub Organization:
- **Name:** `zentra-web-design`
- **Purpose:** Professional brand for all client sites
- **Account:** `rasulabdullayev510-create`
- **Authenticated:** GitHub CLI (`gh`) ready to use

### Branding Benefits:
- Clean professional URLs (no personal username)
- All client sites under one org
- Easy to manage and scale
- Professional appearance for pitches

---

## 🚀 Current Live Site - Southwood Automotive

### Site Details:
- **Business:** Southwood Automotive Ltd
- **Location:** 11029 Elbow Dr SW, Calgary, AB T2W 1G7
- **Phone:** (587) 352-9990
- **Google Rating:** 4.9★ (176+ reviews)
- **Live URL:** https://zentra-web-design.github.io/southwood-automotive-pitch/

### Pages Built:
1. **Home** - Hero, features, services preview, stats
2. **About** - Company story, values, team section
3. **Services** - 12 detailed services with pricing
4. **Pricing** - Transparent pricing tables + packages
5. **Testimonials** - 9 REAL Google reviews (extracted from Maps)

### Key Features:
✅ Modern gradient design
✅ Fully responsive (mobile/tablet/desktop)
✅ Real customer reviews from Google Maps
✅ Professional animations and transitions
✅ SEO-friendly HTML structure
✅ Fast loading, no dependencies

---

## 💰 Business Model

### Pricing Structure:
- **Website Setup:** $500
- **Monthly Maintenance:** $50/month
- **Custom Domain Setup:** Included (they buy domain ~$15/year)
- **Hosting:** FREE (GitHub Pages, unlimited bandwidth)

### Value Proposition:
- Professional 5-page website
- Real customer reviews integrated
- Free unlimited hosting (no Netlify bandwidth issues)
- Custom domain support
- Fast edits when clients need changes
- SSL/HTTPS included free

---

## 🔄 Workflow for New Clients

### When Mr. Rasul Says:
> "Take current template - [Business Name] - [Google Maps Link]"

### Agent Should:

1. **Extract Business Info from Google Maps:**
   ```
   - Business name
   - Address
   - Phone number
   - Google rating and review count
   - Extract 5-9 real customer reviews
   ```

2. **Generate Custom Site:**
   ```bash
   # Copy template
   cp -r ~/Desktop/auto-shop-template ~/clawd-webdesign/[client-slug]
   
   # Customize HTML files with:
   - Business name
   - Contact info
   - Real reviews
   - Custom services/pricing if provided
   ```

3. **Deploy to GitHub Pages:**
   ```bash
   cd ~/clawd-webdesign/[client-slug]
   git init
   git add .
   git commit -m "Initial site for [Business Name]"
   gh repo create zentra-web-design/[client-slug] --public --source=. --push
   gh api repos/zentra-web-design/[client-slug]/pages -X POST -F 'source[branch]=main' -F 'source[path]=/'
   ```

4. **Deliver Live URL:**
   ```
   https://zentra-web-design.github.io/[client-slug]/
   ```

**Total Time:** ~10-15 minutes per client

---

## 🌐 Custom Domain Setup (When Client Buys Domain)

### Process:
1. Client purchases domain (e.g., `southwoodauto.com`)
2. Mr. Rasul provides domain registrar access
3. Agent adds DNS records:

**DNS Configuration (for GitHub Pages):**
```
Type: A     | Name: @    | Value: 185.199.108.153
Type: A     | Name: @    | Value: 185.199.109.153
Type: A     | Name: @    | Value: 185.199.110.153
Type: A     | Name: @    | Value: 185.199.111.153
Type: CNAME | Name: www  | Value: zentra-web-design.github.io
```

4. Configure GitHub Pages custom domain:
```bash
echo "southwoodauto.com" > CNAME
git add CNAME
git commit -m "Add custom domain"
git push
```

5. Wait 10-60 minutes for DNS propagation
6. GitHub automatically provisions FREE SSL certificate
7. Site goes live on custom domain with HTTPS

---

## 📝 Important Files in Each Project

### Documentation:
- `PROJECT-HANDOFF.md` - This file (workflow reference)
- `DEPLOYMENT-INFO.md` - Live URLs, repo info, pricing
- `REVIEWS-INFO.md` - List of real reviews used
- `README.md` - Template usage guide

### Website Files:
- `index.html` - Homepage
- `about.html` - About page
- `services.html` - Services page
- `pricing.html` - Pricing page
- `testimonials.html` - Testimonials page

---

## ✅ Client Edit Requests

### When Client Wants Changes:

1. Edit the HTML files in their project folder
2. Commit and push:
```bash
cd ~/clawd-webdesign/[client-slug]
# Make edits
git add .
git commit -m "Update per client request: [what changed]"
git push
```
3. Changes go live automatically in 1-2 minutes
4. Bill client for maintenance ($50/month covers all edits)

### Common Edit Types:
- Text changes (hours, phone, address)
- Service pricing updates
- Adding new testimonials
- Changing photos/colors
- Adding new pages

**Agent can handle ALL edits** - just describe what client wants changed.

---

## 🛠 Technical Stack

### Hosting:
- **Platform:** GitHub Pages (free, unlimited bandwidth)
- **Organization:** zentra-web-design
- **SSL:** Automatic HTTPS
- **CDN:** Global distribution included

### Development:
- **Languages:** Pure HTML/CSS (no frameworks needed)
- **Design:** Modern gradient-based, fully responsive
- **Fonts:** Google Fonts (Inter)
- **Icons:** Emoji (no external dependencies)

### Tools:
- **GitHub CLI:** `gh` (authenticated and ready)
- **Git:** Version control for all sites
- **Local Preview:** `python3 -m http.server 8080`

---

## 🚨 Known Issues & Solutions

### Issue: Netlify Bandwidth Exceeded
**Solution:** Switched to GitHub Pages (unlimited free bandwidth)

### Issue: GitHub CLI Not Installed
**Solution:** Already installed via Homebrew (`brew install gh`)

### Issue: Personal Username in URLs
**Solution:** Created `zentra-web-design` organization for professional branding

---

## 💡 Future Enhancements

### Potential Add-ons:
- Online booking system integration
- Google Maps embed
- Live chat widget
- Photo galleries
- Blog section
- Email contact forms
- Social media feeds

### Template Expansion:
- Save variants for different industries (restaurants, plumbers, dentists)
- Build Zentra Web Design agency site
- Create pricing packages document
- Develop client onboarding checklist

---

## 📞 Key Contacts

**Client:** Southwood Automotive Ltd
- Phone: (587) 352-9990
- Address: 11029 Elbow Dr SW, Calgary, AB T2W 1G7

**Owner:** Mr. Rasul (via WhatsApp +18255212075)

---

## 🎯 Success Metrics

### Goals:
- ✅ Professional website template created
- ✅ Real Google reviews integrated
- ✅ GitHub Pages deployment automated
- ✅ Zentra Web Design brand established
- ⏳ First client pitch pending
- ⏳ First $500 sale pending
- ⏳ Scale to multiple clients

### Revenue Target:
- 5 clients @ $500 setup = $2,500
- 5 clients @ $50/month = $250/month recurring
- **Annual value per client:** $500 + ($50 × 12) = $1,100

**10 clients = $11,000 first year revenue** 💰

---

## 📚 Resources

### GitHub Pages Docs:
https://docs.github.com/pages

### DNS Setup Guide:
https://docs.github.com/pages/configuring-a-custom-domain-for-your-github-pages-site

### Template Location:
`~/Desktop/auto-shop-template/`

### Live Example:
https://zentra-web-design.github.io/southwood-automotive-pitch/

---

## 🤖 Agent Instructions

**Agent webdesign** and **Agent main** both have access to:
1. All files in `/Users/rasulabdullayev/clawd-webdesign/`
2. Template on Desktop: `~/Desktop/auto-shop-template/`
3. GitHub CLI authenticated as `rasulabdullayev510-create`
4. Access to `zentra-web-design` organization

**When tagged, remember:**
- This entire workflow
- Template location and structure
- GitHub Pages deployment process
- Custom domain setup steps
- Pricing structure for clients

**DO NOT:**
- Forget the workflow
- Use personal GitHub username for new sites
- Deploy to Netlify (bandwidth issues)
- Fake reviews (always extract real ones from Google)

---

**Created:** March 15, 2026  
**Last Updated:** March 15, 2026  
**Status:** ✅ Ready for client pitches and scaling

---

## 🚀 READY TO MAKE MONEY! 💰
