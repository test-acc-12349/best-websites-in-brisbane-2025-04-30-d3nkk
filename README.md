# Brisbane Web Landing Page - Maintenance Guide

This guide will help you maintain and customize the Brisbane Web landing page. It's written for beginners with no prior coding experience.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Main Sections Overview
The landing page is divided into these key sections:
- Header (Navigation)
- Hero Section
- Features Section
- Benefits Section
- FAQ Section
- CTA Section
- Footer

### Updating Text Content

#### Hero Section
Find this section near the top of the file:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 leading-tight mb-8">
    Best Websites In Brisbane
</h1>
```
To change the main heading, simply replace "Best Websites In Brisbane" with your desired text.

#### Features Section
Locate the features cards:
```html
<div class="bg-white rounded-xl p-8 shadow-lg hover:shadow-xl transition-shadow duration-300">
    <h3 class="text-xl font-bold mb-4">Easy to Use</h3>
    <p class="text-gray-600">Intuitive interface and user-friendly design...</p>
</div>
```
To update a feature:
1. Change the heading text between `<h3>` tags
2. Modify the description between `<p>` tags
3. Update the icon by changing the Font Awesome class (e.g., `fa-magic` to `fa-star`)

### Modifying Tailwind CSS Classes

#### Understanding Responsive Classes
In this code, responsive classes use these prefixes:
- `md:` - applies to medium screens (768px and up)
- `lg:` - applies to large screens (1024px and up)

Example:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl">
```
This means:
- Mobile: text-4xl (2.25rem)
- Tablet: text-5xl (3rem)
- Desktop: text-6xl (3.75rem)

#### Common Tailwind Classes Used
- Spacing: `px-6` (padding left/right), `py-4` (padding top/bottom)
- Colors: `text-gray-600`, `bg-blue-600`
- Flex: `flex`, `items-center`, `justify-between`
- Hover: `hover:text-blue-600`, `hover:bg-blue-700`

## Managing Links

### Navigation Menu Links
Current navigation links are in the header:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
</div>
```

To update a link:
1. Locate the `<a>` tag
2. Change the `href` attribute
3. Update the text between the tags

Example updating Features link:
```html
<a href="#new-section" class="text-gray-600 hover:text-blue-600">New Section</a>
```

### External Links
The main CTA button links to an external site:
```html
<a href="https://sigmaseo.io" class="inline-block bg-blue-600...">
```

To update:
1. Replace `https://sigmaseo.io` with your desired URL
2. Ensure the URL includes `https://` or `http://`

## Adding Privacy and Terms Pages

### Step 1: Create New Pages
Create two new files in your website folder:
- `privacy.html`
- `terms.html`

### Step 2: Update Footer Links
Locate this section in the footer:
```html
<div>
    <h3 class="text-xl font-bold mb-4">Legal</h3>
    <ul class="space-y-2 text-gray-400">
        <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

Replace the `#` placeholders:
```html
<li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues

1. **Broken Links**
   - Check that all `href` attributes point to valid pages or sections
   - Ensure section IDs match their corresponding links (e.g., `#features` matches `id="features"`)

2. **Responsive Design Issues**
   - Test the page at different screen sizes
   - Verify that `md:` and `lg:` classes are working correctly
   - Use browser developer tools to check for CSS conflicts

3. **Icons Not Showing**
   - Confirm Font Awesome is properly loaded
   - Check that icon class names are correct (e.g., `fas fa-magic`)

### Need Help?
If you encounter issues:
1. Check the browser's developer console (F12) for errors
2. Verify all files are in the correct directory
3. Ensure all external resources (Tailwind CSS, Font Awesome) are loading properly

Remember to always make a backup of your files before making changes!