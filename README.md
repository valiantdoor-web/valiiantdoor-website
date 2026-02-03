# Valiant Garage Door Website

Professional garage door service website for Valiant Garage Door - Your trusted partner for garage door repair, installation, and maintenance.

## 📋 Overview

This is a fully responsive, professional garage door service website featuring:
- Express.js backend with nodemailer for quote submissions
- Modern, clean design with professional branding
- Mobile-friendly navigation
- Multiple service pages (Commercial, Emergency, Installations)
- Quote request form with email notifications
- Customer testimonials and reviews
- Mission statement and gallery pages
- SEO-optimized with sitemap and robots.txt

## 🚀 Quick Start

### Prerequisites

- Node.js (v14 or higher)
- npm or yarn package manager
- Gmail account for email notifications (or other SMTP service)

### Installation

1. Clone the repository:
```bash
git clone https://github.com/vm-valiantshit/Valiiantdoor-Website.git
cd Valiiantdoor-Website
```

2. Install dependencies:
```bash
npm install
```

3. Set up environment variables:
```bash
cp .env.example .env
```

Edit `.env` and add your email credentials:
```
EMAIL_USER=your-email@gmail.com
EMAIL_PASS=your-app-password
EMAIL_TO=business@valiantgaragedoor.com
PORT=3000
```

**Note:** For Gmail, you need to use an [App Password](https://support.google.com/accounts/answer/185833) instead of your regular password.

### Running Locally

Development mode (with auto-restart):
```bash
npm run dev
```

Production mode:
```bash
npm start
```

The website will be available at `http://localhost:3000`

### Project Structure

```
valiiantdoor-website/
├── server/
│   └── server.js               # Express server with nodemailer
├── assets/
│   ├── logo/                   # Logo files
│   └── [other images]          # Service images, backgrounds, icons
├── services/
│   ├── commercial.html         # Commercial solutions page
│   ├── emergency.html          # Emergency services page
│   └── installations.html      # New installations page
├── css/
│   └── styles.css              # Main stylesheet
├── js/
│   └── main.js                 # JavaScript functionality
├── data/
│   └── reviews.json            # Customer reviews data
├── index.html                  # Homepage
├── services.html               # Services overview
├── quote.html                  # Quote request form
├── mission.html                # Mission statement
├── gallery.html                # Project gallery
├── about.html                  # About us page
├── contact.html                # Contact page
├── robots.txt                  # SEO robots file
├── sitemap.xml                 # SEO sitemap
├── package.json                # Node.js dependencies
├── vercel.json                 # Vercel deployment config
├── .env.example                # Environment variables template
├── .gitignore                  # Git ignore rules
└── README.md                   # This file
```

## 🌐 Deployment to Vercel

### One-Click Deploy

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new)

### Manual Deployment

1. Install Vercel CLI:
```bash
npm i -g vercel
```

2. Login to Vercel:
```bash
vercel login
```

3. Deploy:
```bash
vercel
```

4. Set environment variables in Vercel dashboard:
   - Go to your project settings
   - Navigate to "Environment Variables"
   - Add: `EMAIL_USER`, `EMAIL_PASS`, `EMAIL_TO`

5. Redeploy to apply environment variables:
```bash
vercel --prod
```

### Updating Production URL

After deployment, update the sitemap URL in `sitemap.xml` and `robots.txt` with your production domain.

## ✨ Features

### Pages
- **Home**: Welcome page with hero section, service overview, and call-to-action
- **Services**: Overview of all services with links to detailed pages
- **Commercial Solutions**: Commercial garage door services
- **Emergency Services**: 24/7 emergency repair services
- **New Installations**: Residential and commercial installations
- **Quote Request**: Form for requesting service quotes (with email notifications)
- **Mission**: Company mission statement and values
- **Gallery**: Project portfolio and completed work
- **About**: Company information
- **Contact**: Contact information and inquiry form

### Technical Features
- Express.js backend for serving static files and handling API requests
- Nodemailer integration for email notifications on quote submissions
- Responsive design (mobile, tablet, desktop)
- Modern UI with professional branding
- JSON-based customer reviews system
- SEO-optimized with sitemap and robots.txt
- Environment-based configuration
- Vercel-ready deployment configuration

## 🛠️ API Endpoints

### POST /api/requests
Submit a quote request form.

**Request Body:**
```json
{
  "name": "John Doe",
  "email": "john@example.com",
  "phone": "555-1234",
  "address": "123 Main St",
  "service": "Residential Repair",
  "message": "My garage door won't open"
}
```

**Response:**
```json
{
  "success": true,
  "message": "Quote request submitted successfully! We will contact you soon."
}
```

### GET /api/health
Check server status.

**Response:**
```json
{
  "status": "OK",
  "timestamp": "2026-02-03T21:54:00.000Z"
}
```

## 🔧 Customization

### Changing Colors

