# Lifewireless Landing Page - Maintenance & Customization Guide

Welcome! This comprehensive guide will help you maintain and customize the Lifewireless landing page, even if you're new to HTML and CSS. We'll walk through everything step-by-step with specific examples from your page.

---

## Table of Contents

1. [Understanding the Page Structure](#understanding-the-page-structure)
2. [Updating Text Content](#updating-text-content)
3. [Modifying Colors and Styling](#modifying-colors-and-styling)
4. [Fixing and Updating Links](#fixing-and-updating-links)
5. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
6. [Common Tasks & Troubleshooting](#common-tasks--troubleshooting)
7. [Best Practices](#best-practices)

---

## Understanding the Page Structure

Before making changes, let's understand how your landing page is organized:

### Main Sections

Your page contains these key sections (in order from top to bottom):

1. **Header/Navigation** - The sticky menu at the top
2. **Hero Section** - The large red banner with "Activate Lifewireless SIM Card"
3. **Features Section** - Three cards explaining Quick Activation, Instant Service, Easy Setup
4. **Benefits Section** - Four benefit cards with icons
5. **CTA Section** - Call-to-action with background image
6. **About Us Section** - Company information with statistics
7. **Testimonials Section** - Customer reviews (4 cards)
8. **FAQ Section** - Frequently asked questions with expandable answers
9. **Contact Section** - Contact form and information
10. **Footer** - Links, social media, and copyright

### File Organization

Your page uses:
- **HTML** - The structure and content (in `index.html`)
- **Tailwind CSS** - Classes for styling (loaded from CDN)
- **Font Awesome** - Icons (loaded from CDN)
- **Custom CSS** - Additional styling in the `<style>` tag

---

## Updating Text Content

### Finding the Text You Want to Change

All text content is between HTML tags. Here's how to locate and change specific text:

#### Example 1: Changing the Main Headline

**Current text:**
```html
<h1 class="text-5xl md:text-6xl lg:text-7xl font-bold text-white tracking-tight leading-tight mb-4">
    Activate Lifewireless SIM Card
</h1>
```

**To change it:**
1. Find the line with "Activate Lifewireless SIM Card"
2. Replace that text with your new headline
3. Example: `Activate Your Mobile Service Today`

**Result:**
```html
<h1 class="text-5xl md:text-6xl lg:text-7xl font-bold text-white tracking-tight leading-tight mb-4">
    Activate Your Mobile Service Today
</h1>
```

> **Important:** Only change the text between the `>` and `</h1>` tags. Don't change the class names or HTML structure.

#### Example 2: Changing the Hero Subtitle

**Current text:**
```html
<p class="text-xl md:text-2xl text-white opacity-95 leading-relaxed font-medium">
    Get connected instantly with our seamless activation process. No complications, no delays—just fast, reliable service.
</p>
```

**To change it:**
1. Replace the text between `<p>` and `</p>`
2. Example: `Experience lightning-fast activation and unlimited connectivity.`

**Result:**
```html
<p class="text-xl md:text-2xl text-white opacity-95 leading-relaxed font-medium">
    Experience lightning-fast activation and unlimited connectivity.
</p>
```

#### Example 3: Changing Feature Titles

**Current text (Features section):**
```html
<h3 class="text-2xl font-bold text-dark mb-3">Quick Activation</h3>
```

**To change it:**
1. Replace "Quick Activation" with your new title
2. Example: `Speedy Setup`

**Result:**
```html
<h3 class="text-2xl font-bold text-dark mb-3">Speedy Setup</h3>
```

### Changing Text in Different Sections

#### Navigation Menu Text

**Location:** Find this in the header section:
```html
<a href="#features" class="text-dark font-medium hover:text-[#FF5A5F] transition-colors duration-300">Features</a>
```

**To change:** Replace "Features" with your new menu item text (but keep the `href="#features"` part)

```html
<a href="#features" class="text-dark font-medium hover:text-[#FF5A5F] transition-colors duration-300">Our Advantages</a>
```

#### Button Text

**Location:** Find buttons throughout the page:
```html
<a href="https://www.clipsit.net/..." class="btn-primary rounded-lg px-8 py-4 font-bold text-lg text-center inline-flex items-center justify-center gap-2 hover:shadow-2xl">
    <span>Activate Your SIM Now</span>
    <i class="fas fa-arrow-right"></i>
</a>
```

**To change:** Replace "Activate Your SIM Now" with your new button text

```html
<span>Get Started Today</span>
```

#### Footer Text

**Location:** Find this at the very bottom:
```html
<p class="text-gray-400 font-medium mb-4 md:mb-0">
    &copy; 2025 Lifewireless. All rights reserved.
</p>
```

**To change:** Update the year and company name as needed

```html
<p class="text-gray-400 font-medium mb-4 md:mb-0">
    &copy; 2025 Your Company Name. All rights reserved.
</p>
```

### Changing Testimonial Content

**Location:** Find testimonial cards in the testimonials section:
```html
<p class="text-gray-700 font-medium mb-6 leading-relaxed">
    "The activation process was incredibly smooth and fast. I was connected within minutes and the service has been reliable ever since. Highly recommend Lifewireless to anyone looking for hassle-free mobile service!"
</p>
<div class="border-t border-gray-200 pt-4">
    <p class="font-bold text-dark">Sarah Martinez</p>
    <p class="text-sm text-gray-600">Marketing Manager, Tech Solutions Inc.</p>
</div>
```

**To change:**
1. Replace the testimonial quote text
2. Replace the customer name
3. Replace the customer title/company

---

## Modifying Colors and Styling

### Understanding Tailwind CSS Classes

Tailwind CSS uses class names to apply styles. Here are the most common ones on your page:

| Class | What It Does | Example |
|-------|-------------|---------|
| `text-white` | Makes text white | `<h1 class="text-white">` |
| `bg-[#FF5A5F]` | Sets background to red color | `<div class="bg-[#FF5A5F]">` |
| `text-2xl` | Makes text large (size 2) | `<h1 class="text-2xl">` |
| `font-bold` | Makes text bold | `<p class="font-bold">` |
| `px-8` | Adds left and right padding | `<button class="px-8">` |
| `py-4` | Adds top and bottom padding | `<button class="py-4">` |
| `rounded-lg` | Rounds corners | `<div class="rounded-lg">` |
| `shadow-lg` | Adds shadow effect | `<div class="shadow-lg">` |
| `hover:bg-gray-100` | Changes background on hover | `<button class="hover:bg-gray-100">` |

### Main Brand Colors on This Page

Your page uses these primary colors:

```
Primary Red:    #FF5A5F (used for buttons, headings, accents)
Secondary Red:  #FF7A7F (used in gradients)
Yellow/Gold:    #FFD166 (used for secondary buttons and accents)
Dark Text:      #1A1A1A (used for body text on light backgrounds)
```

### How to Change the Primary Color

**Step 1:** Find all instances of `#FF5A5F` in your HTML file

**Step 2:** Replace with your new color code

**Example - Changing from Red (#FF5A5F) to Blue (#3B82F6):**

**Before:**
```html
<div class="hero-gradient">
    background: linear-gradient(135deg, #FF5A5F 0%, #FF7A7F 100%);
</div>
```

**After:**
```html
<div class="hero-gradient">
    background: linear-gradient(135deg, #3B82F6 0%, #1E40AF 100%);
</div>
```

**Where to find and replace:**

1. **In the `<style>` section** - Find these color definitions:
   ```css
   .hero-gradient {
       background: linear-gradient(135deg, #FF5A5F 0%, #FF7A7F 100%);
   }
   
   .btn-primary {
       background-color: #FF5A5F;
   }
   
   .btn-primary:hover {
       background-color: #E84A50;
   }
   
   .section-title {
       color: #FF5A5F;
   }
   
   .feature-icon {
       color: #FF5A5F;
   }
   ```

2. **In the HTML** - Find classes like:
   ```html
   <span class="text-[#FF5A5F]">Life</span>
   bg-[#FF5A5F]
   hover:text-[#FF5A5F]
   border-[#FF5A5F]
   ```

### Changing Button Styling

**Current button:**
```html
<a href="..." class="btn-primary rounded-lg px-8 py-4 font-bold text-lg text-center inline-flex items-center justify-center gap-2 hover:shadow-2xl">
    <span>Activate Your SIM Now</span>
    <i class="fas fa-arrow-right"></i>
</a>
```

**To make it larger:**
Change `px-8 py-4` to `px-12 py-6`

**To make it smaller:**
Change `px-8 py-4` to `px-6 py-3`

**To remove the icon:**
Remove the `<i class="fas fa-arrow-right"></i>` line

**To change text size:**
Change `text-lg` to `text-xl` (larger) or `text-base` (smaller)

### Changing Card Shadows

**Current:**
```html
<div class="card-hover bg-white rounded-2xl p-8 shadow-lg border border-gray-100">
```

**Shadow options:**
- `shadow-sm` - Very light shadow
- `shadow-md` - Medium shadow
- `shadow-lg` - Large shadow (current)
- `shadow-xl` - Extra large shadow
- `shadow-2xl` - Very large shadow

**Example - Making shadows more prominent:**
```html
<div class="card-hover bg-white rounded-2xl p-8 shadow-2xl border border-gray-100">
```

### Changing Spacing

Padding and margin use consistent units:

**Padding (inside element):**
- `p-4` = 1 unit of padding on all sides
- `px-8` = 8 units left and right
- `py-4` = 4 units top and bottom
- `pt-8` = 8 units top only
- `pb-4` = 4 units bottom only

**Margin (outside element):**
- `m-4` = 1 unit margin on all sides
- `mx-auto` = Center horizontally
- `mb-8` = 8 units margin bottom
- `mt-6` = 6 units margin top

**Example - Increasing padding in feature cards:**

**Before:**
```html
<div class="card-hover bg-white rounded-2xl p-8 shadow-lg border border-gray-100">
```

**After (more spacious):**
```html
<div class="card-hover bg-white rounded-2xl p-12 shadow-lg border border-gray-100">
```

---

## Fixing and Updating Links

### Understanding Links on Your Page

Your page has several types of links that need attention:

1. **Navigation menu links** - Internal links to page sections
2. **Button links** - External links to activation page
3. **Footer links** - Links to policies, social media, other pages
4. **CTA links** - Call-to-action buttons

### How HTML Links Work

A basic link looks like this:
```html
<a href="DESTINATION" class="styling">Link Text</a>
```

- `href` = Where the link goes
- `Link Text` = What users see and click on
- `class` = How it looks

### Types of Links

#### Internal Links (to other sections on the same page)

**Format:** `href="#section-id"`

**Example from your page:**
```html
<a href="#features" class="text-dark font-medium hover:text-[#FF5A5F]">Features</a>
```

This link jumps to the section with `id="features"` when clicked.

**Current internal links on your page:**
- `#features` - Features section
- `#benefits` - Benefits section
- `#faq` - FAQ section
- `#testimonials` - Testimonials section
- `#contact` - Contact section

#### External Links (to other websites)

**Format:** `href="https://www.example.com"`

**Example from your page:**
```html
<a href="https://www.clipsit.net/lifewireless-com-activate-how-to-activate-lifewireless-sim-card-and-phone/" class="btn-primary rounded-lg px-8 py-4 font-bold text-lg">
    Activate Your SIM Now
</a>
```

### Finding All Links on Your Page

**In the Header/Navigation:**
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="#testimonials">Testimonials</a>
<a href="#contact">Contact</a>
<a href="https://www.clipsit.net/lifewireless-com-activate-...">Activate Now</a>
```

**In the Hero Section:**
```html
<a href="https://www.clipsit.net/lifewireless-com-activate-...">Activate Your SIM Now</a>
```

**In the CTA Section:**
```html
<a href="https://www.clipsit.net/lifewireless-com-activate-...">Activate Now</a>
```

**In the Footer:**
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#testimonials">Testimonials</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
<a href="privacy.html">Privacy Policy</a>
<a href="terms.html">Terms of Service</a>
<a href="blog.html">Blog</a>
```

### Step-by-Step: Updating the Main Activation Link

Your page links to an external activation page. Here's how to update it:

**Step 1:** Find the link in your HTML (appears multiple times)
```html
href="https://www.clipsit.net/lifewireless-com-activate-how-to-activate-lifewireless-sim-card-and-phone/"
```

**Step 2:** Replace with your actual activation URL

**Example:** If your activation page is `https://activate.yourcompany.com/`

**Before:**
```html
<a href="https://www.clipsit.net/lifewireless-com-activate-how-to-activate-lifewireless-sim-card-and-phone/" class="btn-primary rounded-lg px-8 py-4 font-bold text-lg">
    Activate Your SIM Now
</a>
```

**After:**
```html
<a href="https://activate.yourcompany.com/" class="btn-primary rounded-lg px-8 py-4 font-bold text-lg">
    Activate Your SIM Now
</a>
```

**Step 3:** Find all instances and replace them

**Locations where this link appears:**
1. Line in hero section (large button)
2. Line in mobile menu
3. Line in CTA section

Use your text editor's "Find & Replace" feature:
- Press `Ctrl+H` (Windows) or `Cmd+H` (Mac)
- Find: `https://www.clipsit.net/lifewireless-com-activate-how-to-activate-lifewireless-sim-card-and-phone/`
- Replace with: Your new URL
- Click "Replace All"

### Updating Social Media Links

**Location:** Footer section

**Current:**
```html
<a href="#" class="w-10 h-10 flex items-center justify-center rounded-lg bg-gray-800 hover:bg-[#FF5A5F]">
    <i class="fab fa-facebook-f text-white"></i>
</a>
```

**To update Facebook link:**

**Before:**
```html
<a href="#" class="...">
    <i class="fab fa-facebook-f text-white"></i>
</a>
```

**After:**
```html
<a href="https://www.facebook.com/yourpage" class="...">
    <i class="fab fa-facebook-f text-white"></i>
</a>
```

**For other social media:**
- Facebook: `https://www.facebook.com/yourpage`
- Twitter: `https://www.twitter.com/yourhandle`
- Instagram: `https://www.instagram.com/yourprofile`
- LinkedIn: `https://www.linkedin.com/company/yourcompany`

### Fixing Broken Links

**How to identify broken links:**
1. Open your page in a browser
2. Click each link
3. If it doesn't work or shows an error, it's broken

**Common broken link issues:**

| Problem | Solution | Example |
|---------|----------|---------|
| Wrong URL | Copy correct URL from browser | Change `https://example.com` to `https://correct-example.com` |
| Missing `https://` | Add protocol for external links | Change `example.com` to `https://example.com` |
| Typo in URL | Check spelling carefully | `htps://` should be `https://` |
| Wrong section ID | Check that `id=` matches `href=#` | `href="#features"` should link to `id="features"` |
| Link to file that doesn't exist | Create the file or update link | If `privacy.html` doesn't exist, create it or update the link |

---

## Adding Privacy and Terms Pages

Your footer currently links to privacy and terms pages that don't exist yet. Let's create them and link them properly.

### Step 1: Create the Privacy Policy Page

**Create a new file called `privacy.html` in the same folder as your `index.html`**

Copy this template:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Privacy Policy for Lifewireless">
    <title>Privacy Policy - Lifewireless</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800&display=swap" rel="stylesheet">
    <style>
        * {
            font-family: 'Inter', sans-serif;
        }
    </style>
</head>
<body class="bg-white text-gray-900">
    <!-- Header -->
    <header class="sticky top-0 z-50 bg-white shadow-md">
        <nav class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-4 flex justify-between items-center">
            <div class="flex items-center">
                <h1 class="text-2xl font-bold text-gray-900">
                    <a href="index.html">
                        <span class="text-[#FF5A5F]">Life</span>wireless
                    </a>
                </h1>
            </div>
            <div class="flex gap-8">
                <a href="index.html" class="text-gray-900 font-medium hover:text-[#FF5A5F] transition-colors">Home</a>
                <a href="index.html#contact" class="text-gray-900 font-medium hover:text-[#FF5A5F] transition-colors">Contact</a>
            </div>
        </nav>
    </header>

    <!-- Content -->
    <main class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8 py-24">
        <h1 class="text-4xl font-bold text-gray-900 mb-8">Privacy Policy</h1>
        
        <div class="prose prose-lg max-w-none space-y-6 text-gray-700">
            <section>
                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">1. Introduction</h2>
                <p>
                    Lifewireless ("we," "us," "our," or "Company") is committed to protecting your privacy. This Privacy Policy explains how we collect, use, disclose, and safeguard your information when you visit our website.
                </p>
            </section>

            <section>
                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">2. Information We Collect</h2>
                <p>
                    We may collect information about you in a variety of ways. The information we may collect on the site includes:
                </p>
                <ul class="list-disc list-inside space-y-2">
                    <li>Personal Data: Name, email address, phone number, and other contact information</li>
                    <li>Device Information: Browser type, IP address, and operating system</li>
                    <li>Usage Data: Pages visited, time spent on pages, and links clicked</li>
                </ul>
            </section>

            <section>
                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">3. Use of Your Information</h2>
                <p>
                    Having accurate information about you permits us to provide you with a smooth, efficient, and customized experience. Specifically, we may use information collected about you via the site to:
                </p>
                <ul class="list-disc list-inside space-y-2">
                    <li>Process your transactions and send related information</li>
                    <li>Email you regarding your account or order</li>
                    <li>Fulfill and manage purchases, orders, payments, and other transactions related to the site</li>
                    <li>Generate a personal profile about you to make future visits to the site more personalized</li>
                    <li>Increase the efficiency and operation of the site</li>
                </ul>
            </section>

            <section>
                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">4. Disclosure of Your Information</h2>
                <p>
                    We may share information we have collected about you in certain situations:
                </p>
                <ul class="list-disc list-inside space-y-2">
                    <li>By Law or to Protect Rights</li>
                    <li>Third-Party Service Providers</li>
                    <li>Business Transfers</li>
                </ul>
            </section>

            <section>
                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">5. Security of Your Information</h2>
                <p>
                    We use administrative, technical, and physical security measures to protect your personal information. However, no method of transmission over the Internet or method of electronic storage is 100% secure.
                </p>
            </section>

            <section>
                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">6. Contact Us</h2>
                <p>
                    If you have questions or comments about this Privacy Policy, please contact us at:
                </p>
                <p>
                    <strong>Email:</strong> lifewirelessactivate@gmail.com<br>
                    <strong>Support Hours:</strong> 24/7 Available
                </p>
            </section>
        </div>
    </main>

    <!-- Footer -->
    <footer class="bg-gray-900 text-white py-12 mt-24">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
            <p class="text-gray-400 font-medium">
                &copy; 2025 Lifewireless. All rights reserved.
            </p>
        </div>
    </footer>
</body>
</html>
```

### Step 2: Create the Terms of Service Page

**Create a new file called `terms.html` in the same folder as your `index.html`**

Copy this template:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Terms of Service for Lifewireless">
    <title>Terms of Service - Lifewireless</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800&display=swap" rel="stylesheet">
    <style>
        * {
            font-family: 'Inter', sans-serif;
        }
    </style>
</head>
<body class="bg-white text-gray-900">
    <!-- Header -->
    <header class="sticky top-0 z-50 bg-white shadow-md">
        <nav class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-4 flex justify-between items-center">
            <div class="flex items-center">
                <h1 class="text-2xl font-bold text-gray-900">
                    <a href="index.html">
                        <span class="text-[#FF5A5F]">Life</span>wireless
                    </a>
                </h1>
            </div>
            <div class="flex gap-8">
                <a href="index.html" class="text-gray-900 font-medium hover:text-[#FF5A5F] transition-colors">Home</a>
                <a href="index.html#contact" class="text-gray-900 font-medium hover:text-[#FF5A5F] transition-colors">Contact</a>
            </div>
        </nav>
    </header>

    <!-- Content -->
    <main class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8 py-24">
        <h1 class="text-4xl font-bold text-gray-900 mb-8">Terms of Service</h1>
        
        <div class="prose prose-lg max-w-none space-y-6 text-gray-700">
            <section>
                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">1. Agreement to Terms</h2>
                <p>
                    By accessing and using this website, you accept and agree to be bound by the terms and provision of this agreement. If you do not agree to abide by the above, please do not use this service.
                </p>
            </section>

            <section>
                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">2. Use License</h2>
                <p>
                    Permission is granted to temporarily download one copy of the materials (information or software) on Lifewireless's website for personal, non-commercial transitory viewing only. This is the grant of a license, not a transfer of title, and under this license you may not:
                </p>
                <ul class="list-disc list-inside space-y-2">
                    <li>Modify or copy the materials</li>
                    <li>Use the materials for any commercial purpose or for any public display</li>
                    <li>Attempt to decompile or reverse engineer any software contained on the website</li>
                    <li>Remove any copyright or other proprietary notations from the materials</li>
                    <li>Transfer the materials to another person or "mirror" the materials on any other server</li>
                </ul>
            </section>

            <section>
                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">3. Disclaimer</h2>
                <p>
                    The materials on Lifewireless's website are provided on an 'as is' basis. Lifewireless makes no warranties, expressed or implied, and hereby disclaims and negates all other warranties including, without limitation, implied warranties or conditions of merchantability, fitness for a particular purpose, or non-infringement of intellectual property or other violation of rights.
                </p>
            </section>

            <section>
                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">4. Limitations</h2>
                <p>
                    In no event shall Lifewireless or its suppliers be liable for any damages (including, without limitation, damages for loss of data or profit, or due to business interruption) arising out of the use or inability to use the materials on Lifewireless's website.
                </p>
            </section>

            <section>
                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">5. Accuracy of Materials</h2>
                <p>
                    The materials appearing on Lifewireless's website could include technical, typographical, or photographic errors. Lifewireless does not warrant that any of the materials on its website are accurate, complete, or current. Lifewireless may make changes to the materials contained on its website at any time without notice.
                </p>
            </section>

            <section>
                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">6. Links</h2>
                <p>
                    Lifewireless has not reviewed all of the sites linked to its website and is not responsible for the contents of any such linked site. The inclusion of any link does not imply endorsement by Lifewireless of the site. Use of any such linked website is at the user's own risk.
                </p>
            </section>

            <section>
                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">7. Modifications</h2>
                <p>
                    Lifewireless may revise these terms of service for its website at any time without notice. By using this website, you are agreeing to be bound by the then current version of these terms of service.
                </p>
            </section>

            <section>
                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">8. Governing Law</h2>
                <p>
                    These terms and conditions are governed by and construed in accordance with the laws of the United States, and you irrevocably submit to the exclusive jurisdiction of the courts in that location.
                </p>
            </section>

            <section>
                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">9. Contact Information</h2>
                <p>
                    If you have any questions about these Terms of Service, please contact us at:
                </p>
                <p>
                    <strong>Email:</strong> lifewirelessactivate@gmail.com<br>
                    <strong>Support Hours:</strong> 24/7 Available
                </p>
            </section>
        </div>
    </main>

    <!-- Footer -->
    <footer class="bg-gray-900 text-white py-12 mt-24">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
            <p class="text-gray-400 font-medium">
                &copy; 2025 Lifewireless. All rights reserved.
            </p>
        </div>
    </footer>
</body>
</html>
```

### Step 3: Verify Links in Your Index.html

Your `index.html` already has these links in the footer:

```html
<a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300 font-medium">Privacy Policy</a>
<a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300 font-medium">Terms of Service</a>
```

**These links should now work correctly!** The pages will be found because:
1. `privacy.html` is in the same folder as `index.html`
2. `terms.html` is in the same folder as `index.html`
3. The links use relative paths (no full URL needed)

### Step 4: Customize the Policy Pages

Once you've created the pages, customize them:

**In `privacy.html`:**
1. Find "Privacy Policy" headings and update as needed
2. Update the contact email: Change `lifewirelessactivate@gmail.com` to your email
3. Add your specific privacy practices in each section
4. Update copyright year if needed

**In `terms.html`:**
1. Find "Terms of Service" headings and update as needed
2. Update the contact email
3. Customize terms specific to your business
4. Update copyright year if needed

### File Structure After Adding Pages

Your folder should now look like this:

```
your-project-folder/
├── index.html          (your main landing page)
├── privacy.html        (new - privacy policy)
├── terms.html          (new - terms of service)
└── blog.html           (optional - if you want to create it)
```

---

## Common Tasks & Troubleshooting

### Task 1: Change the Company Name Throughout the Page

**Step 1:** Find all instances of "Lifewireless"

**Step 2:** Replace with your company name

**Locations to update:**
- Logo in header: `<span class="text-[#FF5A5F]">Life</span>wireless`
- Hero title: `Activate Lifewireless SIM Card`
- Section titles: `Why Choose Lifewireless Activation?`
- About section: `About Lifewireless`
- Footer copyright: `&copy; 2025 Lifewireless`
- Meta tags: `<title>Lifewireless Activate...`

**Example:**

**Before:**
```html
<h1 class="text-2xl font-bold text-dark">
    <span class="text-[#FF5A5F]">Life</span>wireless
</h1>
```

**After (if your company is "MobileConnect"):**
```html
<h1 class="text-2xl font-bold text-dark">
    <span class="text-[#FF5A5F]">Mobile</span>Connect
</h1>
```

### Task 2: Change the Contact Email

**Current email:** `lifewirelessactivate@gmail.com`

**Locations to update:**
1. Contact section form
2. Contact information box
3. Footer social links area
4. All policy pages

**Find & Replace:**
- Find: `lifewirelessactivate@gmail.com`
- Replace with: `your-email@yourcompany.com`

### Task 3: Add a New Feature Card

**Current structure (in Features section):**
```html
<div class="grid grid-cols-1 md:grid-cols-3 gap-8">
    <!-- Feature 1 -->
    <div class="card-hover bg-white rounded-2xl p-8 shadow-lg border border-gray-100">
        <!-- content -->
    </div>
    
    <!-- Feature 2 -->
    <div class="card-hover bg-white rounded-2xl p-8 shadow-lg border border-gray-100">
        <!-- content -->
    </div>
    
    <!-- Feature 3 -->
    <div class="card-hover bg-white rounded-2xl p-8 shadow-lg border border-gray-100">
        <!-- content -->
    </div>
</div>
```

**To add a 4th feature:**

**Step 1:** Change the grid from 3 columns to 4:
```html
<div class="grid grid-cols-1 md:grid-cols-4 gap-8">
```

**Step 2:** Add a new feature card after Feature 3:
```html
<!-- Feature 4 -->
<div class="card-hover bg-white rounded-2xl p-8 shadow-lg border border-gray-100">
    <div class="mb-6 flex items-center justify-center w-16 h-16 rounded-full bg-[#FF5A5F] bg-opacity-10">
        <svg class="w-8 h-8 text-[#FF5A5F]" fill="none" stroke="currentColor" viewBox="0 0 24 24" stroke-width="1.5">
            <!-- Icon SVG code -->
        </svg>
    </div>
    <h3 class="text-2xl font-bold text-dark mb-3">Feature Name</h3>
    <p class="text-gray-600 font-medium leading-relaxed mb-4">
        Feature description goes here.
    </p>
    <ul class="space-y-2">
        <li class="flex items-center gap-2 text-gray-700">
            <svg class="w-5 h-5 text-[#FF5A5F]" fill="none" stroke="currentColor" viewBox="0 0 24 24" stroke-width="2">
                <path stroke-linecap="round" stroke-linejoin="round" d="M5 13l4 4L19 7"></path>
            </svg>
            <span>Benefit 1</span>
        </li>
        <li class="flex items-center gap-2 text-gray-700">
            <svg class="w-5 h-5 text-[#FF5A5F]" fill="none" stroke="currentColor" viewBox="0 0 24 24" stroke-width="2">
                <path stroke-linecap="round" stroke-linejoin="round" d="M5 13l4 4L19 7"></path>
            </svg>
            <span>Benefit 2</span>
        </li>
    </ul>
</div>
```

**Note:** On mobile, it will still show 1 column (`md:grid-cols-4` means 4 columns on medium screens and up).

### Task 4: Update the Hero Background Image

**Current CTA section:**
```html
<div class="absolute inset-0 bg-cover bg-center" style="background-image: url('https://images.unsplash.com/photo-1556656793-08538906a9f8?w=1200&h=600&fit=crop'); background-attachment: fixed;"></div>
```

**To change the image:**

**Step 1:** Get a new image URL (from Unsplash, Pexels, or your own server)

**Step 2:** Replace the URL:
```html
style="background-image: url('YOUR-NEW-IMAGE-URL-HERE');"
```

**Example with a different image:**
```html
style="background-image: url('https://images.unsplash.com/photo-1611532736579-6b16e2b50449?w=1200&h=600&fit=crop');"
```

### Task 5: Change the Number of Testimonial Cards Shown

**Current:** 4 testimonial cards in a row on desktop

**To show 3 per row:**

Find this line:
```html
<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-8">
```

Change to:
```html
<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
```

**Explanation:**
- `grid-cols-1` = 1 column on mobile
- `md:grid-cols-2` = 2 columns on medium screens
- `lg:grid-cols-3` = 3 columns on large screens (changed from 4)

### Troubleshooting: Links Not Working

| Problem | Solution |
|---------|----------|
| Button doesn't go anywhere | Check that `href="..."` is not empty or `href="#"` |
| Internal link doesn't scroll to section | Verify section has matching `id="name"` and link has `href="#name"` |
| External link shows error | Check URL spelling, ensure it starts with `https://` |
| Page looks broken after editing | Check that all opening tags have closing tags (`<div>` has `</div>`) |

**Example of matching internal link:**

**HTML section:**
```html
<section id="features">
    <!-- content -->
</section>
```

**Link to that section:**
```html
<a href="#features">Go to Features</a>
```

The `id` and `href` must match exactly!

### Troubleshooting: Styling Looks Wrong

| Problem | Solution |
|---------|----------|
| Text is wrong color | Check `text-[#COLORCODE]` or `text-white` class |
| Button is too small | Increase `px-8 py-4` to `px-12 py-6` |
| Card has no shadow | Add `shadow-lg` or `shadow-xl` to the card class |
| Spacing is too tight | Increase margin/padding values (e.g., `mb-8` to `mb-12`) |
| Text is too small | Change `text-lg` to `text-xl` or `text-2xl` |

---

## Best Practices

### 1. Always Backup Before Making Changes

**Before editing:**
1. Make a copy of your HTML file
2. Name it something like `index-backup.html`
3. Keep it in the same folder
4. This way, you can revert if something goes wrong

### 2. Test Changes in a Browser

**After making changes:**
1. Save your HTML file
2. Open it in a web browser
3. Check that everything looks correct
4. Click all links to verify they work
5. Test on mobile by resizing your browser window

### 3. Use Consistent Formatting

**Keep your code organized:**
- Use indentation (4 spaces or 1 tab) to show structure
- Keep related elements together
- Add comments for complex sections

**Example:**
```html
<!-- Hero Section -->
<section class="hero-gradient">
    <!-- Hero content -->
</section>

<!-- Features Section -->
<section id="features">
    <!-- Feature content -->
</section>
```

### 4. Test Responsive Design

Your page should work on:
- Desktop (1920px wide)
- Tablet (768px wide)
- Mobile (375px wide)

**To test:**
1. Open page in browser
2. Press F12 (or right-click → Inspect)
3. Click the device icon (mobile view)
4. Try different device sizes

### 5. Keep Color Consistency

**Your page uses:**
- Primary Red: `#FF5A5F` - Use for main buttons and accents
- Secondary Red: `#FF7A7F` - Use in gradients
- Gold: `#FFD166` - Use for secondary elements
- Dark: `#1A1A1A` - Use for main text

**Don't add too many new colors.** Stick to 3-4 main colors for a professional look.

### 6. Verify All Links Work

**Weekly checklist:**
- [ ] Test all navigation menu links
- [ ] Test all buttons
- [ ] Test footer links
- [ ] Test social media links
- [ ] Check external links still work

### 7. Keep Contact Information Updated

**Remember to update:**
- Email address: `lifewirelessactivate@gmail.com`
- Phone number (if you add one)
- Social media links
- Physical address (if applicable)

### 8. Use Descriptive Link Text

**Bad:**
```html
<a href="https://example.com">Click here</a>
```

**Good:**
```html
<a href="https://example.com">Learn more about our features</a>
```

This helps:
- Users understand where the link goes
- Search engines understand your content
- Accessibility tools work better

---

## Quick Reference: Common Edits

### Changing Text
```html
<!-- Find this -->
<h1>Old Text</h1>

<!-- Change to -->
<h1>New Text</h1>
```

### Changing Links
```html
<!-- Find this -->
<a href="old-link.html">Link Text</a>

<!-- Change to -->
<a href="new-link.html">Link Text</a>
```

### Changing Colors
```html
<!-- Find this -->
background-color: #FF5A5F;

<!-- Change to -->
background-color: #3B82F6;
```

### Adding Spacing
```html
<!-- Increase padding -->
<div class="p-8">  <!-- Change 8 to 12 -->
<div class="p-12">

<!-- Increase margin -->
<div class="mb-4">  <!-- Change 4 to 8 -->
<div class="mb-8">
```

### Making Text Larger
```html
<!-- Find this -->
<h1 class="text-2xl">Heading</h1>

<!-- Change to -->
<h1 class="text-4xl">Heading</h1>
```

---

## Getting Help

### Resources for Learning

- **Tailwind CSS Documentation:** https://tailwindcss.com/docs
- **HTML Basics:** https://www.w3schools.com/html/
- **CSS Basics:** https://www.w3schools.com/css/
- **Font Awesome Icons:** https://fontawesome.com/icons

### Common Questions Answered

**Q: Can I use this page with a different company name?**
A: Yes! Replace all instances of "Lifewireless" with your company name.

**Q: How do I add more testimonials?**
A: Copy one of the testimonial cards and paste it below, then update the text and name.

**Q: Can I change the page colors?**
A: Yes! Find all instances of `#FF5A5F` (red) and replace with your brand color code.

**Q: Where do I host this page?**
A: You can use services like Netlify, Vercel, GitHub Pages, or traditional web hosting.

**Q: How do I make the contact form actually send emails?**
A: The page includes Web3Forms integration. Update the `access_key` value with your own from https://web3forms.com/

---

## Summary

You now have the knowledge to:

✅ Update all text content on the page  
✅ Modify colors and styling with Tailwind CSS  
✅ Fix and update all links  
✅ Create and link privacy and terms pages  
✅ Handle common customization tasks  
✅ Troubleshoot common issues  

**Remember:** Always test your changes in a browser before publishing, and keep a backup of your original files!

Happy editing! 🚀