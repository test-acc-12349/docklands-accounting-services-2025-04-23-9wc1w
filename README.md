# Docklands Accounting Landing Page - Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the Docklands Accounting landing page. Whether you're new to web development or need a quick reference, you'll find step-by-step guidance for common maintenance tasks.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Text Content Updates

#### Header and Navigation
```html
<!-- Located in the header section -->
<a href="/" class="text-2xl font-bold">
    Docklands  <!-- Company name -->
</a>
```
To modify the company name, simply replace "Docklands" with your desired text.

#### Hero Section
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold mb-6">
    Docklands accounting services  <!-- Main headline -->
</h1>
<p class="text-xl md:text-2xl text-gray-300 mb-12">
    Partners in your financial journey  <!-- Subheading -->
</p>
```
- Update the main headline and subheading by replacing the text between the tags
- Maintain the existing classes to preserve responsive design

### Tailwind CSS Classes Explained

Key classes used throughout the page:

1. Text Sizes:
   - `text-4xl`: Large text (desktop)
   - `md:text-5xl`: Medium screen size adjustment
   - `lg:text-6xl`: Large screen size adjustment

2. Colors:
   - `text-gray-300`: Light gray text
   - `bg-gray-900`: Dark background
   - `from-purple-500 to-pink-500`: Gradient colors

3. Spacing:
   - `mb-6`: Bottom margin
   - `px-4`: Horizontal padding
   - `py-24`: Vertical padding

To modify styles, adjust these numbers while maintaining the pattern:
```html
<!-- Example: Changing text size and color -->
<h3 class="text-xl font-semibold mb-4">
<!-- Change to: -->
<h3 class="text-2xl font-bold mb-6 text-gray-200">
```

## Managing Links

### Navigation Menu Links
Current navigation links are located in the header:
```html
<div class="hidden md:flex items-center space-x-8">
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#contact">Contact Us</a>
</div>
```

To update links:
1. Internal links (same page sections):
   - Keep the `#` symbol
   - Match the ID of the target section
   ```html
   <a href="#new-section-id">New Section</a>
   ```

2. External links:
   - Replace with full URL
   ```html
   <a href="https://your-website.com/page">External Page</a>
   ```

### Footer Links
Located at the bottom of the page:
```html
<ul class="space-y-2 text-gray-400">
    <li><a href="#" class="hover:text-white transition-colors duration-300">About</a></li>
    <!-- Add more links here -->
</ul>
```

To update:
1. Replace `#` with your actual URL
2. Maintain the classes for consistent styling
3. Add new links by copying the `<li>` element pattern

## Adding Privacy and Terms Pages

### Step 1: Update Footer Links
Locate the Legal section in the footer:
```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2 text-gray-400">
        <li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy</a></li>
        <li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms</a></li>
    </ul>
</div>
```

### Step 2: Create Policy Pages
1. Create two new files:
   - `privacy.html`
   - `terms.html`

2. Link them using relative paths:
```html
<!-- Example privacy link -->
<a href="./privacy.html">Privacy Policy</a>

<!-- Example terms link -->
<a href="./terms.html">Terms of Service</a>
```

## Troubleshooting

### Common Issues and Solutions

1. Broken Internal Links
   - Check that section IDs match exactly with href values
   - Example:
     ```html
     <section id="features">  <!-- ID here -->
     <a href="#features">     <!-- Must match exactly -->
     ```

2. Responsive Design Issues
   - Maintain the responsive class patterns:
     ```html
     text-base md:text-lg lg:text-xl
     ```
   - Don't remove `md:` or `lg:` prefixes

3. Gradient Colors Not Showing
   - Ensure both `from-` and `to-` classes are present
   - Example:
     ```html
     class="bg-gradient-to-r from-purple-500 to-pink-500"
     ```

### Need Help?
If you encounter issues:
1. Check class names match exactly
2. Verify all tags are properly closed
3. Maintain the existing responsive design patterns
4. Test on multiple screen sizes using browser dev tools

Remember to always backup your files before making changes, and test thoroughly after updates.