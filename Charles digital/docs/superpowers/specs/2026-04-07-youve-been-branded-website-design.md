# You've Been Branded Website Design Spec

**Date:** April 7, 2026
**Project:** Custom laser engraving business website
**Style:** Rustic/Artisan with premium 3D interactions
**Goal:** Showcase portfolio, build brand credibility, enable customer contact

---

## Overview

A single-page, immersive portfolio website for You've Been Branded — a laser engraving business specializing in custom leather and cork products. The site prioritizes a dramatic, interactive gallery experience with rustic aesthetic and full 3D cursor interactions throughout.

**Tagline:** "We cut corners — beautifully"

---

## Design Principles

1. **Portfolio First:** Gallery section immediately visible and interactive after hero
2. **Rustic Premium:** Dark, warm color palette with leather/natural textures
3. **Fully Interactive:** 3D effects on every interaction (cursor, scroll, hover)
4. **Balanced CTAs:** Equal emphasis on portfolio showcase, brand story, and contact
5. **Mobile Responsive:** Touch-friendly, simplified interactions on mobile devices

---

## Color Palette

- **Primary Dark:** #0A0A0A (deep black for backgrounds)
- **Secondary Dark:** #141414 (card backgrounds)
- **Accent Warm:** #D4883A (amber/leather tone)
- **Accent Light:** #E8A85C (lighter amber)
- **Text:** #FFFFFF (white)
- **Texture Base:** #8B5E3C (leather brown for overlays)

---

## Page Structure

### 1. Navigation (Fixed Header)

**Elements:**
- Logo (left)
- Nav links: Portfolio | About | Contact (center/right)
- Smooth backdrop blur when scrolled past hero

**Behavior:**
- Fixed position, z-index maintained
- Subtle fade-in of background as user scrolls
- Smooth scroll to sections on link click

---

### 2. Hero Section

**Layout:** Full viewport height (100vh)

**Content:**
- Tagline: "We cut corners — beautifully"
- Subheading: "Custom laser-engraved leather & cork goods"
- CTA Button: "Explore Our Work" (links to gallery)

**3D Effects:**
- Parallax depth layers in background
- Mountains/geometric shapes move with cursor
- Subtle animated glow that follows mouse position
- Fade-in animation on page load

**Styling:**
- Dark background with warm lighting/gradient
- Large, bold typography (serif for tagline, sans-serif for body)
- Centered composition

---

### 3. Gallery Section (Hero Feature)

**Purpose:** Showcase all portfolio items with maximum visual impact

**Layout:**
- 3-column grid on desktop (1440px+)
- 2-column grid on tablet (768px - 1439px)
- 1-column grid on mobile (< 768px)
- Padding: 60px top/bottom, 40px sides

**Card Components:**

Each product card contains:
- **Image:** Product photo (high-quality, optimized)
- **Tilt Effect:** Card rotates/tilts smoothly as cursor moves (max 15° rotation)
- **Overlay:** Semi-transparent dark overlay on hover
- **Text Label:** Product category (e.g., "Custom Coasters", "Personalized Keyrings", "Branded Boxes")
- **Scale Animation:** Subtle 1.05x scale on hover
- **Shadow:** Deeper shadow on hover state

**Lightbox:**
- Clicking a card opens full-screen lightbox
- Shows larger image + product details
- Arrow navigation to browse gallery
- Close button (X) or click outside to close
- Smooth fade-in/out animations

**Scroll Animation:**
- Photos fade in as they enter viewport
- Staggered horizontal flip effect (each card flips slightly)
- Offset timing for cascading effect
- Smooth easing (cubic-bezier preferred)

**Content:** 12-14 product images from Instagram portfolio
- Leather boxes, cork coasters, keyrings, tags, branded items

---

### 4. About Section

**Layout:** Two-column grid (text left, visual right on desktop; stacked on mobile)

**Column 1 (Text):**
- Heading: "Crafted with Precision"
- 3-4 paragraphs about:
  - Who you are and your story
  - Laser engraving philosophy
  - Custom approach
  - Commitment to quality
- Key bullet points:
  - Precision laser cutting
  - Fully customizable
  - Quality materials (leather, cork)
  - Fast turnaround

**Column 2 (Visual):**
- Parallax background image (workspace/product shot)
- Optional: animated accent graphic
- Warm lighting, leather textures

**Animations:**
- Text fades in as section comes into view
- Parallax effect on background image (moves slower than scroll)
- Smooth transitions

**Vibe:** Builds emotional connection, establishes credibility

---

### 5. Contact Section

**Layout:** Two-column on desktop (form left, info right); stacked on mobile

