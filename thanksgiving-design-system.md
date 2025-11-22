# Thanksgiving Planning App - Design System & Master Prompt

## Brand Identity & Theme

### Core Theme: "Warm Harvest Celebration"
A sophisticated yet approachable aesthetic that celebrates abundance, togetherness, and the joy of a well-executed feast. The design should feel like a warm kitchen on Thanksgiving morning - organized, inviting, and full of promise.

---

## Color Palette

### Primary Colors (Semantic Tokens)

```
Harvest Orange (Primary Action):
- primary-500: #f59e0b (amber-500) - CTAs, primary buttons
- primary-600: #d97706 (amber-600) - Hover states
- primary-700: #b45309 (amber-700) - Active states

Cranberry Red (Accent/Emphasis):
- accent-500: #dc2626 (red-600) - Important highlights
- accent-600: #b91c1c (red-700) - Hover
- accent-700: #991b1b (red-800) - Active

Sage Green (Success/Fresh):
- success-500: #65a30d (lime-600) - Success states, fresh elements
- success-600: #4d7c0f (lime-700) - Hover

Pumpkin Orange (Warm Secondary):
- warm-400: #fb923c (orange-400) - Light accents
- warm-500: #f97316 (orange-500) - Secondary actions
- warm-600: #ea580c (orange-600) - Hover
```

### Neutral Palette (Warm-tinted)

```
Background & Surface:
- cream-50: #fefdfb - Page background
- cream-100: #fdf8f3 - Card backgrounds
- cream-200: #f5ebe0 - Elevated surfaces

Text Colors:
- brown-900: #44403c (stone-800) - Primary text
- brown-700: #78716c (stone-500) - Secondary text
- brown-500: #a8a29e (stone-400) - Tertiary/disabled

Border Colors:
- border-light: #e7e5e4 (stone-200)
- border-default: #d6d3d1 (stone-300)
- border-strong: #a8a29e (stone-400)
```

### Accent Colors

```
Burgundy (Rich/Elegant):
- burgundy-600: #9f1239 (rose-800)
- burgundy-700: #881337 (rose-900)

Gold (Celebration/Premium):
- gold-400: #fbbf24 (amber-400)
- gold-500: #f59e0b (amber-500)

Copper (Metallic warmth):
- copper-500: #c2410c (orange-700)
```

---

## Typography

### Font Stack
```css
--font-display: 'Georgia', 'Cambria', serif; /* Headers - warm, traditional */
--font-body: system-ui, -apple-system, sans-serif; /* Body - clean, readable */
--font-mono: 'SF Mono', 'Consolas', monospace; /* Times, measurements */
```

### Type Scale for Thanksgiving Content
```
Display (Hero): 3rem / 48px - "Thanksgiving 2025"
H1: 2.25rem / 36px - Section headers
H2: 1.5rem / 24px - Recipe titles
H3: 1.25rem / 20px - Subsection headers
Body: 1rem / 16px - Instructions, descriptions
Small: 0.875rem / 14px - Meta info, hints
Tiny: 0.75rem / 12px - Labels, tags
```

---

## Spacing & Layout

### Content Rhythm
```
Page margins: 1rem (mobile), 2rem (desktop)
Section spacing: 2rem between major sections
Card padding: 1.5rem
List item spacing: 0.5rem
Tight groups: 0.25rem
```

### Grid System
- Mobile: Single column, full width
- Tablet: 2 columns for cards/lists
- Desktop: 3-4 columns for shopping lists, 2 columns for recipes

---

## Component Patterns

### Recipe Cards
```
- Warm cream background (#fdf8f3)
- Left border accent in harvest orange
- Rounded corners (12px)
- Subtle shadow for depth
- Clear hierarchy: Title > Meta > Ingredients > Instructions
```

### Timeline Items
```
- Time badge in harvest orange
- Connecting line in border color
- Highlighted "important" items with warm background
- Checkmark indicators for completed items
```

### Shopping List
```
- Checkbox styling with harvest orange
- Category headers with icons
- Strikethrough for checked items
- Grouped by store section
```

### Info Boxes
```
- Success (sage green left border): Tips, make-ahead notes
- Warning (pumpkin orange left border): Critical timing, oven temps
- Info (burgundy left border): Expert advice, pro tips
```

---

## Iconography

Use food/kitchen-related icons where possible:
- Turkey for main dish
- Carrot for vegetables
- Clock for timing
- Thermometer for temperatures
- Checkbox for shopping
- Calendar for timeline
- Chef hat for tips

---

## Interaction & Motion

### Hover States
- Cards: Subtle lift (-2px) + shadow increase
- Buttons: Darken 10% + slight scale (1.02)
- Links: Underline appears

### Transitions
- Default: 150ms ease-out
- Card hover: 200ms ease-out
- Page sections: No animation (instant)

### Print Styles
- Remove shadows and backgrounds
- Ensure all text is black
- Page breaks between major sections
- Checkboxes printable for shopping lists

---

## Mobile-First Responsive Design

### Breakpoints
```
xs: 0-479px (small phones)
sm: 480px-767px (large phones)
md: 768px-1023px (tablets)
lg: 1024px+ (desktop)
```

### Mobile Optimizations
- Single column layouts
- Larger touch targets (48px minimum)
- Collapsible sections for long content
- Sticky navigation for quick access
- Bottom-positioned primary actions

---

## Accessibility Requirements

### Color Contrast
- All text meets WCAG AA (4.5:1 minimum)
- Interactive elements clearly distinguishable
- Don't rely on color alone (use icons/text)

### Keyboard Navigation
- All interactive elements focusable
- Visible focus indicators
- Logical tab order

### Screen Readers
- Semantic HTML throughout
- Descriptive alt text for decorative elements
- ARIA labels for icon-only buttons

---

## Content Guidelines

### Voice & Tone
- Encouraging and supportive ("You've got this!")
- Clear and actionable ("Remove turkey when...")
- Warm but not overly casual
- Expert but approachable

### Microcopy Patterns
```
Timing: "11:00 AM - Turkey goes in"
Tips: "Pro tip: Save the backbone for stock"
Warnings: "Critical: Check temperature before serving"
Success: "You did it! Time to enjoy your feast!"
```

---

## Design Principles for This Project

1. **Clarity over cleverness** - Cooking is stressful; make everything obvious
2. **Scannability** - Users will glance while cooking; use bold headers and clear hierarchy
3. **Progressive disclosure** - Show essentials first, details on demand
4. **Forgiving** - Include backup plans and timing buffers
5. **Celebratory** - This is a joyful occasion; let the design reflect that

---

## Implementation Notes

### CSS Custom Properties
```css
:root {
  /* Colors */
  --color-primary: #f59e0b;
  --color-accent: #dc2626;
  --color-success: #65a30d;
  --color-background: #fefdfb;
  --color-surface: #fdf8f3;
  --color-text: #44403c;
  --color-text-secondary: #78716c;
  --color-border: #e7e5e4;

  /* Typography */
  --font-display: Georgia, serif;
  --font-body: system-ui, sans-serif;

  /* Spacing */
  --space-xs: 0.25rem;
  --space-sm: 0.5rem;
  --space-md: 1rem;
  --space-lg: 1.5rem;
  --space-xl: 2rem;

  /* Borders */
  --radius-sm: 4px;
  --radius-md: 8px;
  --radius-lg: 12px;
  --radius-xl: 16px;
}
```

This design system creates a cohesive, warm, and functional experience that makes the daunting task of Thanksgiving planning feel achievable and even enjoyable.
