# RF Paving Website Scrape - Header, Footer & Design System

**Source:** https://rflandscapeproducts.co.uk/
**Date Scraped:** 2026-05-04
**Purpose:** Exact replication reference for header, footer, colour scheme, and typography

---

## 1. COLOUR SCHEME

### Primary Brand Colours

| Colour | Hex | Usage |
|--------|-----|-------|
| Dark Charcoal | `#282828` | Primary text, nav links, headings, footer text, CTA text on light buttons |
| Light Grey / Cream | `#EDEDED` | Main background (header nav bar, footer, featured sections, newsletter area) |
| Sage Green | `#C3CCB8` | Primary CTA button background, sale badges |
| Warm Beige/Gold | `#EDD7B7` | Hero CTA button background, newsletter submit button |
| White | `#FFFFFF` | Page background, card backgrounds |
| Black | `#000000` | Hover state for buttons, accordion borders |

### Secondary/Supporting Colours

| Colour | Hex | Usage |
|--------|-----|-------|
| Medium Grey | `#4B4B4B` | Secondary text, "As Seen In" title, meta text, active slider dots |
| Dark Grey | `#515151` | Hover state for headings |
| Warm Grey | `#595D5E` | Body text in content sections (e.g., stockist page) |
| Tile Colour (meta) | `#3b3b3b` | Safari pinned tab colour, MS tile colour |

### Accent/Functional Colours

| Colour | Hex | Usage |
|--------|-----|-------|
| Red (Pinterest) | `#F0002A` | Pinterest social icon background |
| Red (YouTube) | `red` (CSS keyword) | YouTube social icon background |
| Spotify Green | `#1DB954` | Spotify social icon background |
| Facebook Blue | `#1877F2` | (available in older CSS) |
| LinkedIn Blue | `#0A66C2` | (available in older CSS) |

### Button States

| State | Style |
|-------|-------|
| Primary CTA | Background: `#C3CCB8`, Text: `#282828`, Padding: 16px, Letter-spacing: 1.5px |
| Secondary CTA | Background: transparent, Border: 1px solid `#C3CCB8`, Text: `#282828` |
| Hero Primary CTA | Background: `#EDD7B7`, Text: `#282828` |
| Hero Secondary CTA | Background: transparent, Border: 1px solid `#EDD7B7`, Text: `#EDD7B7` |
| All Buttons Hover | Background: `#000000`, Text: `#FFFFFF`, Border: `#000000` |
| Trade Link | Background: `#282828`, Text: `#FFFFFF` |
| Trade Link Hover | Background: `#000000`, Text: `#FFFFFF` |

---

## 2. TYPOGRAPHY

### Font Families

| Font | Source | Usage |
|------|--------|-------|
| **Figtree** | Google Fonts (weights 300-900, italic 300-900) | Primary UI font - body text, navigation, buttons, product cards, forms, general content |
| **Lora** | Google Fonts (weights 400-700, italic 400-700) | Accent/display font - feature headings (italic), prices, testimonial meta, quotes section title |
| **Raleway** | Legacy (still in older CSS) | Search inputs, form placeholders, dropdowns (being phased out for Figtree) |
| **FontAwesome** | Self-hosted | Social media icons, UI icons |

### Google Fonts Import URL
```
https://fonts.googleapis.com/css2?family=Figtree:ital,wght@0,300..900;1,300..900&family=Lora:ital,wght@0,400..700;1,400..700&display=swap
```

### Typography Scale

