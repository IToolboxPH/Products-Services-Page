# IToolbox Landing Page - Setup Guide

**Status:** ✅ Active Development  
**Version:** 1.0  
**Last Updated:** February 5, 2026

---

## 📋 Overview

Modern, responsive landing page for IToolbox startup company featuring:
- Product showcase
- Contact form with analytics
- Mobile-responsive design
- Built-in visitor tracking
- Dark theme with gradient accents

---

## 🚀 Quick Start

### Option 1: Direct File Access (Simplest)
```bash
cd "<type here the directory path to your landing_page folder>"
open index.html
```

### Option 2: Local HTTP Server (Recommended)
```bash
# Using Python
cd "<type here the directory path to your landing_page folder>"
python3 -m http.server 8000

# Access at: http://localhost:8000
```

### Option 3: VS Code Live Server
1. Install "Live Server" extension in VS Code
2. Right-click on `index.html`
3. Select "Open with Live Server"

---

## 📁 Project Structure

```
landing_page/
├── index.html           # Main landing page
├── css/
│   └── style.css       # Styles and responsive design
├── js/
│   └── main.js         # Interactivity and analytics
└── assets/             # Images, icons, media (to be added)
    └── icons           # (Add your favicon)
    └── images          # (Add your images, e.g. logo)
```

---

## ✨ Features

### 1. Hero Section
- Eye-catching gradient text
- Clear call-to-action buttons
- Company statistics display
- Animated background effects

### 2. Product Showcase
- BilMoko - Price Aggregator
- InForMa - Forest Monitoring (Featured)
- DigiCool - School Platform
- Interactive hover effects
- Status badges (Active/Planning)

### 3. Contact Form
- Name, email, company fields
- Product interest dropdown
- Message textarea
- Form validation
- Submission tracking

### 4. Analytics (Built-in)
- Page view tracking
- Event tracking (button clicks, form submissions)
- Scroll depth monitoring
- Time on page tracking
- Data stored in localStorage

### 5. Responsive Design
- Mobile-first approach
- Hamburger menu for mobile
- Tablet and desktop layouts
- Smooth animations

---

## 🎨 Customization

### Colors (CSS Variables in style.css)
```css
--primary-color: #2563eb;     /* Blue */
--secondary-color: #7c3aed;   /* Purple */
--accent-color: #06b6d4;      /* Cyan */
--success-color: #10b981;     /* Green */
--warning-color: #f59e0b;     /* Orange */
```

### Company Information
Edit in `index.html`:
- Company name and logo
- Contact information (email, phone, address)
- Social media links
- Product descriptions

### Configuration
Edit `config.yaml` for:
- Company details
- Product information
- Social media URLs
- Feature flags

---

## 📊 Analytics Dashboard

### Access Analytics Data (Browser Console)
```javascript
// View all analytics
getAnalyticsSummary()

// Export analytics to JSON file
exportAnalytics()

// Clear analytics (testing only)
clearAnalytics()
```

### Data Collected
- **Page Views:** URL, referrer, timestamp, user agent, screen size
- **Events:** CTA clicks, product clicks, social clicks, scroll depth
- **Form Submissions:** Name, email, company, interest, message, timestamp

---

## 🔧 Technical Details

### Technologies Used
- **HTML5:** Semantic markup
- **CSS3:** Flexbox, Grid, animations, transitions
- **Vanilla JavaScript:** ES6+, no frameworks
- **Font Awesome:** Icons
- **Google Fonts:** Inter font family

### Browser Support
- Chrome/Edge (latest)
- Firefox (latest)
- Safari (latest)
- Mobile browsers (iOS Safari, Chrome Mobile)

### Performance
- Minimal dependencies
- Optimized CSS
- Lazy loading ready
- Fast load times

---

## 📝 Content Updates

### Update Product Information
Edit `index.html` in the Products section:
```html
<div class="product-card">
    <div class="product-icon">
        <i class="fas fa-ICON"></i>
    </div>
    <h3>Product Name</h3>
    <p class="product-tagline">Tagline</p>
    <p class="product-description">Description</p>
    <!-- ... -->
</div>
```

### Update Contact Information
Edit `index.html` in the Contact section:
```html
<div class="info-item">
    <i class="fas fa-envelope"></i>
    <div>
        <h4>Email</h4>
        <p>your-email@itoolbox.ph</p>
    </div>
</div>
```

---

## 🚀 Deployment Guide

### Option 1: Static Hosting (Netlify/Vercel)
1. Push code to GitHub repository
2. Connect to Netlify or Vercel
3. Deploy from `landing_page/` directory
4. Custom domain: itoolbox.ph

### Option 2: Traditional Hosting
1. Upload all files via FTP/SFTP
2. Point domain to hosting server
3. Configure SSL certificate
4. Test all functionality

### Option 3: GitHub Pages
1. Push to GitHub repository
2. Enable GitHub Pages in settings
3. Select branch and `/landing_page` folder
4. Access via: username.github.io/repo

---

## 🔒 Before Going Live

### Checklist
- [ ] Update all contact information
- [ ] Add real email addresses
- [ ] Add phone number
- [ ] Configure social media links
- [ ] Add company logo and favicon
- [ ] Set up contact form backend
- [ ] Implement real analytics (Google Analytics)
- [ ] Test on all devices and browsers
- [ ] Set up SSL certificate
- [ ] Configure domain (itoolbox.ph)
- [ ] Add privacy policy and terms
- [ ] Test all links and forms
- [ ] Optimize images
- [ ] Set up error pages (404, etc.)

### Form Backend Options
**Current:** Data stored in localStorage (development only)

**Production Options:**
1. **Backend API:** Create Node.js/Python backend
2. **Email Service:** Use EmailJS or FormSubmit
3. **Database:** Store in PostgreSQL/MongoDB
4. **Third-party:** Use Typeform, Formspree, or similar

---

## 📧 Contact Form Integration

### Example: EmailJS Integration
```javascript
// In main.js, replace form submission with:
emailjs.send('service_id', 'template_id', formData)
    .then(() => {
        alert('Message sent successfully!');
        contactForm.reset();
    })
    .catch((error) => {
        console.error('Error:', error);
        alert('Failed to send message.');
    });
```

### Example: Backend API
```javascript
// POST to your backend
const response = await fetch('https://api.itoolbox.ph/contact', {
    method: 'POST',
    headers: { 'Content-Type': 'application/json' },
    body: JSON.stringify(formData)
});
```

---

## 🎯 Next Steps

### Immediate (Week 1)
1. ✅ Landing page structure complete
2. ⏳ Add company logo and branding assets
3. ⏳ Set up real contact email
4. ⏳ Create social media accounts
5. ⏳ Test on multiple devices

### Short-term (Month 1)
1. Set up contact form backend
2. Implement Google Analytics
3. Add more product details
4. Create blog section (optional)
5. Prepare for domain purchase

### Long-term (Quarter 1)
1. Deploy to production
2. SEO optimization
3. Add case studies/testimonials
4. Multi-language support (optional)
5. A/B testing framework

---

## 🤝 Contributing

As this is a startup project, updates should be made through:
1. Direct edits by CEO (Nico M.)
2. Pull requests from team members (when hired)
3. Version control via Git

---

## 📞 Support

**Internal Contact:**
- CEO: Nico M.
- Email: nico@itoolbox.ph

---

**Last Updated:** February 5, 2026  
**Maintained By:** Nico M., Founding President & CEO
