# Alphington Landing Page Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the Alphington Accounting Services landing page. Follow these steps to make common updates while preserving the page's design and functionality.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the company name and navigation menu. To update:

1. **Company Name:**
```html
<div class="text-2xl font-bold text-gray-800">Alphington</div>
```
- Replace "Alphington" with your company name
- Adjust text size by changing `text-2xl` to `text-xl` (smaller) or `text-3xl` (larger)

### Hero Section
Located at the top of the page with the main headline:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 leading-tight mb-6">
    We transform numbers into opportunities
</h1>
```
- Update the headline text between the `<h1>` tags
- The classes ensure responsive text sizing:
  - `text-4xl`: Mobile devices
  - `md:text-5xl`: Medium screens
  - `lg:text-6xl`: Large screens

### Features Section
Each feature card follows this structure:
```html
<div class="bg-white rounded-xl shadow-lg p-8 hover:shadow-xl transition-shadow duration-300">
    <div class="w-12 h-12 bg-blue-100 rounded-lg flex items-center justify-center mb-6">
        <i class="fas fa-user-tie text-blue-600 text-2xl"></i>
    </div>
    <h3 class="text-xl font-semibold mb-4">Dedicated Manager</h3>
    <p class="text-gray-600">Your personal financial expert...</p>
</div>
```
To modify:
1. Change the icon by updating the `fa-user-tie` class to any [Font Awesome](https://fontawesome.com/icons) icon
2. Update the heading text in the `<h3>` tag
3. Modify the description in the `<p>` tag

## Managing Links

### Navigation Menu Links
The navigation menu contains internal page links:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Services</a>
    <a href="#benefits" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Benefits</a>
    <a href="#faq" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">FAQ</a>
    <a href="#contact" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Contact</a>
</div>
```
To update:
1. Locate the `href` attribute in each `<a>` tag
2. For internal links, use `#section-id` format
3. For external links, use the full URL: `https://example.com`

### Call-to-Action Buttons
Two main CTA buttons need updating:
```html
<!-- Hero Section CTA -->
<a href="https://theaccountants.com" class="inline-block bg-blue-600 text-white px-8 py-4 rounded-lg...">
    Get Started Today
</a>

<!-- CTA Section Button -->
<a href="https://theaccountants.com" class="inline-block bg-white text-blue-600 px-8 py-4 rounded-lg...">
    Schedule a Consultation
</a>
```
Replace `https://theaccountants.com` with your actual booking or contact page URL.

## Adding Privacy and Terms Pages

### Footer Link Updates
Locate the Legal section in the footer:
```html
<div>
    <h4 class="text-lg font-semibold text-white mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
        <li><a href="#" class="hover:text-white transition-colors duration-300">Contact Us</a></li>
    </ul>
</div>
```

To link privacy and terms pages:
1. Create `privacy.html` and `terms.html` in your root directory
2. Update the href attributes:
```html
<li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Internal Links**
   - Ensure section IDs match the href attributes
   - Check for typos in IDs
   - IDs should not contain spaces

2. **Responsive Design Issues**
   - Don't remove `md:` or `lg:` prefixes from classes
   - Keep the viewport meta tag intact:
   ```html
   <meta name="viewport" content="width=device-width, initial-scale=1.0">
   ```

3. **Icons Not Displaying**
   - Verify the Font Awesome CDN link is present in the head
   - Check icon class names against the [Font Awesome website](https://fontawesome.com)
   - Ensure internet connectivity to load the CDN

### Need Help?
- Review the [Tailwind CSS documentation](https://tailwindcss.com/docs) for styling guidance
- Consult the [Font Awesome documentation](https://fontawesome.com/docs) for icon updates
- Test all changes in multiple browsers and screen sizes

Remember to always backup your files before making significant changes to the code.