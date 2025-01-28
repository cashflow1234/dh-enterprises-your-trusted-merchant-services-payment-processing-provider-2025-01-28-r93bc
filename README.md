# DH Enterprises Landing Page - Maintenance Guide

This guide will help you maintain and customize the DH Enterprises landing page. It's written for beginners with no prior coding experience.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the company name and navigation menu. To update:

1. Company Name:
```html
<div class="text-2xl font-bold text-gray-800 dark:text-white">DH Enterprises</div>
```
Simply replace "DH Enterprises" with your desired text.

### Hero Section
Located at the top of the page with blue gradient background:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-white mb-8 leading-tight">
    Your Trusted Merchant Services Payment Processing Provider
</h1>
<p class="text-xl md:text-2xl text-blue-100 mb-12">
    Get started processing credit and debit card payments...
</p>
```

Key Tailwind classes explained:
- `text-4xl`: Large text on mobile
- `md:text-5xl`: Larger text on medium screens
- `lg:text-6xl`: Largest text on large screens
- `mb-8`: Margin bottom spacing
- `text-white`: White text color

### Features Section
To modify feature cards:

1. Find the feature section with ID "features"
2. Each feature is contained in a `div` with classes:
```html
<div class="bg-white dark:bg-gray-700 rounded-xl shadow-lg p-8">
```

To add/modify features:
1. Copy an existing feature div
2. Update the icon: `<i class="fas fa-shield-alt text-4xl"></i>`
3. Change heading: `<h3 class="text-xl font-bold">New Feature</h3>`
4. Modify description text

## Managing Links

### Navigation Menu Links
Current navigation links are:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```

To update:
1. Change the `href` value to match your section ID
2. Update the link text between the tags
3. Maintain the classes for consistent styling:
```html
<a href="#new-section" class="text-gray-600 dark:text-gray-300 hover:text-blue-600 transition duration-300">New Link</a>
```

### External Links
The quote form link appears in multiple places:
```html
<a href="https://form.jotform.com/250266352834053">Get Free Quote</a>
```

To update:
1. Replace the URL with your new form link
2. Keep the existing classes for consistent styling

## Adding Privacy and Terms Pages

### Current Footer Links
```html
<li><a href="#" class="text-gray-400 hover:text-white transition duration-300">Privacy Policy</a></li>
<li><a href="#" class="text-gray-400 hover:text-white transition duration-300">Terms of Service</a></li>
```

To add proper links:
1. Create privacy.html and terms.html in your root directory
2. Update the href attributes:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white transition duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white transition duration-300">Terms of Service</a></li>
```

## Troubleshooting

Common Issues:
1. **Broken Layout**: Check that you haven't removed important Tailwind classes
2. **Missing Icons**: Ensure Font Awesome is properly loaded in the head section
3. **Non-working Links**: Verify that:
   - Internal links (#) match section IDs
   - External links include https://
   - File paths are correct for privacy/terms pages

### Quick Fixes
- If text styling breaks, copy classes from a similar element
- If responsive design breaks, ensure `md:` and `lg:` prefixed classes remain
- If colors look wrong, check for both light and dark mode classes (dark:)

Need help? Contact support at [email protected]

---

Remember to:
- Test all changes on multiple screen sizes
- Keep backups of working code
- Validate links before publishing
- Maintain consistent styling across sections

This guide specifically matches your landing page structure. For additional customization needs, please consult the Tailwind CSS documentation or reach out for support.