# Design Guidelines: Premium Dark-Themed Bakery Landing Page

## Design Approach
**Reference-Based Approach**: Drawing inspiration from luxury e-commerce and artisan food brands with emphasis on premium product photography, dramatic lighting, and elegant minimalism.

## Core Design Principles
- Premium, luxury aesthetic with dark sophistication
- Product-centric visual storytelling through professional photography
- Elegant restraint with strategic gold accent usage
- Smooth, polished interactions throughout

## Color Palette

**Dark Mode (Primary)**
- Background Primary: 26 0% 10% (≈ #1a1a1a)
- Background Secondary: 0 0% 16% (≈ #2a2a2a)
- Accent Gold: 30 50% 65% (≈ #d4a574)
- Accent Gold Dark: 30 42% 58% (≈ #c49a6c)
- Text Primary: 0 0% 100% (#ffffff)
- Text Secondary: 0 0% 53% (≈ #888888)
- Text Tertiary: 0 0% 40% (≈ #666666)
- Transparent Overlays: rgba(0,0,0,0.5)

## Typography

**Font Families**
- Display/Script Font: Elegant script font (Playfair Display, Libre Baskerville, or similar) for "Baking Maniac", "Cupcake", "Specialities"
- Body Font: Clean sans-serif (Inter, Poppins) for navigation, body text
- Accent Caps: All-caps sans-serif for section prefixes ("OUR", "ABOUT", "CONTACT")

**Hierarchy**
- Hero Display: 4xl-6xl, script font, white
- Section Headers: Gray caps (uppercase, tracking-wide) + white script combination
- Body Text: Base to lg, white for primary, gray for secondary
- Navigation: Base, medium weight
- Buttons: Base, medium weight, uppercase tracking

## Layout System

**Spacing Primitives**: Use Tailwind units of 2, 4, 6, 8, 12, 16, 20, 24, 32
- Section padding: py-20 to py-32
- Card padding: p-6 to p-8
- Element spacing: gap-4, gap-6, gap-8

**Container Strategy**
- Full-width sections with inner max-w-7xl
- Generous white space, breathable layouts
- Consistent rounded corners: rounded-lg (8px) to rounded-xl (12px)

## Component Library

### Navigation Bar
- Fixed top position, dark transparent background with blur
- Three-section layout: left menu | center logo | right actions
- Left: Home, About us, Portfolio (white text, hover: gold)
- Center: "bm BAKING MANIAC" in gold script/elegant font
- Right: Cake shop, Contact, search icon, shopping cart with notification badge
- Minimal padding (py-4), clean spacing

### Hero Section
- Full-screen (min-h-screen) centered product showcase
- Large gray "PEANUT" text as background design element (opacity-20)
- "Cupcake" white script font overlaying
- Dramatic product photography with floating elements
- Gold-outlined "Shop Now" button (rounded-full, border-2, transparent bg, gold border, px-8 py-3)
- Center-aligned, vertical flow

### Specialties Section
- "OUR Specialities" heading (gray caps + white script)
- Grid: 2 rows × 3 columns (grid-cols-3 gap-8)
- Circular icon cards (aspect-square, rounded-full)
- Dark background, gold icons (w-12 h-12), gold labels below
- Categories: Cupcakes, Cheesecakes, Butter Cakes, Cookies, Macarons, Brownies
- Thin circular borders (border border-gold/30)
- Hover: subtle glow (shadow-xl shadow-gold/20) or scale (scale-105)

### About Section
- Two-column layout: text left (60%) | image right (40%)
- "ABOUT Baking Maniac" heading style
- Body text: 2-3 paragraphs, leading-relaxed
- Gold-outlined "Read More" button (matching hero style)
- Right: Circular frame (rounded-full, overflow-hidden) with product photo
- Decorative gold "bm" divider line above footer (h-px bg-gold/30, max-w-xs mx-auto)
- Social icons: Instagram, Twitter, Pinterest (white, hover: gold)

### Portfolio/Products Grid
- Horizontal category navigation with icons (flex gap-6)
- Active category: gold, others: gray
- Product grid: 3 columns, 2+ rows (grid-cols-3 gap-6)
- Product cards: dark rounded rectangles (bg-dark-secondary, rounded-xl)
- Centered product photo, white text label below (p-6)
- Products: Hazelnut, Lime, Caramel, Bubble Tea, Red Velvet, Rum & Raisin
- Hover: slight scale (scale-105), subtle shadow

### Contact Section
- "CONTACT Us" large heading (gray caps + white script)
- Three-column contact info (grid-cols-3 gap-8)
- Icons + text: Email (confectionery@bakingmaniac.com), Phone (+852 669 98090), Location (5B, Kwai Bo Indusrial Bld. Hong Kong)
- Contact form with glassmorphism (bg-white/5, backdrop-blur-md, rounded-xl, p-8)
- Form fields: Name, Email, Phone (grid-cols-3 gap-4), Message textarea (full width, rows-6)
- Dark transparent inputs (bg-white/10, border border-white/20, text-white, placeholder-gray)
- Gold "Send Message" button (bg-gold, text-dark, rounded-lg, py-3)

## Visual Effects

**Glassmorphism**
- Cards/forms: bg-white/5, backdrop-blur-md, border border-white/10

**Animations**
- Fade-in on scroll for sections
- Hover effects: scale-105, brightness increase, subtle glow
- Smooth transitions: transition-all duration-300

**Product Photography Treatment**
- Dramatic professional lighting (hard shadows, high contrast)
- Floating elements (chocolate pieces, peanuts, berries)
- Powder/flour dust atmospheric effects
- Dark background with rim lighting on products

## Images

**Hero Section**
- Large, dramatic full-screen hero image: Professional photo of chocolate cupcake with peanut butter frosting
- Composition: Centered cupcake with floating chocolate pieces and peanuts creating dynamic movement
- Atmospheric effects: Powder/flour dust, dramatic lighting with rim light highlighting the cupcake edges
- Overlay: Large gray "PEANUT" text as background element with low opacity, "Cupcake" script text overlay

**About Section**
- Circular-framed product photo: Dramatic chocolate cake slice with strawberry garnish
- Professional studio lighting, dark background with spotlight effect
- Positioned in right column within circular frame

**Portfolio/Products Section**
- 6+ product photos: Individual cupcake varieties (Hazelnut, Lime, Caramel, Bubble Tea, Red Velvet, Rum & Raisin)
- Each photo: Centered on dark background, professional lighting showing texture and details
- Consistent styling across all product images

## Responsive Behavior
- Mobile: Single column layouts, stacked navigation menu, reduced padding
- Tablet: 2-column grids where applicable
- Desktop: Full multi-column layouts as specified
- Touch-friendly targets on mobile (min 44px)

## Accessibility
- Maintain contrast ratios (gold on dark: 4.5:1 minimum)
- Focus states visible with gold outline
- Smooth scrolling with reduced motion support
- Alt text for all product photography

This design creates a premium, luxury bakery experience with dramatic product photography, elegant typography, and sophisticated dark aesthetics throughout.