| Element | Font | Size | Weight | Letter-spacing | Line-height | Style |
|---------|------|------|--------|----------------|-------------|-------|
| Hero Title | Figtree | 64px | - | - | - | Uppercase |
| Hero Subtitle | Figtree | 28px | 300 | - | 32px | - |
| Section Titles (h2) | Figtree | 32px | 500 | 2.5px | 56px | Uppercase |
| Homepage Content h1 | Lora | 36px | 100 | 0 | 58px | Italic |
| Quotes Section Title | Lora | 48px | 100 | 0 | 58px | Italic, capitalize |
| Product Card h3 | Figtree | 24px | 700 | 0 | 30px | - |
| CTA Block h3 | Figtree | 40px | 700 | - | 70px | Uppercase |
| Footer CTA h3 | Figtree | 20px | 600 | 2.5px | 26px | - |
| Brochure Module h3 | Figtree | 32px | 700 | 0 | 36px | - |
| Body Text | Figtree | 16px | 400 | - | 24px | - |
| CTA Buttons | Figtree | 16px | - | 1.5px | 18px | Uppercase |
| Nav Links | Figtree | - | - | - | - | - |
| USP Bar Text | Figtree | - | - | 3.5px | - | Uppercase |
| Trade Link | Figtree | 16px | - | 1.5px | 18px | Uppercase |
| Product Price | Lora | - | 100 | 0 | - | - |
| Price Unit (small) | Figtree | 14px | 500 | 2.5px | 20px | - |
| Testimonial Meta | Lora | 14px | 100 | 0 | 24px | Italic |
| Footer Section Title | Figtree | 16px | - | 0 | 24px | - |
| Footer Bottom | Figtree | 10px | - | - | - | - |
| Accordion Title | Figtree | 26px | 700 | 0 | 30px | - |

---

## 3. HEADER STRUCTURE

### Layout (Top to Bottom)

#### 3a. Top Navigation Bar
- **Background:** `#EDEDED`
- **Border-bottom:** none
- **Content (right-aligned):**
  - Phone: `Call: 01977 782 240` (clickable tel: link)
  - Separator: `|`
  - Link: `Contact Us` -> `/contact-us/`

#### 3b. Main Header Navigation
- **Background:** White
- **Height:** Logo height 44px
- **Layout:** 3-column grid (logo | search | account links)

**Left Column (col-3):**
- Logo: `<a href="https://rflandscapeproducts.co.uk" id="logo-main">`
- Logo Image: `https://rflandscapeproducts.co.uk/wp-content/uploads/2026/02/RF-Paving-Logo-Secondary-e1771003409814-300x68.png`
- Logo height: 44px (set via CSS: `.header a#logo-main{height:44px}`)

**Middle Column (search, flex-grow):**
- Search bar with placeholder: "Search for products..."
- Search icon: SVG magnifier
- Height: 42px
- Right margin: 50px

**Right Column (account links, right-aligned):**
- "Open a trade account" button -> `/trade-accounts/`
  - Style: Background `#282828`, color `#fff`, uppercase, letter-spacing 1.5px, font-size 16px, padding 12px 18px
- Account button icons (42x42px each):
  - Search (hidden on desktop)
  - Phone (mobile only, black_button_style)
  - My Account -> `/my-account/`
  - Basket -> `/basket/` (shows item count)
  - Mobile menu toggle

#### 3c. Main Menu Bar
- **Background:** `#EDEDED` (via `.main-navigation-section`)
- **Link colour:** `#282828`
- **Link padding:** 22px 16px

**Primary Menu Items:**
1. Shop By (mega menu dropdown)
   - All Porcelain Paving
   - Porcelain Cobbles and Edging
   - Porcelain Steps and Copings
   - Porcelain Grouts and Cleaners
   - Laying Systems
   - All Stone Paving
   - Stone Cobbles and Edging
   - Stone Steps and Copings
   - Stone Circle Kits
   - Stone Grouts and Cleaners
   - Internal Tiles
   - Porcelain In and Out Paving
   - Pergolas
   - Aluminium Drainage
   - Ecogrid
   - Aggregates
   - (and more sub-items)

2. Porcelain Paving (mega menu)
3. Stone Paving (mega menu)
4. Cladding and Tiles
5. Outdoor Kitchens
6. Pedestals
7. Drainage
8. Landscaping
9. Steps and Copings

**Secondary Menu (right side):**
- Commercial Paving
- Book a consultation
- Deliveries
- Contact Us

