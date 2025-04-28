# Landing Page Maintenance Guide
## For 101Headshots Corporate Photography Website

This guide provides detailed instructions for maintaining and customizing the 101Headshots landing page. Whether you're new to web development or need a quick reference, follow these step-by-step instructions.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Main Sections Overview
The landing page is divided into these key sections:
- Header (Navigation)
- Hero Section
- Features Section
- Benefits Section
- Contact Section
- Footer

### Updating Text Content

#### Header/Navigation
```html
<!-- Located at the top of the page -->
<a href="/" class="text-2xl font-bold">
    101Headshots  <!-- Change company name here -->
</a>
```

#### Hero Section
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold">
    Raymore, Missouri Corporate Headshot Photography Services  <!-- Update main heading -->
</h1>
<p class="text-xl md:text-2xl text-gray-300">
    Photos showcasing authentic personality behind Raymore's businesses.  <!-- Update subheading -->
</p>
```

#### Features & Benefits
Each card in these sections follows this structure:
```html
<div class="bg-gray-800 rounded-2xl p-8">
    <h3 class="text-xl font-semibold mb-4">
        Self Coaching  <!-- Update feature title -->
    </h3>
    <p class="text-gray-400">
        Expert guidance throughout your session...  <!-- Update feature description -->
    </p>
</div>
```

### Modifying Tailwind CSS Classes

#### Understanding Responsive Classes
- `md:` prefix = applies on medium screens (768px+)
- `lg:` prefix = applies on large screens (1024px+)

Example:
```html
class="text-4xl md:text-5xl lg:text-6xl"
<!-- text-4xl = default size -->
<!-- md:text-5xl = larger on medium screens -->
<!-- lg:text-6xl = largest on large screens -->
```

#### Common Tailwind Classes Used
- Spacing: `p-8` (padding), `m-4` (margin)
- Colors: `text-gray-400`, `bg-gray-800`
- Flex: `flex`, `items-center`, `justify-between`
- Grid: `grid`, `grid-cols-1`, `md:grid-cols-3`

## Fixing Broken Links

### Current Link Inventory
1. Navigation Menu Links:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#contact">Book Now</a>
```

2. Call-to-Action Links:
```html
<a href="https://www.101headshots.com">Schedule Your Session</a>
```

3. Contact Links:
```html
<a href="mailto:bryan@101headshots.com">Email Us</a>
```

### Updating Links
1. Internal Links (Same Page):
```html
<!-- Format: -->
<a href="#section-id">Link Text</a>

<!-- Example: -->
<a href="#features">Features</a>
```

2. External Links (Other Websites):
```html
<!-- Format: -->
<a href="https://full-website-url">Link Text</a>

<!-- Example: -->
<a href="https://www.101headshots.com">Visit Website</a>
```

## Linking Privacy and Terms Pages

### Adding Privacy Policy Link
Locate this section in the footer:
```html
<div>
    <h3 class="text-xl font-bold mb-4">Legal</h3>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-400 hover:text-white">Privacy Policy</a></li>
        <!-- Change from href="#" to: -->
        <li><a href="privacy.html" class="text-gray-400 hover:text-white">Privacy Policy</a></li>
    </ul>
</div>
```

### Adding Terms of Service Link
In the same footer section:
```html
<li><a href="#" class="text-gray-400 hover:text-white">Terms of Service</a></li>
<!-- Change to: -->
<li><a href="terms.html" class="text-gray-400 hover:text-white">Terms of Service</a></li>
```

### Maintaining Consistent Styling
When adding new links, copy these classes:
```html
class="text-gray-400 hover:text-white transition-colors duration-300"
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Internal Links**
   - Ensure section IDs match href attributes
   - Check for typos in IDs
   - IDs must be unique

2. **Responsive Design Issues**
   - Check mobile view using browser dev tools
   - Verify responsive classes (md:, lg:) are correct
   - Test on different screen sizes

3. **Gradient Text Not Showing**
   - Ensure these classes are present:
     ```html
     bg-gradient-to-r from-purple-400 to-pink-400 bg-clip-text text-transparent
     ```

### Need Help?
- Check Tailwind CSS documentation for class references
- Validate HTML at [W3C Validator](https://validator.w3.org/)
- Test all links before deploying changes

Remember to always backup your files before making changes, and test on multiple devices and browsers after updates.