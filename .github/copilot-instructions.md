# GitHub Copilot Instructions for Aït M'Hend DNA Heritage Site

## Project Overview

This is a static genealogy and cultural heritage website showcasing Amazigh (Berber) DNA analysis and cultural identity from the Anti-Atlas Mountains of Morocco. The site presents genetic research in a scholarly, professional manner while celebrating Berber cultural heritage.

**Live Site:** https://aitmhend-dna.github.io  
**Repository:** https://github.com/aitmhend-dna/aitmhend-dna.github.io

## Design Philosophy

### Core Principles
- **Professional & Scholarly**: Academic tone with scientific credibility
- **Culturally Authentic**: Berber/Anti-Atlas identity throughout
- **Modern & Minimal**: Flat design, clean lines, no excessive decoration
- **Sharp & Precise**: Crisp borders (3-8px radius), no rounded bubbles
- **Elegant Subtlety**: Gentle gradients (3-6% opacity), refined accents

### Visual Identity
The site uses a **Berber/Anti-Atlas cultural color palette** inspired by the terracotta, ochre, and clay tones of traditional Amazigh architecture and the Atlas Mountains landscape.

**NEVER use blue colors** - they were removed for appearing "AI-generated" and generic.

## Color Palette

### Primary Colors
```css
--primary-terracotta: #CD7F32;      /* Main brand color */
--ochre: #CC8E35;                    /* Secondary accent */
--clay-orange: #D2691E;              /* Tertiary accent */
--warm-sand: #E2A36B;                /* Light accent */
--burnt-sienna: #8B4513;             /* Dark accent */
--deep-brown: #3E2723;               /* Text/borders */
```

### Neutral Colors
```css
--white: #FFFFFF;
--light-gray: #F5F5F5;
--medium-gray: #E0E0E0;
--dark-gray: #424242;
--black: #1A1A1A;
```

### Gradient Backgrounds (Subtle)
Use opacity: 3-6% for card backgrounds
```css
background: linear-gradient(135deg, 
    rgba(205, 127, 50, 0.03) 0%, 
    rgba(204, 142, 53, 0.06) 100%);
```

## Typography

### Font Stack
```css
/* Body Text */
font-family: 'Inter', -apple-system, BlinkMacSystemFont, sans-serif;
font-weight: 300 | 400 | 500 | 600 | 700 | 800;

/* Headings */
font-family: 'Space Grotesk', 'Inter', sans-serif;
font-weight: 400 | 500 | 600 | 700;

/* Data, Code, Numbers */
font-family: 'IBM Plex Mono', 'Courier New', monospace;
font-weight: 400 | 500 | 600;
```

### Font Sizes
```css
h1: 2.5rem (40px)
h2: 2rem (32px)
h3: 1.5rem (24px)
body: 1rem (16px)
small: 0.875rem (14px)
```

## Design Components

### Buttons
```css
/* Primary Button */
background: #CD7F32;              /* Solid, no gradients */
color: #FFFFFF;                   /* White text for clarity */
padding: 0.75rem 1.5rem;
border-radius: 5px;               /* Sharp corners */
border: 2px solid transparent;
font-weight: 600;

/* Hover State */
background: #B8722D;
transform: translateY(-2px);
box-shadow: 0 4px 12px rgba(205, 127, 50, 0.3);
```

### Cards
```css
/* Elegant Card Style */
background: linear-gradient(135deg, 
    rgba(205, 127, 50, 0.03) 0%, 
    rgba(204, 142, 53, 0.06) 100%);
border: 1px solid rgba(205, 127, 50, 0.2);
border-radius: 8px;               /* Sharp minimal */
padding: 1.5rem;
position: relative;

/* Decorative Corner Accent (optional) */
.card::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    width: 40px;
    height: 40px;
    background: linear-gradient(135deg, 
        rgba(205, 127, 50, 0.1) 0%, 
        transparent 100%);
    border-radius: 8px 0 0 0;
}
```

