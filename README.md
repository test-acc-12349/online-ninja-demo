# Online Ninja Landing Page - Maintenance Guide

This guide will help you maintain and customize the Online Ninja landing page. Whether you're new to web development or need a quick reference, follow these instructions to make updates while preserving the design integrity.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains your logo and navigation menu. To update:

```html
<!-- Located at the top of the page -->
<header class="fixed w-full z-50 bg-gray-900/95 backdrop-blur-sm border-b border-gray-800">
    <nav class="container mx-auto px-6 py-4">
        <!-- To change the logo text -->
        <a href="#" class="text-2xl font-bold text-white">
            <span>🥷</span>
            <span>Online Ninja</span> <!-- Edit this text -->
        </a>
```

**Key Tailwind Classes Explained:**
- `fixed`: Keeps header at top of page
- `w-full`: Full width
- `bg-gray-900/95`: Dark background with 95% opacity
- `backdrop-blur-sm`: Slight blur effect

### Hero Section
To modify the main headline and subtitle:

```html
<section class="relative min-h-screen">
    <div class="text-center max-w-4xl mx-auto">
        <!-- Main headline -->
        <h1 class="text-4xl md:text-6xl lg:text-7xl font-bold mb-8">
            10X Your Traffic With Ninja SEO 🥷
        </h1>
        <!-- Subtitle -->
        <p class="text-xl md:text-2xl text-gray-300 mb-12">
            Master the art of SEO with expert guidance
        </p>
    </div>
</section>
```

**Responsive Text Classes:**
- `text-4xl`: Base size for mobile
- `md:text-6xl`: Medium screens
- `lg:text-7xl`: Large screens

### Features Section
To update feature cards:

```html
<div class="bg-gray-900 rounded-xl p-8">
    <!-- Icon container -->
    <div class="w-16 h-16 bg-gradient-to-br from-purple-500 to-blue-500 rounded-full">
        <i class="fas fa-laptop-code text-2xl"></i>
    </div>
    <!-- Feature title -->
    <h3 class="text-xl font-bold mb-4">Online Learning</h3>
    <!-- Feature description -->
    <p class="text-gray-400">Access comprehensive SEO courses</p>
</div>
```

## Managing Links

### Navigation Menu Links
Current navigation links are located in the header:

```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-300 hover:text-white">Features</a>
    <a href="#benefits" class="text-gray-300 hover:text-white">Benefits</a>
    <a href="#faq" class="text-gray-300 hover:text-white">FAQ</a>
    <a href="#contact" class="text-gray-300 hover:text-white">Contact</a>
</div>
```

To update:
1. Locate the `href` attribute
2. Replace `#section-name` with your new link
3. Update the displayed text between `<a>` tags

### Call-to-Action Links
Current CTA buttons point to `https://ninja200.online`. To update:

```html
<a href="https://ninja200.online" class="bg-gradient-to-r from-purple-600 to-blue-600">
    Start Your Journey
</a>
```

Replace `https://ninja200.online` with your new URL.

## Adding Privacy and Terms Pages

### Step 1: Create New Pages
Create two new files in your website directory:
- `privacy.html`
- `terms.html`

### Step 2: Update Footer Links
Locate the footer section and update the legal links:

```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2 text-gray-400">
        <!-- Update these href attributes -->
        <li><a href="privacy.html" class="hover:text-white">Privacy Policy</a></li>
        <li><a href="terms.html" class="hover:text-white">Terms of Service</a></li>
    </ul>
</div>
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Layout on Mobile**
   - Check responsive classes (md:, lg:)
   - Ensure container div is present
   ```html
   <div class="container mx-auto px-6">
   ```

2. **Missing Icons**
   - Verify Font Awesome inclusion in header
   ```html
   <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
   ```

3. **Links Not Working**
   - Check for correct section IDs
   - Ensure href attributes match section IDs exactly
   - Section IDs should be unique

### Need Help?
- Double-check all changes against the original code
- Use browser inspector tools to identify styling issues
- Test on multiple devices and browsers
- Maintain backup copies before making changes

Remember: Always test your changes in a development environment before pushing to production.