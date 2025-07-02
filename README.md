# Career Catalyst Landing Page - Maintenance Guide

This guide will help you maintain and customize the Career Catalyst landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions for common updates.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains the logo and navigation menu. To update:

1. **Logo Text:**
```html
<!-- Find this section at the top of the page -->
<a href="/" class="text-2xl font-bold bg-gradient-to-r from-purple-600 to-blue-600 bg-clip-text text-transparent">
    Career Catalyst  <!-- Change this text to update the logo -->
</a>
```

2. **Navigation Menu Items:**
```html
<div class="hidden md:flex space-x-8">
    <!-- Update these link texts as needed -->
    <a href="#features" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Features</a>
    <a href="#benefits" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Benefits</a>
</div>
```

### Hero Section
Located at the top of the page:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-8 bg-gradient-to-r from-purple-600 to-blue-600 bg-clip-text text-transparent">
    Strategize Your Success. Achieve Your Career Goals.  <!-- Main headline -->
</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-12">
    Gain a competitive edge with Career Catalyst.  <!-- Subheadline -->
</p>
```

### Understanding Tailwind Classes
Common classes used in this landing page:

- Text sizes: `text-xl`, `text-2xl`, `text-3xl`, etc.
- Colors: `text-gray-600`, `bg-purple-600`
- Spacing: `px-6` (padding left/right), `py-4` (padding top/bottom), `mb-8` (margin bottom)
- Responsive design: `md:text-5xl` (applies at medium screens and up)

To modify styles:
1. Find the element you want to change
2. Update the Tailwind classes within the `class=""` attribute
3. Test on different screen sizes

Example:
```html
<!-- Original -->
<p class="text-xl text-gray-600">

<!-- Making text larger and darker -->
<p class="text-2xl text-gray-800">
```

## Fixing Broken Links

### Current Link Structure
The page contains several types of links:

1. **Navigation Menu Links:**
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```

2. **Call-to-Action Links:**
```html
<!-- Update this URL with your actual application URL -->
<a href="https://career-catalyst.site" class="inline-block px-8 py-4 bg-gradient-to-r from-purple-600 to-blue-600">
```

To update links:
1. Locate the `<a>` tag you want to modify
2. Change the `href` attribute to your desired URL
3. For internal links (same page sections), use `#section-id`
4. For external links, use the full URL including `https://`

Example:
```html
<!-- Internal link -->
<a href="#features">Features</a>

<!-- External link -->
<a href="https://your-domain.com/page">External Page</a>
```

## Linking Privacy and Terms Pages

### Adding Policy Links
Located in the footer section:

```html
<div>
    <h4 class="text-lg font-semibold text-white mb-4">Legal</h4>
    <ul class="space-y-2">
        <!-- Update these href attributes with your policy page URLs -->
        <li><a href="/privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="/terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To link your policy pages:
1. Create your `privacy.html` and `terms.html` files
2. Place them in the same directory as your `index.html`
3. Update the href attributes in the footer links
4. Maintain consistent styling by copying the existing classes

## Troubleshooting

Common issues and solutions:

1. **Broken Internal Links:**
- Ensure section IDs match the href attributes
- Check for typos in IDs and hrefs
- IDs are case-sensitive

2. **Responsive Design Issues:**
- Check media query classes (md:, lg:)
- Test on different screen sizes
- Verify Tailwind CDN is loading

3. **Gradient Text Not Showing:**
```html
<!-- All these classes are required for gradient text -->
class="bg-gradient-to-r from-purple-600 to-blue-600 bg-clip-text text-transparent"
```

Need help? Contact support at david@nexai.network

Remember to:
- Always backup before making changes
- Test all links after updating
- View changes on multiple devices
- Keep consistent styling throughout