Edit `css/styles.css` to modify the color scheme:
- Primary color: Gold/Yellow (#FFD700)
- Secondary color: Red (#DC143C)
- Accent colors as needed

### Updating Content

1. **Company Information**: Edit text in HTML files
2. **Contact Details**: Update phone, email, and address in all pages
3. **Services**: Modify service pages to reflect your offerings
4. **Reviews**: Edit `data/reviews.json` to add/update customer testimonials
5. **Images**: Replace files in `assets/` directory with your own images

### Email Configuration

The contact form uses nodemailer to send emails. Supported email services:
- Gmail (default)
- Outlook/Hotmail
- SendGrid
- Custom SMTP

To use a different service, edit `server/server.js` and update the transporter configuration.

## 📱 Browser Support

The website is compatible with:
- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)
- Mobile browsers (iOS Safari, Chrome Mobile)

## 🧪 Testing

### Test Quote Form Locally

1. Start the server: `npm start`
2. Navigate to `http://localhost:3000/quote.html`
3. Fill out the form and submit
4. Check your email for the notification

### Test Static Pages

Simply open any HTML file in your browser or access via `http://localhost:3000/[page].html`

## 🐛 Troubleshooting

### Email Not Sending

1. **Gmail Users**: Make sure you're using an App Password, not your regular password
2. **Firewall**: Ensure port 587 (SMTP) is not blocked
3. **Environment Variables**: Verify `.env` file exists and has correct values
4. **Check Logs**: Look at console output for error messages

### Pages Not Loading

1. Ensure server is running: `npm start`
2. Check that all static files are in the correct directories
3. Verify port 3000 is not in use by another application

### Vercel Deployment Issues

1. Ensure `vercel.json` is properly configured
2. Add environment variables in Vercel dashboard
3. Check build logs in Vercel for specific errors
4. Verify Node.js version compatibility

## 📄 License

This website is part of the Valiant Garage Door business. All rights reserved.

## 📞 Support

For questions or issues, please contact:
- Email: business@valiantgaragedoor.com
- Phone: (555) 123-4567

## 🙏 Credits

Built with:
- Express.js - Web framework
- Nodemailer - Email sending
- Modern HTML5/CSS3/JavaScript
- Vercel - Hosting platform

## 🔄 Restoring Files from URL

If you need to restore or download website files from a backup URL, use the provided utility script:

```bash
# Basic usage
./download-from-url.sh <URL>

# Download to specific directory
./download-from-url.sh <URL> ./backup

# Example: Download from a backup ZIP
./download-from-url.sh https://example.com/website-backup.zip

# Example: Download from a TAR.GZ archive
./download-from-url.sh https://example.com/website-backup.tar.gz ./restore
```

The script will:
1. Download the file from the provided URL
2. Automatically detect and extract archives (ZIP, TAR, TAR.GZ)
3. Place the files in the specified destination
4. Optionally clean up archive files after extraction

### Supported Formats
- ZIP archives
- TAR archives
- TAR.GZ/TGZ archives
- Individual files (HTML, CSS, JS, images, etc.)

## 🌐 Deployment

### GitHub Pages

1. Go to your repository settings
2. Navigate to "Pages" section
3. Select the branch to deploy (usually `main`)
4. Click "Save"
5. Your site will be available at `https://yourusername.github.io/repository-name/`

### Other Hosting Services

Upload all files to your hosting provider via:
- FTP/SFTP
- cPanel File Manager
- Git deployment
- Hosting provider's dashboard

## ✨ Features

### Pages
- **Home**: Welcome page with service overview and call-to-action
- **Services**: Detailed information about all services offered
- **About**: Company story, values, and process
- **Contact**: Contact form and business information

### Design Features
- Responsive layout (mobile, tablet, desktop)
- Modern gradient headers
- Interactive navigation
- Service cards with hover effects
- Professional color scheme
- Smooth scrolling
- Mobile hamburger menu

## 🛠️ Customization

### Changing Colors

Edit `css/style.css` and modify the color variables:
- Primary color: `#3498db`
- Secondary color: `#2c3e50`
- Accent color: `#667eea`

### Updating Content

1. **Company Information**: Edit the text in each HTML file
2. **Contact Details**: Update phone, email, and address in all pages
3. **Services**: Modify `services.html` to reflect your offerings
4. **Navigation**: Edit the nav menu in each HTML file

### Adding Images

1. Create an `images/` directory
2. Add your images
3. Update HTML to reference your images:
   ```html
   <img src="images/your-image.jpg" alt="Description">
   ```

## 📱 Browser Support

The website is compatible with:
- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)
- Mobile browsers (iOS Safari, Chrome Mobile)

## 🐛 Troubleshooting

### Form Submission Not Working

The contact form currently logs data to console. To enable actual email sending, you'll need to:
1. Set up a backend service (Node.js, PHP, etc.)
2. Or use a form service like Formspree, Netlify Forms, or EmailJS
3. Update the form handler in `js/script.js`

### Mobile Menu Not Opening

Ensure JavaScript is enabled in your browser and `js/script.js` is properly linked.

## 📄 License

This website is part of the Valiantdoor business. All rights reserved.

## 📞 Support

For questions or issues, please contact:
- Email: info@valiantdoor.com
- Phone: (555) 123-4567