**Column 1 (Contact Form):**
- Form fields:
  - Name (required)
  - Email (required, validated)
  - Message (textarea, required)
  - Product Interest (dropdown: Custom Order, General Inquiry, Partnership)
- Submit button with hover state
- Success/error messages with animations
- Validation feedback (inline, real-time)

**Column 2 (Contact Info):**
- Heading: "Get in Touch"
- Email: youvebeenbranded@outlook.com
- Website: youvebeenbranded.co.uk
- Social links with icons:
  - Instagram (@youvebeenbranded)
  - Potentially others (TBA)
- Hours/response time note

**Animations:**
- Form inputs have smooth focus states (border color change)
- Button hover: subtle glow, scale increase
- Success message: smooth slide-in

**Vibe:** Professional, accessible, inviting

---

### 6. Footer

**Elements:**
- Copyright text
- Social links
- "Built with precision" tagline
- Links to any legal pages (if needed)

**Styling:** Dark background, matches header, minimal

---

## Technical Specifications

### 3D Effects & Animations

**Cursor Glow:**
- Fixed element (300px diameter circle)
- Follows mouse with smooth easing
- Radial gradient (amber to transparent)
- Low opacity (8-10%)
- Z-index: very high, pointer-events: none

**Card Tilt:**
- Library: Tilt.js (or vanilla JavaScript implementation)
- Max rotation: ±15°
- Speed: 400ms easing
- Reset on mouse leave

**Parallax Scrolling:**
- Hero: depth layers (2-3 layers moving at different speeds)
- About: background image moves 30-50% slower than scroll
- Implemented via: transform: translateY() on scroll

**Scroll Reveals:**
- Intersection Observer API for viewport detection
- Fade-in: opacity 0 → 1 over 600ms
- Flip effect: rotateY(-90deg) → 0 with stagger
- Easing: cubic-bezier(0.34, 1.56, 0.64, 1)

**Smooth Scroll:**
- CSS: scroll-behavior: smooth
- All anchor links smooth-scroll to targets

### Image Optimization

- Source: Instagram portfolio photos (15-20 images)
- Formats: WebP primary, JPEG fallback
- Sizes:
  - Gallery cards: 400px × 400px (desktop)
  - Lightbox: 800px × 800px
  - Lazy loading: all images below fold
- Compression: Balanced quality/performance

### Responsive Breakpoints

- **Desktop:** 1440px+ (3-column grid)
- **Tablet:** 768px - 1439px (2-column grid)
- **Mobile:** < 768px (1-column grid)
- All sections fully responsive, touch-friendly

### Browser Compatibility

- Modern browsers (Chrome, Firefox, Safari, Edge)
- CSS Grid, Flexbox, CSS Transforms fully supported
- Fallbacks for older browsers (graceful degradation)

### Performance Targets

- Lighthouse score: 90+
- Time to interactive: < 3 seconds
- 60fps animations (smooth scroll, hover effects)
- Lazy loading for images below fold

---

## Content Requirements

**Images Needed:**
- 12-14 high-quality product photos from Instagram
- About section background image (workspace/product)
- Hero section optional (accent graphic/animation)

**Text Needed:**
- About section: Brand story (3-4 paragraphs)
- Product categories for gallery labels
- Contact page copy

---

## Interactions Checklist

- ✅ Cursor glow follows mouse
- ✅ Cards tilt on hover
- ✅ Gallery items fade/flip in on scroll
- ✅ Lightbox opens on card click
- ✅ Parallax backgrounds move on scroll
- ✅ Form validation real-time
- ✅ Smooth scroll navigation
- ✅ Mobile: tap for card interactions, no tilt on touch
- ✅ All hover states animated smoothly

---

## Success Criteria

1. **Portfolio Visibility:** Gallery immediately impactful on load
2. **Engagement:** 3D effects feel premium and smooth (60fps)
3. **Conversion:** Contact form easy to find and use
4. **Brand:** Rustic aesthetic maintained throughout
5. **Performance:** Fast load times, smooth animations
6. **Responsiveness:** Mobile experience equally polished

---

## Deliverables

1. Single HTML file with embedded CSS and JavaScript
2. Optimized images (WebP + JPEG fallback)
3. Cross-browser tested
4. Mobile responsive
5. Fully animated and interactive

---

## Next Steps

1. Gather 15-20 product images from Instagram
2. Write About section content
3. Implement HTML structure
4. Add CSS styling (Flexbox/Grid, animations)
5. Implement JavaScript (3D effects, interactions, form validation)
6. Optimize images
7. Test on mobile, tablet, desktop
8. Deploy

