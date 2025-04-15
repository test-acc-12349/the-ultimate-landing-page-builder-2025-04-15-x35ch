# Landing Page Maintenance Guide

This guide will help you maintain and customize your landing page. Follow these detailed instructions to make updates while preserving the design and functionality.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains your logo and navigation menu. To update:

1. Change the logo text:
```html
<!-- Find this line in the header -->
<a href="/" class="text-xl font-bold text-blue-600">PageBuilder</a>
```
Simply replace "PageBuilder" with your desired text.

### Hero Section
Located at the top of the page with the main headline:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 leading-tight mb-6">
    The Ultimate Landing Page Builder
</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-12">
    Create stunning landing pages in minutes
</p>
```

To modify:
1. Replace the h1 text between the tags
2. Update the subtitle in the p tag
3. The sizing classes (text-4xl, etc.) control text size at different breakpoints:
   - `text-4xl`: Default size
   - `md:text-5xl`: Medium screens
   - `lg:text-6xl`: Large screens

### Features Section
Each feature card follows this structure:

```html
<div class="bg-white rounded-xl p-8 shadow-lg hover:shadow-xl transition-shadow duration-300">
    <div class="w-12 h-12 bg-blue-100 rounded-lg flex items-center justify-center mb-6">
        <!-- Icon SVG here -->
    </div>
    <h3 class="text-xl font-semibold mb-4">Clean Modern Design</h3>
    <p class="text-gray-600">Create beautiful, professional landing pages...</p>
</div>
```

To update:
1. Modify the h3 text for the feature title
2. Change the p text for the feature description
3. Key styling classes:
   - `rounded-xl`: Rounds the corners
   - `shadow-lg`: Adds shadow
   - `hover:shadow-xl`: Increases shadow on hover

## Managing Links

### Navigation Menu Links
Current navigation links are:

```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
</div>
```

To update:
1. Internal links (same page):
   - Keep the # symbol
   - Match the id of the section (e.g., `href="#features"`)
2. External links:
   - Replace href with full URL
   - Example: `href="https://yoursite.com/page"`

### Call-to-Action Buttons
Currently pointing to "https://fixrr.online". Update these locations:

```html
<!-- Header CTA -->
<a href="https://fixrr.online" class="hidden md:inline-flex...">

<!-- Hero CTA -->
<a href="https://fixrr.online" class="inline-flex items-center...">

<!-- Bottom CTA -->
<a href="https://fixrr.online" class="inline-flex items-center...">
```

Replace all instances of "https://fixrr.online" with your desired URL.

## Adding Privacy and Terms Pages

### Footer Link Setup
Current placeholder links in footer:

```html
<ul class="space-y-2">
    <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
    <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
</ul>
```

To link to new pages:
1. Create privacy.html and terms.html in your root directory
2. Update the href attributes:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

Common issues and solutions:

1. **Broken Internal Links**
   - Ensure section IDs match href attributes
   - IDs are case-sensitive
   - Example: `href="#FAQ"` won't link to `id="faq"`

2. **Responsive Design Issues**
   - Don't remove `md:` or `lg:` prefixes from classes
   - These control how elements appear on different screen sizes
   - Test on mobile, tablet, and desktop views

3. **Style Changes Not Working**
   - Check for typos in Tailwind class names
   - Maintain spaces between multiple classes
   - Keep the original responsive classes when adding new ones

Remember to:
- Test all links after making changes
- View the page on different devices
- Keep backup copies of working code
- Validate HTML at [W3C Validator](https://validator.w3.org/)

Need more help? Refer to the [Tailwind CSS documentation](https://tailwindcss.com/docs) or contact your development team.