#### 3d. USP/Trust Badge Bar
- **Background:** (part of header)
- **Padding:** 10px top/bottom
- **Layout:** Flexbox, space-between
- **Items (icon + text):**
  1. Icon: `https://rflandscapeproducts.co.uk/wp-content/uploads/2026/02/usp-icon-1.svg` | "Family owned since 1990"
  2. Icon: `https://rflandscapeproducts.co.uk/wp-content/uploads/2023/11/header-cta-2.svg` | "Onsite Showroom"
  3. Icon: `https://rflandscapeproducts.co.uk/wp-content/uploads/2024/02/172528_price_tag_pound_icon.svg` | "PRICE MATCH GUARANTEE"
  4. Icon: `https://rflandscapeproducts.co.uk/wp-content/uploads/2023/11/header-cta-3.svg` | "DEDICATED ACCOUNT MANAGER"
- **Icon container height:** 16px
- **Icon margin-right:** 10px
- **Text style:** letter-spacing 3.5px, uppercase

### Fixed/Sticky Header
- Box shadow when fixed: `0 0 20px 0 rgb(0 0 0 / .2)`
- Submenu dropdown top offset: 64px

---

## 4. FOOTER STRUCTURE

### Layout

#### 4a. Newsletter Signup Section
- **Background:** `#EDEDED`
- **Border:** none (top and bottom)
- **Padding:** 42px top/bottom
- **Title:** "Sign up to our newsletter!" - letter-spacing 2.5px, color `#282828`, centered
- **Form:** Email input (height 50px) + Submit button
- **Submit button:** Background `#EDD7B7`, color `#282828`, letter-spacing 1.5px
- **Submit hover:** Background `#000`, color `#fff`

#### 4b. Main Footer
- **Background:** `#EDEDED`
- **Padding:** 108px top, 65px bottom

**Left Column (col-4):**
- **Title:** "Find Us" (font-size 16px, letter-spacing 0, color `#282828`, line-height 24px)
- **Description:** "The RF Paving range has grown and developed into one of the UK's leading stone brands."
- **Contact Info (with SVG icons, padding-left 33px, icon max-width 24px):**
  - Phone icon + `01977 782 240`
  - Email icon + `sales@rflandscapeproducts.co.uk`
  - Location icon + `RF Paving, A19 Doncaster Road, Whitley, East Yorkshire, DN14 0JW` (links to Google Maps)
- **Mobile: Accreditation logos** (APL Logo, HTA Logo)

**Spacer Column (col-1)**

**Right Column (col-7):**
3-column flex layout (justify-content: space-between)

**Column 1 - "Our Products":**
- Stone Paving -> `/product-category/all-natural-stone-paving/`
- Indoor Outdoor Tiles -> `/product-category/porcelain-paving/all-porcelain-paving/in-and-out-collection/`
- Porcelain Paving -> `/product-category/porcelain-paving/`
- Pedestals -> `/product-category/pedestals/`
- Steps & Copings -> `/product-category/steps-and-copings/`
- Cobbles & Edging -> `/product-category/cobbles-and-edging/`
- Cladding & Tiles -> `/product-category/all-cladding-and-tiles/`
- Decking -> `/product-category/iniwood-decking/`
- Landscaping -> `/product-category/landscaping/`

**Column 2 - "Useful Links":**
- About Us -> `/about-us/`
- Blog -> `/blog/`
- Case Studies -> `/case-studies/`
- Inspiration -> `/inspiration/`
- FAQs -> `/faq/`
- Become a Paving Stockist -> `/become-a-stockist/`
- Open A Trade Account -> `/trade-accounts/`
- Garden Paving Ideas -> `/garden-paving-ideas-landscape-and-garden-design-inspiration/`
- Contact Us -> `/contact-us/`

**Column 3 - "Policies":**
- Deliveries -> `/deliveries/`
- Terms & Conditions -> `/terms-conditions/`
- Returns & Refunds -> `/returns-refunds/`
- Privacy Policy -> `/privacy-policy/`
- Cookie Policy -> `/cookie-policy/`
- Cookie Settings -> `#` (triggers modal)

#### 4c. Footer Center Bar
- **Background:** `#EDEDED`
- **Padding:** 10px top/bottom

