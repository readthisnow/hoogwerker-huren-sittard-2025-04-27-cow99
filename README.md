# Landing Page Maintenance Guide
## For Hoogwerker Huren Sittard Website

This guide provides detailed instructions for maintaining and customizing the Hoogwerker Huren Sittard landing page. Written for beginners with no prior coding experience.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the main navigation and logo. To update:

1. **Company Name/Logo**
```html
<a href="/" class="text-2xl font-bold text-blue-600">Hoogwerker Sittard</a>
```
- Replace "Hoogwerker Sittard" with your desired text
- The `text-2xl` class controls size
- `text-blue-600` controls the blue color

2. **Navigation Menu Items**
```html
<a href="#features" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Voordelen</a>
```
- Replace "Voordelen" with your desired text
- Keep the `href` matching your section IDs
- The `hover:text-blue-600` class creates the blue hover effect

### Hero Section
Located at the top of the page:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-6">
    Hoogwerker Huren Sittard
</h1>
```
- Update the heading text between the `<h1>` tags
- The classes control responsive sizing:
  - `text-4xl`: Mobile size
  - `md:text-5xl`: Tablet size
  - `lg:text-6xl`: Desktop size

### Promotional Text
```html
<p class="text-xl md:text-2xl text-blue-600 font-semibold mb-8">
    Tijdelijk 10% Korting op Alle Hoogwerkers
</p>
```
- Update the promotional text between the `<p>` tags
- Keep the classes to maintain styling

## Managing Links

### Navigation Menu Links
Current internal links in the navigation:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Voordelen</a>
    <a href="#benefits">Diensten</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
</div>
```

To update:
1. Locate the link you want to change
2. Modify the `href` attribute:
   - Use `#section-name` for internal page sections
   - Use full URLs for external links (e.g., `https://example.com`)

### Call-to-Action Buttons
Current CTA links:
```html
<a href="https://hansschuiling.nl" class="inline-block bg-blue-600 text-white px-8 py-4 rounded-lg">
    Direct Reserveren
</a>
```

To update:
1. Replace `https://hansschuiling.nl` with your desired URL
2. Update button text between the `<a>` tags
3. Keep all classes to maintain styling

## Adding Privacy and Terms Pages

### Footer Links Section
Current privacy and terms links:
```html
<ul class="space-y-2">
    <li><a href="#" class="hover:text-blue-400 transition-colors duration-300">Privacy Policy</a></li>
    <li><a href="#" class="hover:text-blue-400 transition-colors duration-300">Algemene Voorwaarden</a></li>
</ul>
```

To add proper links:
1. Create your privacy.html and terms.html files
2. Update the href attributes:
```html
<li><a href="privacy.html" class="hover:text-blue-400 transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-blue-400 transition-colors duration-300">Algemene Voorwaarden</a></li>
```

## Troubleshooting

### Common Issues

1. **Broken Internal Links**
- Ensure section IDs match the href attributes
- Section IDs should not contain spaces
- Example: `href="#contact"` must match `id="contact"`

2. **Styling Problems**
- Don't remove classes unless you're sure about their purpose
- Key class types:
  - `text-[size]`: Controls text size
  - `md:` or `lg:`: Responsive breakpoints
  - `hover:`: Hover effects
  - `transition-`: Animation effects

3. **Layout Issues**
- Maintain the container structure:
```html
<div class="container mx-auto px-4 sm:px-6 lg:px-8">
    <!-- Content here -->
</div>
```
- This ensures proper page width and margins

### Need Help?
- Check the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Verify all links work by clicking them
- Test the page on different screen sizes
- Keep backups before making changes

Remember: Always test your changes in a development environment before pushing to production.