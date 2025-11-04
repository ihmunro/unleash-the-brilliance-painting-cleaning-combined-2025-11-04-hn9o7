# Fresh Feel Painting & Cleaning - Landing Page Maintenance & Customization Guide

Welcome! This comprehensive guide will help you maintain and customize your Fresh Feel Painting & Cleaning landing page. Whether you're updating text, fixing links, or adding new pages, you'll find detailed, beginner-friendly instructions below.

---

## Table of Contents

1. [Quick Start Overview](#quick-start-overview)
2. [Section 1: Updating Text and Tailwind CSS Classes](#section-1-updating-text-and-tailwind-css-classes)
3. [Section 2: Fixing Broken Links](#section-2-fixing-broken-links)
4. [Section 3: Linking Privacy and Terms Pages](#section-3-linking-privacy-and-terms-pages)
5. [Troubleshooting Tips](#troubleshooting-tips)
6. [File Structure Best Practices](#file-structure-best-practices)

---

## Quick Start Overview

Your landing page (`index.html`) is built with:
- **HTML**: The structure and content of your page
- **Tailwind CSS**: A utility-first CSS framework for styling and responsive design
- **Font Awesome**: Icons for visual elements
- **Vanilla JavaScript**: For interactive features like mobile menu and FAQ accordion

### Key Sections in Your Landing Page:
1. **Header/Navigation** - Logo and menu links
2. **Hero Section** - Main headline and call-to-action buttons
3. **Features Section** - Three main service offerings
4. **Benefits Section** - Why choose Fresh Feel
5. **About Us Section** - Company story and mission
6. **Testimonials Section** - Client reviews
7. **FAQ Section** - Common questions and answers
8. **CTA Section** - Final call-to-action before footer
9. **Footer** - Contact info, links, and copyright

---

## Section 1: Updating Text and Tailwind CSS Classes

### Understanding the Basics

Before making changes, it's helpful to understand what you're looking at:

- **HTML Tags** look like this: `<h1>This is a heading</h1>`
- **Tailwind Classes** look like this: `class="text-3xl md:text-4xl font-bold"`
- **Text Content** is the actual words users see on your page

### 1.1 Updating Header/Logo Text

**Location**: Lines 49-54 in your HTML

**Current Code:**
```html
<div class="flex-shrink-0">
    <a href="#" class="text-2xl font-bold text-gray-900">
        <i class="fas fa-paint-brush text-blue-600 mr-2"></i>Fresh Feel
    </a>
</div>
```

**To Change the Logo Text:**

1. Find the words "Fresh Feel" in the header
2. Replace "Fresh Feel" with your desired text
3. Example:
```html
<i class="fas fa-paint-brush text-blue-600 mr-2"></i>Your Company Name
```

**Understanding the Classes:**
- `text-2xl` = Text size (2xl = extra large)
- `font-bold` = Bold text weight
- `text-gray-900` = Dark gray color
- `mr-2` = Margin-right (spacing to the right)

---

### 1.2 Updating Navigation Menu Links

**Location**: Lines 59-67 (Desktop Menu) and Lines 76-81 (Mobile Menu)

**Current Desktop Menu Code:**
```html
<div class="hidden md:flex items-center space-x-8">
    <a href="#features" class="text-gray-700 hover:text-blue-600 transition-colors duration-300 font-medium">Features</a>
    <a href="#benefits" class="text-gray-700 hover:text-blue-600 transition-colors duration-300 font-medium">Benefits</a>
    <a href="#testimonials" class="text-gray-700 hover:text-blue-600 transition-colors duration-300 font-medium">Testimonials</a>
    <a href="#faq" class="text-gray-700 hover:text-blue-600 transition-colors duration-300 font-medium">FAQ</a>
    <a href="https://www.freshfeelpaintingandcleaning.ca/" target="_blank" rel="noopener noreferrer" class="btn-primary bg-blue-600 text-white px-6 py-2 rounded-lg hover:bg-blue-700 shadow-md hover:shadow-lg font-medium">Get Started</a>
</div>
```

**To Add or Change Menu Items:**

1. **To rename a menu item:** Change the text between the `>` and `</a>`
   - Example: Change "Features" to "Our Services"
   ```html
   <a href="#features" class="...">Our Services</a>
   ```

2. **To change what a menu link points to:** Modify the `href="#"` part
   - Internal links (to sections on this page) use `#` followed by section ID
   - Example: `href="#features"` points to the Features section
   - External links use full URLs: `href="https://www.example.com"`

3. **To add a new menu item:** Copy an existing line and modify it
   ```html
   <a href="#portfolio" class="text-gray-700 hover:text-blue-600 transition-colors duration-300 font-medium">Portfolio</a>
   ```

**Important**: Keep the mobile menu (lines 76-81) synchronized with the desktop menu. Both should have the same links.

---

### 1.3 Updating Hero Section (Main Headline)

**Location**: Lines 98-120

**Current Hero Code:**
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-6 leading-tight tracking-tight">
    Unleash the Brilliance: Painting & Cleaning Combined
</h1>
<p class="text-lg md:text-xl text-gray-700 mb-8 leading-relaxed max-w-2xl mx-auto">
    Discover the ultimate transformation for any room. Our meticulous approach combines professional painting services with comprehensive cleaning, delivering spotless results and cohesive aesthetics that exceed your expectations.
</p>
```

**To Update the Hero Headline:**

1. Replace the text inside the `<h1>` tags
2. Keep the class structure intact
3. Example:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-6 leading-tight tracking-tight">
    Your New Headline Here
</h1>
```

**Understanding Responsive Classes:**
- `text-4xl` = Size on small screens (mobile)
- `md:text-5xl` = Size on medium screens (tablets)
- `lg:text-6xl` = Size on large screens (desktops)

**To Update the Hero Subtitle:**

Replace the text in the `<p>` tag below the headline:
```html
<p class="text-lg md:text-xl text-gray-700 mb-8 leading-relaxed max-w-2xl mx-auto">
    Your new subtitle text here
</p>
```

---

### 1.4 Updating Feature Cards

**Location**: Lines 141-230 (Features Section)

Your landing page has three feature cards. Here's the structure of one:

**Current Feature Card Code:**
```html
<div class="feature-card bg-gradient-to-br from-gray-50 to-white p-8 rounded-xl shadow-md hover:shadow-xl border border-gray-100">
    <div class="flex items-center justify-center w-16 h-16 bg-blue-100 rounded-lg mb-6">
        <i class="fas fa-tools text-blue-600 text-2xl"></i>
    </div>
    <h3 class="text-xl md:text-2xl font-bold text-gray-900 mb-4">Full-Service Renovation Support</h3>
    <p class="text-gray-700 leading-relaxed mb-4">
        Our expert team handles every aspect...
    </p>
    <ul class="space-y-2 text-sm text-gray-600">
        <li class="flex items-start">
            <i class="fas fa-check text-green-500 mr-3 mt-1 flex-shrink-0"></i>
            <span>Professional surface preparation and priming</span>
        </li>
        <!-- More list items... -->
    </ul>
</div>
```

**To Change Feature Card Content:**

1. **Change the icon**: Replace `fa-tools` with another Font Awesome icon
   - Visit [fontawesome.com](https://fontawesome.com/icons) to find icons
   - Example: `fa-paint-brush`, `fa-broom`, `fa-palette`
   ```html
   <i class="fas fa-paint-brush text-blue-600 text-2xl"></i>
   ```

2. **Change the icon background color**: Modify the color class
   - Current: `bg-blue-100` (light blue background)
   - Options: `bg-purple-100`, `bg-green-100`, `bg-red-100`
   ```html
   <div class="flex items-center justify-center w-16 h-16 bg-purple-100 rounded-lg mb-6">
   ```

3. **Change the icon color**: Modify `text-blue-600`
   - Options: `text-purple-600`, `text-green-600`, `text-red-600`

4. **Change the title**: Replace text in `<h3>` tags
   ```html
   <h3 class="text-xl md:text-2xl font-bold text-gray-900 mb-4">Your New Feature Title</h3>
   ```

5. **Change the description**: Replace the paragraph text
   ```html
   <p class="text-gray-700 leading-relaxed mb-4">
       Your new description here
   </p>
   ```

6. **Update the bullet points**: Modify each `<li>` item
   ```html
   <li class="flex items-start">
       <i class="fas fa-check text-green-500 mr-3 mt-1 flex-shrink-0"></i>
       <span>Your new bullet point text</span>
   </li>
   ```

---

### 1.5 Updating Benefits Section

**Location**: Lines 238-310

**Current Benefits Code Example:**
```html
<div class="bg-white p-8 rounded-xl shadow-md hover:shadow-lg transition-all duration-300 border border-blue-100">
    <div class="flex items-start">
        <div class="flex-shrink-0">
            <div class="flex items-center justify-center h-12 w-12 rounded-md bg-blue-500 text-white">
                <i class="fas fa-sparkles"></i>
            </div>
        </div>
        <div class="ml-4">
            <h3 class="text-xl font-bold text-gray-900 mb-2">Cohesive Aesthetics</h3>
            <p class="text-gray-700 leading-relaxed">
                Our integrated painting and cleaning approach...
            </p>
        </div>
    </div>
</div>
```

**To Update Benefit Items:**

1. **Change the icon**: Replace `fa-sparkles` with your choice
   - Example: `fa-clock`, `fa-check-circle`

2. **Change the icon background color**: Modify `bg-blue-500`
   - Options: `bg-purple-500`, `bg-green-500`

3. **Update the title**: Change text in `<h3>` tags

4. **Update the description**: Change the paragraph text

---

### 1.6 Updating Testimonials

**Location**: Lines 392-461

**Current Testimonial Code:**
```html
<div class="testimonial-card bg-white p-8 rounded-xl shadow-md border border-gray-100">
    <div class="flex items-center mb-4">
        <div class="flex-1">
            <h3 class="text-lg font-bold text-gray-900">Sarah Mitchell</h3>
            <p class="text-sm text-gray-600">Homeowner, Toronto</p>
        </div>
    </div>
    <div class="flex mb-4 text-yellow-400">
        <i class="fas fa-star"></i>
        <i class="fas fa-star"></i>
        <i class="fas fa-star"></i>
        <i class="fas fa-star"></i>
        <i class="fas fa-star"></i>
    </div>
    <p class="text-gray-700 leading-relaxed">
        "Fresh Feel transformed my entire living room..."
    </p>
</div>
```

**To Update Testimonials:**

1. **Change the customer name**: Replace "Sarah Mitchell"
2. **Change the title/location**: Replace "Homeowner, Toronto"
3. **Adjust star rating**: Remove or add `<i class="fas fa-star"></i>` lines
   - 5 stars = excellent
   - 4 stars = very good
   - 3 stars = good
4. **Update the testimonial text**: Replace the quoted text
   - Keep the quotation marks for clarity

---

### 1.7 Updating FAQ Questions and Answers

**Location**: Lines 486-597

**Current FAQ Item Code:**
```html
<div class="faq-item border border-gray-200 rounded-lg overflow-hidden shadow-sm hover:shadow-md transition-shadow duration-300">
    <button class="faq-question w-full px-6 py-4 md:px-8 md:py-5 bg-white hover:bg-gray-50 transition-colors duration-300 flex items-center justify-between cursor-pointer">
        <span class="text-lg font-semibold text-gray-900 text-left">How long does a typical painting project take?</span>
        <i class="faq-icon fas fa-chevron-down text-blue-600 flex-shrink-0 ml-4"></i>
    </button>
    <div class="faq-answer hidden bg-gray-50 px-6 py-4 md:px-8 md:py-5 border-t border-gray-200">
        <p class="text-gray-700 leading-relaxed">
            The timeline for your painting project depends on several factors...
        </p>
    </div>
</div>
```

**To Update FAQ Items:**

1. **Change the question**: Replace text in the `<span>` tag
   ```html
   <span class="text-lg font-semibold text-gray-900 text-left">Your new question?</span>
   ```

2. **Change the answer**: Replace the text in the `<p>` tag inside `.faq-answer`
   ```html
   <p class="text-gray-700 leading-relaxed">
       Your new answer here
   </p>
   ```

3. **Add a new FAQ item**: Copy the entire `<div class="faq-item">` block and paste it, then modify

---

### 1.8 Updating Footer Text

**Location**: Lines 637-729

**Current Footer Code Example:**
```html
<div>
    <h3 class="text-white font-bold text-lg mb-4 flex items-center">
        <i class="fas fa-paint-brush text-blue-400 mr-2"></i>Fresh Feel
    </h3>
    <p class="text-sm leading-relaxed mb-4">
        Professional painting and cleaning services that transform your space with precision and care.
    </p>
</div>
```

**To Update Footer Content:**

1. **Change company name**: Replace "Fresh Feel"
2. **Update company description**: Replace the paragraph text
3. **Update copyright year**: Find this line:
   ```html
   &copy; 2025 Fresh Feel Painting & Cleaning. All rights reserved.
   ```
   Change "2025" to current year and "Fresh Feel Painting & Cleaning" to your company name

---

### 1.9 Understanding Tailwind CSS Classes - Quick Reference

Here are the most common Tailwind classes used in your landing page:

| Class | Purpose | Example |
|-------|---------|---------|
| `text-xl`, `text-2xl`, `text-3xl` | Text size | `text-3xl` = large heading |
| `font-bold`, `font-semibold` | Text weight | `font-bold` = thick text |
| `text-gray-900`, `text-blue-600` | Text color | `text-blue-600` = blue text |
| `bg-white`, `bg-gray-50` | Background color | `bg-white` = white background |
| `px-6`, `py-4` | Padding (inside spacing) | `px-6` = horizontal padding |
| `mb-6`, `mt-4` | Margin (outside spacing) | `mb-6` = bottom margin |
| `rounded-lg`, `rounded-xl` | Rounded corners | `rounded-xl` = very rounded |
| `shadow-md`, `shadow-lg` | Drop shadow | `shadow-lg` = large shadow |
| `md:`, `lg:` | Responsive prefix | `md:text-5xl` = size on medium+ screens |
| `hover:` | Hover effect | `hover:text-blue-600` = blue on hover |

---

### 1.10 Responsive Design Explained

Your landing page uses **mobile-first design**, meaning it looks good on phones first, then adapts to larger screens.

**Breakpoints:**
- **Mobile**: Default (no prefix) - applies to all screen sizes
- **Tablet**: `md:` prefix - applies to medium screens and up (768px+)
- **Desktop**: `lg:` prefix - applies to large screens and up (1024px+)

**Example:**
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl">
```
- On mobile: `text-4xl` (size 36px)
- On tablet: `md:text-5xl` (size 48px)
- On desktop: `lg:text-6xl` (size 60px)

**When updating text sizes, always include all three breakpoints for consistency.**

---

## Section 2: Fixing Broken Links

### 2.1 Identifying All Links in Your Landing Page

Your landing page contains several types of links:

1. **Navigation links** (point to sections on this page)
2. **External links** (point to your website)
3. **Social media links** (point to social profiles)
4. **Email links** (open email client)
5. **Policy links** (point to policy pages - currently broken)

---

### 2.2 Navigation Links (Internal)

**What they are**: Links that point to different sections of your landing page using `#` (anchor links)

**Current Navigation Links:**

| Link Text | Current href | Points To |
|-----------|--------------|-----------|
| Features | `#features` | Features Section |
| Benefits | `#benefits` | Benefits Section |
| Testimonials | `#testimonials` | Testimonials Section |
| FAQ | `#faq` | FAQ Section |

**Locations:**
- Desktop menu: Lines 59-67
- Mobile menu: Lines 76-81

**How They Work:**
- The `href="#features"` points to an element with `id="features"`
- When clicked, the page smoothly scrolls to that section
- These links are already working correctly if the section IDs match

**To Verify Navigation Links Are Working:**

1. Find each section in your HTML:
   - Line 139: `<section id="features">`
   - Line 239: `<section id="benefits">`
   - Line 319: `<section id="testimonials">`
   - Line 385: `<section id="faq">`

2. Confirm the navigation links point to these IDs (they already do)

3. Test by clicking each menu item - the page should scroll to that section

**If a navigation link isn't working:**

1. Check the `href` attribute matches the section `id` exactly
2. Ensure there are no typos
3. Example fix:
   ```html
   <!-- In navigation -->
   <a href="#testimonials" ...>Testimonials</a>
   
   <!-- In page -->
   <section id="testimonials" ...>
   ```

---

### 2.3 External Links (Your Website)

**Current External Links:**

Your landing page links to your main website in several places:
- Line 69: "Get Started" button in desktop menu
- Line 82: "Get Started" button in mobile menu
- Line 122: "Start Your Transformation" button in hero
- Line 631: "Get Your Free Consultation" button in CTA section

**Current URL:**
```
https://www.freshfeelpaintingandcleaning.ca/
```

**To Update External Links:**

1. **Find all instances** of `https://www.freshfeelpaintingandcleaning.ca/`
2. **Replace with your actual website URL**
3. **Use Find & Replace** (easiest method):
   - Press `Ctrl+H` (Windows) or `Cmd+H` (Mac)
   - Find: `https://www.freshfeelpaintingandcleaning.ca/`
   - Replace with: `https://www.yourwebsite.com/`
   - Click "Replace All"

**Example:**
```html
<!-- Before -->
<a href="https://www.freshfeelpaintingandcleaning.ca/" target="_blank">Get Started</a>

<!-- After -->
<a href="https://www.yourwebsite.com/" target="_blank">Get Started</a>
```

**Important Attributes Explained:**
- `target="_blank"` = Opens link in new tab (good for external links)
- `rel="noopener noreferrer"` = Security best practice for external links

---

### 2.4 Email Links

**Current Email Link:**

Your landing page has email links in:
- Line 628: Email button in CTA section
- Line 715: Email in footer

**Current Email:**
```
iainhmunro@gmail.com
```

**To Update Email Links:**

1. **Find all instances** of `iainhmunro@gmail.com`
2. **Replace with your email address**
3. **Use Find & Replace**:
   - Find: `iainhmunro@gmail.com`
   - Replace with: `your-email@yourdomain.com`
   - Click "Replace All"

**Email Link Format:**
```html
<a href="mailto:your-email@yourdomain.com">Email Us</a>
```

**How it works:**
- `mailto:` tells the browser to open the user's email client
- When clicked, it creates a new email addressed to your email
- Users can then type their message and send

---

### 2.5 Social Media Links

**Location**: Lines 700-713 in footer

**Current Social Media Code:**
```html
<div class="flex space-x-4">
    <a href="#" class="text-gray-400 hover:text-blue-400 transition-colors duration-300" aria-label="Facebook">
        <i class="fab fa-facebook-f"></i>
    </a>
    <a href="#" class="text-gray-400 hover:text-blue-400 transition-colors duration-300" aria-label="Instagram">
        <i class="fab fa-instagram"></i>
    </a>
    <a href="#" class="text-gray-400 hover:text-blue-400 transition-colors duration-300" aria-label="Twitter">
        <i class="fab fa-twitter"></i>
    </a>
    <a href="#" class="text-gray-400 hover:text-blue-400 transition-colors duration-300" aria-label="LinkedIn">
        <i class="fab fa-linkedin-in"></i>
    </a>
</div>
```

**To Update Social Media Links:**

1. **Facebook**: Replace `href="#"` with your Facebook page URL
   ```html
   <a href="https://www.facebook.com/yourpage" class="..." aria-label="Facebook">
   ```

2. **Instagram**: Replace `href="#"` with your Instagram profile URL
   ```html
   <a href="https://www.instagram.com/yourprofile" class="..." aria-label="Instagram">
   ```

3. **Twitter**: Replace `href="#"` with your Twitter profile URL
   ```html
   <a href="https://www.twitter.com/yourprofile" class="..." aria-label="Twitter">
   ```

4. **LinkedIn**: Replace `href="#"` with your LinkedIn company page URL
   ```html
   <a href="https://www.linkedin.com/company/yourcompany" class="..." aria-label="LinkedIn">
   ```

**To Find Your Social Media URLs:**
- **Facebook**: Go to your page, copy the URL from the address bar
- **Instagram**: Go to your profile, copy the URL from the address bar
- **Twitter**: Go to your profile, copy the URL from the address bar
- **LinkedIn**: Go to your company page, copy the URL from the address bar

**Important**: Always include `https://` at the beginning of the URL

---

### 2.6 Policy and Blog Links

**Location**: Lines 720-722 in footer

**Current Code:**
```html
<a href="privacy.html" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">Privacy Policy</a>
<a href="terms.html" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">Terms of Service</a>
<a href="blog.html" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">Blog</a>
```

**Status**: These links are currently broken because the files don't exist yet.

**To Fix These Links**: See **Section 3: Linking Privacy and Terms Pages** below.

---

### 2.7 Logo Link

**Location**: Line 51

**Current Code:**
```html
<a href="#" class="text-2xl font-bold text-gray-900">
    <i class="fas fa-paint-brush text-blue-600 mr-2"></i>Fresh Feel
</a>
```

**To Fix the Logo Link:**

The logo currently links to `#` (nowhere). Update it to link to your main website:

```html
<a href="https://www.yourwebsite.com/" class="text-2xl font-bold text-gray-900">
    <i class="fas fa-paint-brush text-blue-600 mr-2"></i>Fresh Feel
</a>
```

Or, if this is your main website, you can link to the home page:
```html
<a href="index.html" class="text-2xl font-bold text-gray-900">
    <i class="fas fa-paint-brush text-blue-600 mr-2"></i>Fresh Feel
</a>
```

---

### 2.8 Link Verification Checklist

Use this checklist to verify all links are working:

- [ ] Navigation menu links scroll to correct sections
- [ ] "Get Started" buttons link to your website
- [ ] Email links open your email client
- [ ] Social media links point to your profiles
- [ ] Logo links to home/main website
- [ ] Privacy Policy link works (see Section 3)
- [ ] Terms of Service link works (see Section 3)
- [ ] Blog link works (see Section 3)

---

## Section 3: Linking Privacy and Terms Pages

### 3.1 Understanding What We're Creating

You need to create two new HTML pages:
1. **privacy.html** - Your privacy policy page
2. **terms.html** - Your terms of service page

These pages will be linked from your footer (currently broken links).

---

### 3.2 File Structure Setup

**What you need:**

```
your-project-folder/
├── index.html          (your main landing page - already exists)
├── privacy.html        (new file you'll create)
├── terms.html          (new file you'll create)
└── (optional) blog.html (if you want a blog page)
```

**Important**: All these files must be in the same folder for the links to work.

---

### 3.3 Step-by-Step: Creating the Privacy Policy Page

**Step 1: Create a new file**

1. Open your code editor
2. Create a new file
3. Save it as `privacy.html` in the same folder as `index.html`

**Step 2: Add basic HTML structure**

Copy and paste this template into `privacy.html`:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Privacy Policy - Fresh Feel Painting & Cleaning">
    <title>Privacy Policy - Fresh Feel Painting & Cleaning</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        html {
            scroll-behavior: smooth;
        }
    </style>
</head>
<body class="bg-white text-gray-900">
    <!-- Header & Navigation -->
    <header class="sticky top-0 z-50 bg-white shadow-md">
        <nav class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex justify-between items-center h-20">
                <div class="flex-shrink-0">
                    <a href="index.html" class="text-2xl font-bold text-gray-900">
                        <i class="fas fa-paint-brush text-blue-600 mr-2"></i>Fresh Feel
                    </a>
                </div>
                <div class="hidden md:flex items-center space-x-8">
                    <a href="index.html" class="text-gray-700 hover:text-blue-600 transition-colors duration-300 font-medium">Home</a>
                </div>
                <button class="mobile-menu-button md:hidden text-gray-700 hover:text-blue-600 transition-colors duration-300">
                    <i class="fas fa-bars text-2xl"></i>
                </button>
            </div>
        </nav>
    </header>

    <!-- Main Content -->
    <main class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8 py-16 md:py-24">
        <h1 class="text-4xl md:text-5xl font-bold text-gray-900 mb-8">Privacy Policy</h1>
        
        <div class="prose prose-lg text-gray-700 space-y-6">
            <section class="mb-8">
                <h2 class="text-2xl font-bold text-gray-900 mb-4">Introduction</h2>
                <p>Fresh Feel Painting & Cleaning ("we," "us," "our," or "Company") is committed to protecting your privacy. This Privacy Policy explains how we collect, use, disclose, and safeguard your information when you visit our website.</p>
            </section>

            <section class="mb-8">
                <h2 class="text-2xl font-bold text-gray-900 mb-4">Information We Collect</h2>
                <p>We may collect information about you in a variety of ways. The information we may collect on the Site includes:</p>
                <ul class="list-disc list-inside space-y-2">
                    <li>Personal Data: Personally identifiable information, such as your name, shipping address, email address, and telephone number, that you voluntarily give to us when you register with the Site or when you choose to participate in various activities related to the Site.</li>
                    <li>Financial Data: Financial information, such as data related to your payment method (e.g., valid credit card number, card brand, expiration date) that we may collect when you purchase, order, return, exchange, or request information about our services from the Site.</li>
                    <li>Data From Contests, Giveaways, and Surveys: Personal and other information you may provide when entering contests or giveaways and/or responding to surveys.</li>
                </ul>
            </section>

            <section class="mb-8">
                <h2 class="text-2xl font-bold text-gray-900 mb-4">Use of Your Information</h2>
                <p>Having accurate information about you permits us to provide you with a smooth, efficient, and customized experience. Specifically, we may use information collected about you via the Site to:</p>
                <ul class="list-disc list-inside space-y-2">
                    <li>Generate a personal profile about you so that future visits to the Site will be personalized as possible.</li>
                    <li>Increase the efficiency and operation of the Site.</li>
                    <li>Monitor and analyze usage and trends to improve your experience with the Site.</li>
                    <li>Notify you of updates to the Site.</li>
                    <li>Offer new products, services, and/or recommendations to you.</li>
                </ul>
            </section>

            <section class="mb-8">
                <h2 class="text-2xl font-bold text-gray-900 mb-4">Disclosure of Your Information</h2>
                <p>We may share your information in the following situations:</p>
                <ul class="list-disc list-inside space-y-2">
                    <li><strong>By Law or to Protect Rights:</strong> If we believe the release of information about you is necessary to comply with the law, enforce our Site policies, or protect ours or others' rights, property, and safety.</li>
                    <li><strong>Third-Party Service Providers:</strong> We may share your information with third parties that perform services for us or on our behalf, including payment processing, data analysis, email delivery, hosting services, customer service, and marketing assistance.</li>
                </ul>
            </section>

            <section class="mb-8">
                <h2 class="text-2xl font-bold text-gray-900 mb-4">Security of Your Information</h2>
                <p>We use administrative, technical, and physical security measures to protect your personal information. However, perfect security is impossible to guarantee.</p>
            </section>

            <section class="mb-8">
                <h2 class="text-2xl font-bold text-gray-900 mb-4">Contact Us</h2>
                <p>If you have questions or comments about this Privacy Policy, please contact us at:</p>
                <p>
                    Email: <a href="mailto:iainhmunro@gmail.com" class="text-blue-600 hover:text-blue-700">iainhmunro@gmail.com</a>
                </p>
            </section>
        </div>
    </main>

    <!-- Footer -->
    <footer class="bg-gray-900 text-gray-300 mt-16">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-12">
            <div class="text-center">
                <p class="text-sm text-gray-400">
                    &copy; 2025 Fresh Feel Painting & Cleaning. All rights reserved.
                </p>
            </div>
        </div>
    </footer>
</body>
</html>
```

**Step 3: Customize the privacy policy**

Replace the placeholder text with your actual privacy policy. Key sections to update:
- Introduction
- Information We Collect
- Use of Your Information
- Disclosure of Your Information
- Security of Your Information
- Contact Us (update email address)

---

### 3.4 Step-by-Step: Creating the Terms of Service Page

**Step 1: Create a new file**

1. Open your code editor
2. Create a new file
3. Save it as `terms.html` in the same folder as `index.html`

**Step 2: Add basic HTML structure**

Copy and paste this template into `terms.html`:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Terms of Service - Fresh Feel Painting & Cleaning">
    <title>Terms of Service - Fresh Feel Painting & Cleaning</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        html {
            scroll-behavior: smooth;
        }
    </style>
</head>
<body class="bg-white text-gray-900">
    <!-- Header & Navigation -->
    <header class="sticky top-0 z-50 bg-white shadow-md">
        <nav class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex justify-between items-center h-20">
                <div class="flex-shrink-0">
                    <a href="index.html" class="text-2xl font-bold text-gray-900">
                        <i class="fas fa-paint-brush text-blue-600 mr-2"></i>Fresh Feel
                    </a>
                </div>
                <div class="hidden md:flex items-center space-x-8">
                    <a href="index.html" class="text-gray-700 hover:text-blue-600 transition-colors duration-300 font-medium">Home</a>
                </div>
                <button class="mobile-menu-button md:hidden text-gray-700 hover:text-blue-600 transition-colors duration-300">
                    <i class="fas fa-bars text-2xl"></i>
                </button>
            </div>
        </nav>
    </header>

    <!-- Main Content -->
    <main class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8 py-16 md:py-24">
        <h1 class="text-4xl md:text-5xl font-bold text-gray-900 mb-8">Terms of Service</h1>
        
        <div class="prose prose-lg text-gray-700 space-y-6">
            <section class="mb-8">
                <h2 class="text-2xl font-bold text-gray-900 mb-4">Agreement to Terms</h2>
                <p>These Terms of Service ("Terms") constitute a legally binding agreement made between you, whether personally or on behalf of an entity ("you" or "User") and Fresh Feel Painting & Cleaning ("we," "us," "our," or "Company"), concerning your access to and use of the website and all related applications, software, tools, and services available through the website (the "Site").</p>
            </section>

            <section class="mb-8">
                <h2 class="text-2xl font-bold text-gray-900 mb-4">Intellectual Property Rights</h2>
                <p>Unless otherwise indicated, the Site is our proprietary property and all source code, databases, functionality, software, website designs, audio, video, text, photographs, and graphics on the Site (collectively, the "Content") and the trademarks, service marks, and logos contained therein (the "Marks") are owned or controlled by us, licensed to us, or otherwise used by us in accordance with applicable law.</p>
            </section>

            <section class="mb-8">
                <h2 class="text-2xl font-bold text-gray-900 mb-4">User Representations</h2>
                <p>By using the Site, you represent and warrant that:</p>
                <ul class="list-disc list-inside space-y-2">
                    <li>All registration information you submit is true, accurate, and current.</li>
                    <li>You will maintain the confidentiality of your password and account information.</li>
                    <li>You have the legal capacity and you agree to comply with these Terms of Service.</li>
                    <li>You are not a minor in the jurisdiction in which you reside.</li>
                </ul>
            </section>

            <section class="mb-8">
                <h2 class="text-2xl font-bold text-gray-900 mb-4">User Prohibited Behavior</h2>
                <p>You may not access or use the Site for any purpose other than that for which we make the Site available. The Site may not be used in connection with any commercial endeavors except those specifically endorsed or approved by us.</p>
            </section>

            <section class="mb-8">
                <h2 class="text-2xl font-bold text-gray-900 mb-4">Disclaimer of Warranties</h2>
                <p>The Site is provided on an "AS-IS" and "AS AVAILABLE" basis. We make no warranties, expressed or implied, regarding the Site. To the fullest extent permissible pursuant to applicable law, we disclaim all warranties, expressed or implied, including, but not limited to, implied warranties of merchantability and fitness for a particular purpose.</p>
            </section>

            <section class="mb-8">
                <h2 class="text-2xl font-bold text-gray-900 mb-4">Limitation of Liability</h2>
                <p>In no event shall the Company or its suppliers be liable for any damages (including, without limitation, damages for loss of data or profit, or due to business interruption) arising out of the use or inability to use the materials on the Site.</p>
            </section>

            <section class="mb-8">
                <h2 class="text-2xl font-bold text-gray-900 mb-4">Indemnification</h2>
                <p>You agree to defend, indemnify, and hold us harmless, including our subsidiaries, affiliates, and all of our respective officers, agents, partners, and employees, from and against any loss, damage, liability, claim, or demand, including reasonable attorneys' fees and expenses, made by any third party due to or arising out of your use of the Site or violation of these Terms of Service.</p>
            </section>

            <section class="mb-8">
                <h2 class="text-2xl font-bold text-gray-900 mb-4">Contact Us</h2>
                <p>If you have questions or comments about these Terms of Service, please contact us at:</p>
                <p>
                    Email: <a href="mailto:iainhmunro@gmail.com" class="text-blue-600 hover:text-blue-700">iainhmunro@gmail.com</a>
                </p>
            </section>
        </div>
    </main>

    <!-- Footer -->
    <footer class="bg-gray-900 text-gray-300 mt-16">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-12">
            <div class="text-center">
                <p class="text-sm text-gray-400">
                    &copy; 2025 Fresh Feel Painting & Cleaning. All rights reserved.
                </p>
            </div>
        </div>
    </footer>
</body>
</html>
```

**Step 3: Customize the terms of service**

Replace the placeholder text with your actual terms. Key sections to update:
- Agreement to Terms
- Intellectual Property Rights
- User Representations
- User Prohibited Behavior
- Disclaimer of Warranties
- Limitation of Liability
- Indemnification
- Contact Us (update email address)

---

### 3.5 Verifying the Links in Your Landing Page

Once you've created `privacy.html` and `terms.html`, the footer links in `index.html` should work automatically.

**Current footer links (Lines 720-722 in index.html):**
```html
<a href="privacy.html" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">Privacy Policy</a>
<a href="terms.html" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">Terms of Service</a>
<a href="blog.html" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">Blog</a>
```

**To verify:**
1. Open `index.html` in your browser
2. Scroll to the footer
3. Click "Privacy Policy" - should open privacy.html
4. Click "Terms of Service" - should open terms.html

**If links aren't working:**
- Verify all three files are in the same folder
- Check file names match exactly (case-sensitive on some systems)
- Ensure you saved the files with correct extensions (.html)

---

### 3.6 Creating a Blog Page (Optional)

The footer also links to `blog.html`, which doesn't exist yet. Here's how to create it:

**Step 1: Create blog.html**

Save this template as `blog.html`:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Blog - Fresh Feel Painting & Cleaning">
    <title>Blog - Fresh Feel Painting & Cleaning</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        html {
            scroll-behavior: smooth;
        }
    </style>
</head>
<body class="bg-white text-gray-900">
    <!-- Header & Navigation -->
    <header class="sticky top-0 z-50 bg-white shadow-md">
        <nav class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex justify-between items-center h-20">
                <div class="flex-shrink-0">
                    <a href="index.html" class="text-2xl font-bold text-gray-900">
                        <i class="fas fa-paint-brush text-blue-600 mr-2"></i>Fresh Feel
                    </a>
                </div>
                <div class="hidden md:flex items-center space-x-8">
                    <a href="index.html" class="text-gray-700 hover:text-blue-600 transition-colors duration-300 font-medium">Home</a>
                </div>
                <button class="mobile-menu-button md:hidden text-gray-700 hover:text-blue-600 transition-colors duration-300">
                    <i class="fas fa-bars text-2xl"></i>
                </button>
            </div>
        </nav>
    </header>

    <!-- Main Content -->
    <main class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8 py-16 md:py-24">
        <h1 class="text-4xl md:text-5xl font-bold text-gray-900 mb-12">Blog</h1>
        
        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
            <!-- Blog Post 1 -->
            <article class="bg-white rounded-lg shadow-md overflow-hidden hover:shadow-lg transition-shadow duration-300">
                <img src="https://images.unsplash.com/photo-1581092918056-0c4c3acd3789?w=400&h=250&fit=crop" alt="Painting tips" class="w-full h-48 object-cover">
                <div class="p-6">
                    <h2 class="text-xl font-bold text-gray-900 mb-2">How to Choose the Perfect Paint Color</h2>
                    <p class="text-gray-600 mb-4">Learn the key factors to consider when selecting paint colors for your home or office space.</p>
                    <a href="#" class="text-blue-600 hover:text-blue-700 font-semibold">Read More →</a>
                </div>
            </article>

            <!-- Blog Post 2 -->
            <article class="bg-white rounded-lg shadow-md overflow-hidden hover:shadow-lg transition-shadow duration-300">
                <img src="https://images.unsplash.com/photo-1552321554-5fefe8c9ef14?w=400&h=250&fit=crop" alt="Painting preparation" class="w-full h-48 object-cover">
                <div class="p-6">
                    <h2 class="text-xl font-bold text-gray-900 mb-2">Preparation is Key: Pre-Painting Tips</h2>
                    <p class="text-gray-600 mb-4">Discover how proper preparation ensures a flawless paint job that lasts for years.</p>
                    <a href="#" class="text-blue-600 hover:text-blue-700 font-semibold">Read More →</a>
                </div>
            </article>

            <!-- Blog Post 3 -->
            <article class="bg-white rounded-lg shadow-md overflow-hidden hover:shadow-lg transition-shadow duration-300">
                <img src="https://images.unsplash.com/photo-1581092918056-0c4c3acd3789?w=400&h=250&fit=crop" alt="Cleaning tips" class="w-full h-48 object-cover">
                <div class="p-6">
                    <h2 class="text-xl font-bold text-gray-900 mb-2">Post-Painting Cleanup: What to Expect</h2>
                    <p class="text-gray-600 mb-4">Learn about our thorough cleanup process that leaves your space spotless.</p>
                    <a href="#" class="text-blue-600 hover:text-blue-700 font-semibold">Read More →</a>
                </div>
            </article>
        </div>
    </main>

    <!-- Footer -->
    <footer class="bg-gray-900 text-gray-300 mt-16">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-12">
            <div class="text-center">
                <p class="text-sm text-gray-400">
                    &copy; 2025 Fresh Feel Painting & Cleaning. All rights reserved.
                </p>
            </div>
        </div>
    </footer>
</body>
</html>
```

Now all footer links will work!

---

### 3.7 Summary of File Structure After Creating Policy Pages

After completing this section, your project folder should look like this:

```
your-project-folder/
├── index.html          ← Your main landing page
├── privacy.html        ← New privacy policy page
├── terms.html          ← New terms of service page
└── blog.html           ← Optional blog page
```

All links in the footer will now work correctly:
- ✅ Privacy Policy link → Opens privacy.html
- ✅ Terms of Service link → Opens terms.html
- ✅ Blog link → Opens blog.html

---

## Troubleshooting Tips

### Issue 1: Links Not Working

**Problem**: Clicked a link but nothing happened or got a 404 error

**Solutions**:
1. **Check file names**: Ensure file names are spelled correctly and match exactly
   - `privacy.html` (not `Privacy.html` or `privacy.HTML`)
   - On Mac/Linux, file names are case-sensitive
   
2. **Verify file location**: All HTML files must be in the same folder
   - ❌ Wrong: `index.html` in folder A, `privacy.html` in folder B
   - ✅ Correct: All files in the same folder

3. **Check href attributes**: Verify the path is correct
   ```html
   <!-- Correct for same folder -->
   <a href="privacy.html">Privacy Policy</a>
   
   <!-- Wrong -->
   <a href="/privacy.html">Privacy Policy</a>
   <a href="./privacy.html">Privacy Policy</a>
   ```

4. **Test in browser**: Open the HTML file directly in your browser
   - Don't rely on previews in your code editor

---

### Issue 2: Styling Looks Wrong After Editing

**Problem**: Text is too big/small or colors are wrong

**Solutions**:
1. **Don't delete class attributes**: Always keep the `class="..."` part
   ```html
   <!-- Wrong - removed classes -->
   <h1>Your Headline</h1>
   
   <!-- Correct - kept classes -->
   <h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-6">Your Headline</h1>
   ```

2. **Check for typos in class names**: Tailwind classes must be exact
   ```html
   <!-- Wrong -->
   <h1 class="text-4xl md:text-5xl lg:text-6xl font-bold">
   
   <!-- Correct -->
   <h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900">
   ```

3. **Use Find & Replace carefully**: When replacing text, don't accidentally delete HTML tags
   - Use `Ctrl+H` (Find & Replace) carefully
   - Preview changes before replacing all

---

### Issue 3: Mobile Menu Not Working

**Problem**: Mobile menu button doesn't open/close

**Solutions**:
1. **Check JavaScript is intact**: Don't modify the `<script>` section at the bottom
2. **Verify button HTML**: The mobile menu button should have class `mobile-menu-button`
   ```html
   <button class="mobile-menu-button md:hidden ...">
   ```

3. **Check mobile menu div**: Should have class `mobile-menu`
   ```html
   <div class="mobile-menu hidden md:hidden pb-4">
   ```

---

### Issue 4: External Links Opening in Same Tab

**Problem**: Clicking "Get Started" opens your website in the same tab, losing the landing page

**Solution**: Add `target="_blank"` to external links
```html
<!-- Before - opens in same tab -->
<a href="https://www.yourwebsite.com/">Get Started</a>

<!-- After - opens in new tab -->
<a href="https://www.yourwebsite.com/" target="_blank" rel="noopener noreferrer">Get Started</a>
```

---

### Issue 5: Email Link Not Working

**Problem**: Clicking email link does nothing

**Solutions**:
1. **Check email format**: Should start with `mailto:`
   ```html
   <!-- Correct -->
   <a href="mailto:your-email@yourdomain.com">Email Us</a>
   
   <!-- Wrong -->
   <a href="your-email@yourdomain.com">Email Us</a>
   ```

2. **Verify email address**: Check for typos
   ```html
   <!-- Wrong - missing @ -->
   <a href="mailto:your-emailyourdomain.com">Email Us</a>
   
   <!-- Correct -->
   <a href="mailto:your-email@yourdomain.com">Email Us</a>
   ```

---

### Issue 6: Page Not Displaying Correctly

**Problem**: Page looks broken or incomplete

**Solutions**:
1. **Hard refresh browser**: Press `Ctrl+Shift+R` (Windows) or `Cmd+Shift+R` (Mac)
   - This clears the cache and reloads the page

2. **Check for unclosed tags**: All opening tags need closing tags
   ```html
   <!-- Wrong - missing closing tag -->
   <div class="...">
       <p>Content</p>
   
   <!-- Correct -->
   <div class="...">
       <p>Content</p>
   </div>
   ```

3. **Verify Tailwind CDN**: Make sure this line is in your `<head>`:
   ```html
   <script src="https://cdn.tailwindcss.com"></script>
   ```

---

### Issue 7: FAQ Accordion Not Expanding

**Problem**: Clicking FAQ questions doesn't reveal answers

**Solutions**:
1. **Check JavaScript**: Don't modify the FAQ JavaScript code at the bottom
2. **Verify HTML structure**: Each FAQ item needs:
   - `<div class="faq-item">` wrapper
   - `<button class="faq-question">` for the question
   - `<div class="faq-answer hidden">` for the answer

3. **Test in different browser**: Try Chrome, Firefox, or Safari

---

### Issue 8: Colors Not Updating

**Problem**: Changed color class but color didn't change

**Solutions**:
1. **Use correct Tailwind color names**:
   ```html
   <!-- Correct color classes -->
   text-blue-600, text-purple-600, text-green-600, text-red-600
   
   <!-- Wrong -->
   text-blue, text-purple, text-green (missing number)
   ```

2. **Ensure you're in the right element**: Make sure you're changing the right element
   ```html
   <!-- Icon color -->
   <i class="fas fa-tools text-blue-600"></i>
   
   <!-- Background color -->
   <div class="bg-blue-100">
   
   <!-- Text color -->
   <h3 class="text-gray-900">
   ```

3. **Hard refresh**: Browser cache might be showing old colors

---

### Issue 9: Text Too Large or Too Small

**Problem**: Headline or body text size is wrong

**Solutions**:
1. **Check responsive classes**: Update all three breakpoints
   ```html
   <!-- Correct - includes all sizes -->
   <h1 class="text-4xl md:text-5xl lg:text-6xl">
   
   <!-- Wrong - missing sizes -->
   <h1 class="text-4xl">
   ```

2. **Reference size guide**:
   - `text-sm` = 14px (small text)
   - `text-base` = 16px (normal text)
   - `text-lg` = 18px (large text)
   - `text-xl` = 20px (extra large)
   - `text-2xl` = 24px (2x large)
   - `text-3xl` = 30px (3x large)
   - `text-4xl` = 36px (4x large)
   - `text-5xl` = 48px (5x large)
   - `text-6xl` = 60px (6x large)

---

### Issue 10: Spacing Looks Wrong

**Problem**: Too much or too little space between elements

**Solutions**:
1. **Understand spacing classes**:
   - `mb-4` = 16px margin below
   - `mt-4` = 16px margin above
   - `px-6` = 24px padding left and right
   - `py-4` = 16px padding top and bottom

2. **Adjust spacing**:
   ```html
   <!-- Decrease space -->
   <div class="mb-4">  <!-- was mb-8 -->
   
   <!-- Increase space -->
   <div class="mb-12">  <!-- was mb-6 -->
   ```

3. **Number reference**:
   - `1` = 4px
   - `2` = 8px
   - `3` = 12px
   - `4` = 16px
   - `6` = 24px
   - `8` = 32px
   - `12` = 48px
   - `16` = 64px

---

## File Structure Best Practices

### 3.1 Recommended Project Organization

As your website grows, organize files like this:

```
fresh-feel-website/
├── index.html              ← Main landing page
├── privacy.html            ← Privacy policy
├── terms.html              ← Terms of service
├── blog.html               ← Blog page
├── css/
│   └── custom.css          ← Custom CSS (optional)
├── js/
│   └── custom.js           ← Custom JavaScript (optional)
├── images/
│   ├── logo.png            ← Your logo
│   ├── hero.jpg            ← Hero section image
│   └── testimonial-1.jpg   ← Client photos
└── README.md               ← Documentation
```

---

### 3.2 Naming Conventions

**File Names:**
- Use lowercase letters: `privacy.html` (not `Privacy.html`)
- Use hyphens for spaces: `about-us.html` (not `about_us.html`)
- Be descriptive: `color-consultation-guide.html` (not `page1.html`)

**Folder Names:**
- Use lowercase: `images/`, `css/`, `js/`
- Use plural for collections: `images/`, `pages/`
- Avoid spaces: `my-assets/` (not `my assets/`)

---

### 3.3 Backing Up Your Files

**Important**: Always keep backups of your HTML files

**Simple Backup Method:**
1. Create a folder called `backups/`
2. Copy your HTML files to this folder
3. Add the date to backup files: `index-2025-01-15.html`

**Using Git (Advanced):**
```bash
# Initialize git repository
git init

# Add all files
git add .

# Create backup snapshot
git commit -m "Initial landing page setup"
```

---

### 3.4 Version Control Notes

When making changes:
1. **Make one change at a time**: Easier to debug if something breaks
2. **Test after each change**: Verify it works before moving on
3. **Keep old versions**: Don't delete files until you're sure new version works
4. **Document changes**: Write notes about what you changed

Example:
```
2025-01-15: Updated hero headline and feature card colors
2025-01-14: Added privacy and terms pages
2025-01-13: Fixed all external links to new website URL
```

---

## Quick Reference: Common Edits

### Changing Company Name

Find and replace these in all HTML files:
- `Fresh Feel` → Your Company Name
- `Fresh Feel Painting & Cleaning` → Your Full Company Name
- `freshfeelpaintingandcleaning.ca` → Your Website URL
- `iainhmunro@gmail.com` → Your Email

### Changing Color Scheme

Current colors:
- Primary: Blue (`text-blue-600`, `bg-blue-600`)
- Secondary: Purple (`text-purple-600`, `bg-purple-600`)
- Accent: Green (`text-green-500`, `bg-green-500`)

To change all blues to greens:
1. Use Find & Replace: `text-blue-600` → `text-green-600`
2. Use Find & Replace: `bg-blue-600` → `bg-green-600`
3. Update hover colors: `hover:bg-blue-700` → `hover:bg-green-700`

### Changing Hero Image

Current image URL:
```html
<img src="https://images.unsplash.com/photo-1552321554-5fefe8c9ef14?w=600&h=600&fit=crop">
```

To use your own image:
1. Upload image to your server or use a service like Unsplash
2. Replace the entire URL with your image URL
3. Keep the `w=600&h=600&fit=crop` parameters for sizing

---

## Final Checklist Before Publishing

Before launching your website, verify:

- [ ] All navigation links work correctly
- [ ] "Get Started" buttons link to your website
- [ ] Email links open your email client
- [ ] Social media links point to your profiles
- [ ] Privacy Policy page loads correctly
- [ ] Terms of Service page loads correctly
- [ ] Mobile menu opens/closes properly
- [ ] FAQ accordion expands/collapses
- [ ] All text is updated with your company info
- [ ] All phone numbers are correct
- [ ] All email addresses are correct
- [ ] Page looks good on mobile (test in phone browser)
- [ ] Page looks good on desktop (test in desktop browser)
- [ ] All images load properly
- [ ] No broken links or 404 errors

---

## Additional Resources

### Learning Resources
- [Tailwind CSS Documentation](https://tailwindcss.com/docs)
- [Font Awesome Icons](https://fontawesome.com/icons)
- [HTML Basics](https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML)
- [CSS Basics](https://developer.mozilla.org/en-US/docs/Learn/CSS)

### Tools
- [Unsplash](https://unsplash.com/) - Free images
- [Color Picker](https://www.google.com/search?q=color+picker) - Find color codes
- [Font Awesome Icon Search](https://fontawesome.com/search) - Find icons
- [HTML Validator](https://validator.w3.org/) - Check HTML validity

### Getting Help
- Check the **Troubleshooting Tips** section above
- Review the HTML comments in your code
- Test changes in multiple browsers
- Use browser developer tools (F12) to inspect elements

---

## Conclusion

You now have a complete guide to maintaining and customizing your Fresh Feel Painting & Cleaning landing page. Remember:

1. **Start small**: Make one change at a time and test
2. **Keep backups**: Always have a copy of your original files
3. **Use Find & Replace carefully**: Preview before replacing all
4. **Test everything**: Check on both desktop and mobile
5. **Ask for help**: Don't hesitate to consult the resources above

Good luck with your website! If you have questions, refer back to the relevant section of this guide.