**Left side (col-6):**
- Payment method logos (height auto, gap 10px):
  - PayPal: `https://rflandscapeproducts.co.uk/wp-content/uploads/2024/02/PayPal.svg`
  - Amex: `https://rflandscapeproducts.co.uk/wp-content/uploads/2024/02/american-express-logo-300x81.png`
  - Mastercard: `https://rflandscapeproducts.co.uk/wp-content/uploads/2024/02/Mastercard_2019_logo.svg`
  - Visa: `https://rflandscapeproducts.co.uk/wp-content/uploads/2024/02/visa.svg`
  - Klarna: `https://rflandscapeproducts.co.uk/wp-content/uploads/2026/02/png-transparent-klarna-pink-button-tech-companies-e1771003278200-300x150.webp`

**Right side (col-6):**
- Accreditation logos (height 60px):
  - APL Logo: `https://rflandscapeproducts.co.uk/wp-content/uploads/2026/02/698e35c73b926_APL-Logo-300x187.png`
  - HTA Logo: `https://rflandscapeproducts.co.uk/wp-content/uploads/2026/02/698e35c732afc_HTA-Logo-300x230.png`
- Social Media Icons (FontAwesome):
  - Instagram: `https://www.instagram.com/rfpaving/`
  - Facebook: `https://www.facebook.com/rfpaving/`
  - Pinterest: `https://uk.pinterest.com/rfpaving/` (background: `#F0002A`)
  - TikTok: `https://www.tiktok.com/@rfpaving`
  - LinkedIn: `https://uk.linkedin.com/company/rf-landscape-products-ltd`
  - YouTube: `https://www.youtube.com/@rfpaving` (custom icon image, background: red)
  - Podcast: `https://www.youtube.com/@pavingthewaypod`

#### 4d. Footer Bottom Bar
- **Background:** `#EDEDED`
- **Padding:** 44px top/bottom
- **Font-size:** 10px

**Left (col-9):**
- "Copyright RF Paving | All Rights Reserved | Sitemap"
- Sitemap links to `/sitemap_index.xml`

**Right (col-3):**
- "Web Design & Development by Identify" -> `https://identifydigital.co.uk/`

---

## 5. MARKETING ASSETS & IMAGES

### Logo
- **Primary Logo URL:** `https://rflandscapeproducts.co.uk/wp-content/uploads/2026/02/RF-Paving-Logo-Secondary-e1771003409814-300x68.png`
- **Logo container ID:** `#logo-main`
- **Logo height:** 44px (CSS controlled)
- **Alt text:** (none specified)

### Favicon & Touch Icons
- Apple Touch Icon (180x180): `/apple-touch-icon.png`
- Favicon 32x32: `/favicon-32x32.png`
- Favicon 16x16: `/favicon-16x16.png`
- Safari Pinned Tab: `/safari-pinned-tab.svg` (colour: `#3b3b3b`)
- Web Manifest: `/site.webmanifest`

### USP Icons
1. `https://rflandscapeproducts.co.uk/wp-content/uploads/2026/02/usp-icon-1.svg`
2. `https://rflandscapeproducts.co.uk/wp-content/uploads/2023/11/header-cta-2.svg`
3. `https://rflandscapeproducts.co.uk/wp-content/uploads/2024/02/172528_price_tag_pound_icon.svg`
4. `https://rflandscapeproducts.co.uk/wp-content/uploads/2023/11/header-cta-3.svg`

### "As Seen In" Media Logos
- Ideal Home: `https://rflandscapeproducts.co.uk/wp-content/uploads/2024/07/Ideal-Home-e1721315369357-400x87.png`
- Homes & Gardens: `https://rflandscapeproducts.co.uk/wp-content/uploads/2024/07/Homes-Gardens-e1721315349438-400x130.png`
- Grand Designs Magazine: `https://rflandscapeproducts.co.uk/wp-content/uploads/2024/07/Grand-Designs-Magazine-Master--e1721315325308-400x252.png`
- Pro Landscaper: `https://rflandscapeproducts.co.uk/wp-content/uploads/2025/02/Pro-Landscaper-no1-landscaping-magazine-01-400x188.png`
- Parade: `https://rflandscapeproducts.co.uk/wp-content/uploads/2025/02/Parade-1--400x81.png`