### Sections
```css
/* Section Styling */
padding: 4rem 0;
background: #FFFFFF;              /* Clean white, no gradients */

/* Section Headings */
border-bottom: 3px solid #CD7F32; /* Terracotta accent */
padding-bottom: 0.5rem;
margin-bottom: 2rem;
```

### Navigation
```css
/* Header Navigation */
position: sticky;
top: 0;
z-index: 2000;                    /* High z-index for visibility */
background: rgba(255, 255, 255, 0.95);
backdrop-filter: blur(10px);
border-bottom: 2px solid #CD7F32;

/* Active Link */
color: #CD7F32;
border-bottom: 2px solid #CD7F32;
```

## Layout Patterns

### Hero Sections
```html
<!-- Scholarly 2-Column Layout -->
<section class="hero">
    <div class="hero-content">
        <div class="hero-text">
            <!-- Text content -->
        </div>
        <div class="hero-image">
            <!-- Image with rounded corners -->
        </div>
    </div>
</section>
```

### Timeline (Vertical Center-Line)
```html
<!-- Alternating Cards -->
<div class="timeline">
    <div class="timeline-item left">
        <div class="timeline-content">
            <div class="timeline-marker"></div>
            <!-- Content -->
        </div>
    </div>
    <div class="timeline-item right">
        <!-- Alternating side -->
    </div>
</div>
```

### Stats Grid
```html
<!-- 4-Column Responsive Grid -->
<div class="stats-grid">
    <div class="stat-card">
        <div class="stat-number">9,500</div>
        <div class="stat-label">Years BP</div>
    </div>
    <!-- Repeat... -->
</div>
```

## Cultural Elements

### Berber Pattern
The site uses a subtle Berber geometric pattern as a background element:
```css
background-image: url('img/berber-pattern.svg');
opacity: 0.08;                    /* Very subtle */
background-size: 300px;
background-repeat: repeat;
```

Apply to:
- Body background
- Header overlay
- Hero section backgrounds

### Emojis (Contextual Only)
Use **meaningful, contextual emojis** that add explanatory value:

**Approved emojis:**
- 🧬 Genetic/DNA content
- 🏔️ Geography/Mountains
- 🌿 Nature/Argan trees
- 🏛️ Historical sites
- 🗣️ Language/Communication
- 👥 Community/People
- 📜 Historical documents
- 🗺️ Maps/Regions
- ⏱️ Time/Dating
- 🔬 Science/Research
- ✉️ Contact/Email
- 👋 Greetings
- 🔒 Privacy/Security

**NEVER use:**
- Decorative or childish emojis
- Multiple emojis in succession
- Emojis without clear contextual meaning

## Content Tone & Voice

### Writing Style
- **Scholarly but accessible**: Scientific accuracy without jargon overload
- **Professional**: Formal academic tone
- **Personal yet objective**: First-person narrative grounded in data
- **Culturally respectful**: Celebrate heritage without exoticization
- **Data-driven**: Always cite sources, dates, and genetic markers

### Terminology
- Use **Amazigh** (not "Berber" alone when possible)
- Use **Anti-Atlas Mountains** (not just "Atlas")
- Use **Tachelhit** for the language (not "Tashelhit" or "Shilha")
- Use proper haplogroup notation: **E-M81 (E-PF2546)**, **H1 (H1c)**
- Date format: **Years BP** (Before Present) or **BCE/CE**

### Example Phrases
✅ "The E-PF2546 subclade emerged approximately 2,400 years BP"  
✅ "Maternal haplogroup H1 traces back 9,500-10,800 years"  
✅ "The Aït M'Hend lineage reflects deep Amazigh roots"

❌ "My DNA is super cool and ancient!"  
❌ "Berber genes are the best"  
❌ "Check out this awesome DNA stuff"

## Technical Stack

