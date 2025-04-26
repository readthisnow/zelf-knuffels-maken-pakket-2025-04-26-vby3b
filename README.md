# KnuffelMaker Landing Page - Maintenance Guide

This guide will help you maintain and customize the KnuffelMaker landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions for common updates.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the site logo and navigation menu. To update:

1. **Logo Text:**
```html
<a href="#" class="text-2xl font-bold text-purple-600">KnuffelMaker</a>
```
- Replace "KnuffelMaker" with your desired brand name
- Adjust size using `text-2xl` (options: text-lg, text-3xl, etc.)
- Change color using `text-purple-600` (options: text-blue-600, text-red-600, etc.)

2. **Navigation Menu Items:**
```html
<a href="#features" class="text-gray-600 hover:text-purple-600">Kenmerken</a>
```
- Replace "Kenmerken" with your desired menu text
- Keep the `href` matching your section IDs
- Maintain the hover effect classes for consistency

### Hero Section
Located at the top of the page:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-extrabold text-gray-900 mb-8 leading-tight">
    Zelf Knuffels Maken Pakket
</h1>
```
- Update the heading text between the `<h1>` tags
- The classes ensure responsive text sizing:
  - `text-4xl`: Mobile devices
  - `md:text-5xl`: Medium screens
  - `lg:text-6xl`: Large screens

### Tailwind CSS Tips for Beginners
- Spacing classes use this format: `m-[number]` for margin, `p-[number]` for padding
- Colors use this format: `[type]-[color]-[shade]`
  - Example: `bg-purple-600`, `text-gray-900`
- Responsive prefixes: `sm:`, `md:`, `lg:`, `xl:`
  - Example: `md:hidden` means hidden on medium screens and up

## Managing Links

### Navigation Menu Links
Current internal links in the navigation:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Kenmerken</a>
    <a href="#benefits">Voordelen</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
</div>
```

To update:
1. Locate the section ID in the main content
2. Update the `href` to match using `#section-id`
3. Ensure the section ID exists in the HTML

### Call-to-Action Buttons
Current purchase link:
```html
<a href="https://amzn.to/42x6ZXR" class="inline-flex items-center px-8 py-4 rounded-full">
    Bestel Nu
</a>
```

To update:
1. Replace the Amazon affiliate link with your product URL
2. Maintain the class structure for consistent styling
3. Test the link thoroughly before deployment

## Adding Privacy and Terms Pages

### Footer Link Updates
Current footer links:
```html
<ul class="space-y-2">
    <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
    <li><a href="#" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
</ul>
```

To add privacy and terms pages:

1. Create new HTML files:
```bash
privacy.html
terms.html
```

2. Update the footer links:
```html
<li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

3. Ensure consistent styling by copying the header and footer from index.html to your new pages

## Troubleshooting

### Common Issues and Solutions

1. **Broken Internal Links**
- Check that section IDs match exactly with href attributes
- IDs are case-sensitive
- Example: `href="#FAQ"` won't link to `id="faq"`

2. **Responsive Design Issues**
- Test all screen sizes using browser developer tools
- Verify media query classes (sm:, md:, lg:) are correct
- Common fix: Add missing responsive classes to parent containers

3. **Style Inconsistencies**
- Compare classes with working elements
- Check for typos in Tailwind class names
- Verify the Tailwind CSS CDN link is working

### Need Help?
- Check the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Use browser developer tools (F12) to inspect elements
- Test all changes in multiple browsers
- Keep a backup of the original code before making changes

Remember to always test your changes thoroughly before pushing to production, and maintain regular backups of your working code.