### Payment Logos
- PayPal SVG: `https://rflandscapeproducts.co.uk/wp-content/uploads/2024/02/PayPal.svg`
- Amex PNG: `https://rflandscapeproducts.co.uk/wp-content/uploads/2024/02/american-express-logo-300x81.png`
- Mastercard SVG: `https://rflandscapeproducts.co.uk/wp-content/uploads/2024/02/Mastercard_2019_logo.svg`
- Visa SVG: `https://rflandscapeproducts.co.uk/wp-content/uploads/2024/02/visa.svg`
- Klarna: `https://rflandscapeproducts.co.uk/wp-content/uploads/2026/02/png-transparent-klarna-pink-button-tech-companies-e1771003278200-300x150.webp`

### Accreditation Logos
- APL Logo: `https://rflandscapeproducts.co.uk/wp-content/uploads/2026/02/698e35c73b926_APL-Logo-300x187.png`
- HTA Logo: `https://rflandscapeproducts.co.uk/wp-content/uploads/2026/02/698e35c732afc_HTA-Logo-300x230.png`

### Hero/Banner Images
- Main Hero: `https://rflandscapeproducts.co.uk/wp-content/uploads/2025/10/IMG-9408-1.jpg-e1759741996105.webp`
- Hero Responsive: `https://rflandscapeproducts.co.uk/wp-content/uploads/2025/10/IMG-9408-1.jpg-e1759741996105-800x523.webp`

### Icon Library
- **FontAwesome** (both old and current versions loaded)
- Custom SVG icons throughout (inline SVGs for phone, email, location, search, arrows)

---

## 6. TECHNICAL DETAILS

### WordPress Theme
- **Parent Theme:** Twenty Seventeen
- **Child Theme:** twentyseventeen-child (custom "Flavor" theme)
- **Grid System:** Bootstrap (custom build)

### Key CSS Files (in load order)
1. `parentThemeCSS` - Base theme styles
2. `bootstrapCSS` - Grid and utility classes
3. `fontawesomeOld` + `fontawesome` - Icon fonts
4. `customCss` - Main custom styles (most design rules)
5. `commercialCSS` - Commercial page styles
6. `responsive` + `responsiveNew` - Responsive breakpoints
7. `sept25Overrides` - Sept 2025 design updates
8. `jan26Overrides` - Jan 2026 design updates (latest, takes precedence)
9. `jan26Responsive` - Jan 2026 responsive updates

### CSS Cache (LiteSpeed)
All CSS is minified and served via LiteSpeed Cache at `/wp-content/litespeed/css/`

### Page Width
- Container-based layout (Bootstrap `.container`)
- Standard Bootstrap breakpoints

### Key Design Patterns
- Cards use `box-shadow: 0 5px 20px 0 rgb(0 0 0 / .1)`
- Image hover: `transform: scale(1.025)` with transition
- Slider dots: inactive `#EDEDED`, active `#4B4B4B`
- Accordion borders: 2px solid `#000`
- All images use lazy loading (LiteSpeed lazy loader)

---

## 7. SOCIAL MEDIA PROFILES

| Platform | URL | Handle |
|----------|-----|--------|
| Instagram | https://www.instagram.com/rfpaving/ | @rfpaving |
| Facebook | https://www.facebook.com/rfpaving/ | rfpaving |
| Pinterest | https://uk.pinterest.com/rfpaving/ | rfpaving |
| TikTok | https://www.tiktok.com/@rfpaving | @rfpaving |
| LinkedIn | https://uk.linkedin.com/company/rf-landscape-products-ltd | rf-landscape-products-ltd |
| YouTube | https://www.youtube.com/@rfpaving | @rfpaving |
| Podcast | https://www.youtube.com/@pavingthewaypod | @pavingthewaypod |

---

## 8. CONTACT INFORMATION

- **Phone:** 01977 782 240
- **Email:** sales@rflandscapeproducts.co.uk
- **Address:** RF Paving, A19 Doncaster Road, Whitley, East Yorkshire, DN14 0JW
- **Google Maps:** [Link](https://www.google.co.uk/maps/dir/''/rf+landscape+paving/)