### Core Technologies
- **HTML5/CSS3** - Static site, no build process
- **Mermaid.js v10** - Phylogenetic tree diagrams
- **Chart.js** - Data visualization
- **Formspree** - Contact form handling
- **GitHub Pages** - Hosting

### File Structure
```
aitmhend-dna.github.io/
├── index.html              # Homepage
├── lineage.html            # Lineage analysis
├── genetics.html           # DNA science
├── culture.html            # Cultural heritage
├── contact.html            # Contact form
├── css/
│   └── styles.css          # All styles (3255 lines)
├── js/                     # Future JavaScript
├── img/                    # All images
├── docs/                   # Documentation
├── README.md
├── .gitignore
├── robots.txt
├── sitemap.xml
└── site.webmanifest
```

## Code Standards

### CSS
- Use **CSS custom properties** for colors
- Follow **BEM naming** for components when possible
- Keep **specificity low** (avoid deep nesting)
- Use **rem units** for spacing/typography
- **Mobile-first** responsive design
- Border radius: **3-8px maximum**

### HTML
- **Semantic HTML5** elements
- Proper **heading hierarchy** (h1 → h2 → h3)
- **Alt text** for all images
- **ARIA labels** for accessibility
- **Meta tags** for SEO

### Images
- Use **WebP format** when possible
- Provide **alt text** describing content
- Maintain **aspect ratios** (use object-fit)
- Optimize file sizes (<500KB per image)

## Consistency Rules

### ❌ NEVER Do
- Use blue colors (#0000FF, #1E90FF, etc.)
- Add excessive animations or transitions
- Use decorative left borders on sections
- Create large gradient banners/heroes
- Use circular badges or rounded bubbles (>8px radius)
- Add childish or decorative emojis
- Mix cultural themes (stay Berber/Anti-Atlas focused)
- Use Comic Sans or unprofessional fonts
- Create cluttered layouts with too many elements

### ✅ ALWAYS Do
- Use terracotta/ochre color palette
- Keep designs flat and minimal
- Use sharp corners (3-8px radius)
- Maintain scholarly, professional tone
- Add contextual, meaningful emojis only
- Ensure button text is clearly visible (white on terracotta)
- Reference Berber/Amazigh cultural heritage
- Cite genetic data sources and dates
- Test on mobile devices
- Maintain accessibility standards

## Future Development

### Planned Features
- Interactive genetic map visualization
- Ancestral migration path animation
- Photo gallery of Anti-Atlas region
- Audio recordings of Tachelhit language
- Family tree interactive diagram

### Maintenance Guidelines
- Update genetic research annually (new findings)
- Keep copyright dates current
- Monitor form submissions (Formspree)
- Update sitemap.xml when adding pages
- Maintain image optimization
- Test cross-browser compatibility

## Contact & Support

**Site Owner:** Amadeus (aitmhend-dna)  
**Email:** aitmhend-dna@outlook.com  
**GitHub:** https://github.com/aitmhend-dna  
**Form:** Formspree ID: myzbzgjn

---

**Last Updated:** January 17, 2026  
**Version:** 2.0 - Berber Cultural Redesign

## AI Assistant Instructions

When working on this project:
1. **Preserve the Berber cultural identity** - never suggest blue colors or generic designs
2. **Maintain design consistency** - follow the color palette and component patterns exactly
3. **Keep it professional** - scholarly tone, no casual language
4. **Respect the cultural context** - use proper terminology (Amazigh, Tachelhit, Anti-Atlas)
5. **Ensure accessibility** - maintain contrast ratios, alt text, semantic HTML
6. **Think mobile-first** - all designs must work on small screens
7. **Stay data-driven** - cite sources for genetic information
8. **Avoid feature creep** - keep it simple and focused on core content

**If suggesting changes:**
- Explain how they align with Berber cultural theme
- Show color codes from the approved palette
- Demonstrate mobile responsiveness
- Maintain scholarly tone in copy
- Preserve existing design patterns
