# Deployment Instructions for Knowledge Management System

This document provides instructions for deploying the Knowledge Management System static website to your own server.

## Contents of the Bundle

The bundle contains the following files and directories:

- `index.html` - Main dashboard page
- `analysis.html` - Research directions analysis page
- `documentation.html` - System documentation page
- `about.html` - About page
- `css/` - Directory containing stylesheets
  - `styles.css` - Main stylesheet
- `js/` - Directory containing JavaScript files
  - `main.js` - Main JavaScript file
- `images/` - Directory for images (if any)

## Deployment Options

### Option 1: Simple Web Server

The simplest way to deploy this static website is to use any web server that can serve static files.

#### Using Apache

1. Install Apache (if not already installed):
   ```
   sudo apt update
   sudo apt install apache2
   ```

2. Copy the website files to the Apache document root:
   ```
   sudo cp -r * /var/www/html/
   ```

3. Ensure proper permissions:
   ```
   sudo chown -R www-data:www-data /var/www/html/
   ```

4. Restart Apache:
   ```
   sudo systemctl restart apache2
   ```

5. Access your website at `http://your-server-ip/`

#### Using Nginx

1. Install Nginx (if not already installed):
   ```
   sudo apt update
   sudo apt install nginx
   ```

2. Copy the website files to the Nginx document root:
   ```
   sudo cp -r * /var/www/html/
   ```

3. Ensure proper permissions:
   ```
   sudo chown -R www-data:www-data /var/www/html/
   ```

4. Restart Nginx:
   ```
   sudo systemctl restart nginx
   ```

5. Access your website at `http://your-server-ip/`

### Option 2: GitHub Pages

You can also host this static website using GitHub Pages:

1. Create a new GitHub repository

2. Upload all the website files to the repository

3. Go to the repository settings

4. Scroll down to the "GitHub Pages" section

5. Select the branch you want to deploy (usually `main` or `master`)

6. Click "Save"

7. Your website will be available at `https://your-username.github.io/your-repository-name/`

### Option 3: Other Static Site Hosting Services

You can use various static site hosting services:

- Netlify
- Vercel
- Firebase Hosting
- AWS S3 + CloudFront
- Azure Static Web Apps

Most of these services offer free tiers and simple deployment processes, often through a web interface or CLI tool.

## Customization

### Changing Content

To update the content of the website:

1. Edit the HTML files using any text editor
2. Modify the text within the HTML tags
3. Save the files and upload them to your server

### Changing Styles

To modify the appearance of the website:

1. Edit the `css/styles.css` file
2. Make your desired changes to the CSS rules
3. Save the file and upload it to your server

### Adding New Pages

To add new pages to the website:

1. Create a new HTML file based on the existing pages
2. Update the navigation links in all pages to include the new page
3. Save the files and upload them to your server

## Troubleshooting

### Common Issues

1. **404 Not Found errors**: Ensure all files are in the correct location and have proper permissions

2. **CSS not loading**: Check that the path to the CSS file is correct in all HTML files

3. **JavaScript not working**: Verify that the path to the JavaScript file is correct and that there are no console errors

### Getting Help

If you encounter any issues with deployment, you can:

1. Check the documentation for your chosen web server or hosting service
2. Search for solutions on Stack Overflow or similar forums
3. Contact your hosting provider's support team

## Maintenance

To keep your website up to date:

1. Regularly check for broken links
2. Update content as needed
3. Test the website in different browsers to ensure compatibility
4. Consider setting up a backup system for your website files

## Security Considerations

Even though this is a static website with no backend functionality:

1. Ensure your web server is kept up to date with security patches
2. Use HTTPS if possible (many hosting services provide this automatically)
3. Be cautious about adding third-party scripts or resources
