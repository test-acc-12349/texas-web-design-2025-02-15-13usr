# Texas Web Design Landing Page - Maintenance Guide

This guide will help you maintain and customize the Texas Web Design landing page. Whether you're new to web development or need a quick reference, follow these instructions to make common updates safely and effectively.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains the company logo and navigation menu. To update:

```html
<!-- Logo Text -->
<div class="text-2xl font-bold text-blue-600">TWD</div>  <!-- Change TWD to your company name -->

<!-- Navigation Menu Items -->
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>  <!-- Update menu text here -->
</div>
```

### Hero Section
To modify the main headline and subheading:

```html
<h1 class="text-4xl md:text-6xl font-bold mb-6">Texas Web Design</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-12">Best Websites In Texas</p>
```

💡 **Tip**: The `md:text-6xl` means the text will be larger on medium-sized screens and above.

### Tailwind CSS Class Guide
Common classes used in this template:
- `container mx-auto`: Centers content with automatic margins
- `px-6`: Adds horizontal padding (6 units)
- `py-4`: Adds vertical padding (4 units)
- `text-gray-600`: Sets text color to gray
- `hover:text-blue-600`: Changes text color to blue on hover

## Fixing Broken Links

### Navigation Menu Links
Current internal links in the navigation:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```

To update these:
1. Locate the section you want to link to
2. Ensure it has a matching `id` attribute
3. Use the `#` symbol followed by the `id` in the `href`

### Call-to-Action Links
The following links need to be updated from placeholder URLs:
```html
<a href="https://twd.com" class="bg-blue-600 text-white">Get Started</a>
```

Replace `https://twd.com` with your actual website URL.

## Linking Privacy and Terms Pages

### Current Footer Structure
```html
<div>
    <h4 class="text-lg font-semibold text-white mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

### To Add Privacy and Terms Links:
1. Create your privacy.html and terms.html files
2. Update the href attributes:
```html
<li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Internal Links**
   - Check that section IDs match exactly with href attributes
   - IDs are case-sensitive
   ```html
   <section id="features">  <!-- Must match href="#features" -->
   ```

2. **Responsive Design Issues**
   - Ensure you keep both mobile and desktop classes
   - Example: `text-4xl md:text-6xl` (don't remove either part)

3. **Missing Styles**
   - Verify the Tailwind CSS CDN link is present in the head:
   ```html
   <script src="https://cdn.tailwindcss.com"></script>
   ```

### Need Help?
If you encounter issues:
1. Check the browser's developer tools (F12) for errors
2. Verify all files are in the correct directory
3. Ensure all HTML tags are properly closed
4. Double-check that class names are spelled correctly

Remember: Always make a backup of your files before making changes!

For additional assistance, refer to:
- [Tailwind CSS Documentation](https://tailwindcss.com/docs)
- [HTML MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/HTML)