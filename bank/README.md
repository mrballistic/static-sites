# SecureBank Demo - RCS Mock Banking Interface

A mobile-first banking demo interface for RCS demonstrations. This is a non-functional mockup designed to look convincing for demo purposes.

## Features

- **Mobile-first responsive design**
- **Convincing bank login interface**
- **Mock dashboard with realistic banking elements**
- **Clean, modern UI with gradient backgrounds**
- **Smooth animations and transitions**
- **Security-focused visual elements**

## Pages Included

1. **index.html** - Main login page
2. **dashboard.html** - Mock account dashboard
3. **forgot-password.html** - Password reset form
4. **signup.html** - Account creation form

## Quick Setup

### Local Development
```bash
# Navigate to the bank demo directory
cd /Users/todd.greco/Library/CloudStorage/OneDrive-Slalom/Documents/work/google/static-sites/bank

# Serve with Python (if available)
python3 -m http.server 8000

# Or with Node.js (if available)
npx serve .
```

### Nginx Deployment
1. Copy all files from the `/bank` folder to your nginx web root (typically `/usr/share/nginx/html/bank/`)
2. Use the provided `nginx.conf` for optimal configuration
3. Restart nginx service

### Docker Deployment
```bash
# Create a simple Dockerfile
echo "FROM nginx:alpine
COPY . /usr/share/nginx/html/
COPY nginx.conf /etc/nginx/conf.d/default.conf" > Dockerfile

# Build and run
docker build -t rcs-bank-demo .
docker run -p 8080:80 rcs-bank-demo
```

## File Structure
```
/bank/
├── index.html          # Main login page
├── dashboard.html      # Account dashboard
├── forgot-password.html # Password reset
├── signup.html         # Account creation
├── styles.css          # Shared stylesheet
├── nginx.conf          # Nginx configuration
└── README.md           # This file
```

## Demo Flow

1. **Login Page** (`index.html`) - Enter any credentials, click "Sign In"
2. **Dashboard** (`dashboard.html`) - View mock account balance and transactions
3. **Additional Forms** - Forgot password and signup flows

## Customization

### Colors
The primary color scheme uses:
- Primary: `#667eea` (purple-blue gradient)
- Secondary: `#764ba2` 
- Bank Blue: `#1B365D`
- Backgrounds: White cards on gradient backgrounds

### Branding
- Change logo SVG in the header sections
- Update "SecureBank" text throughout
- Modify color scheme in `styles.css`

## Notes

- **Non-functional**: Forms don't actually process data
- **Demo purposes only**: Not suitable for real banking applications
- **Mobile-optimized**: Designed for mobile-first experience
- **Modern browsers**: Uses CSS Grid, Flexbox, and modern JavaScript

## Security Headers

The nginx configuration includes security headers appropriate for a banking demo:
- X-Frame-Options
- X-Content-Type-Options  
- X-XSS-Protection
- Referrer-Policy

Perfect for demonstrating security-conscious web development practices.
