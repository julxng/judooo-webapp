# Judooo Brand Guidelines

**Project**: Judooo Art Event Discovery Platform
**Version**: 1.0
**Last Updated**: January 2025

---

## Brand Identity

Judooo is a vibrant, contemporary platform dedicated to discovering and celebrating Vietnamese art and culture. Our brand identity reflects creativity, energy, and accessibility.

## Brand Assets

**Logo & Favicon**: Available in [Google Drive](https://drive.google.com/drive/folders/1OY0aoB14R9q8f0m9kvaGWdLE7hACnQAE)
- `judooo_Logo.ai` - Editable vector logo
- `judooo_Favicon.svg` - SVG favicon
- `judooo_Favicon.ai` - Editable AI format
- `judooo_Favicon.png` - PNG format

---

## Color Palette

### Primary Brand Color
**Judooo Red** (Energy & Passion)
- **Hex**: `#FF5533` (or `#FF6B35` for lighter variation)
- **RGB**: `RGB(255, 85, 51)`
- **HSL**: `HSL(10, 100%, 60%)`
- **Usage**: Logo, primary buttons, CTAs, highlights, accents

### Secondary Colors
**White**
- **Hex**: `#FFFFFF`
- **RGB**: `RGB(255, 255, 255)`
- **Usage**: Logo text, backgrounds, contrast elements

**Dark Gray** (Optional for text)
- **Hex**: `#2C3E50` or `#333333`
- **RGB**: `RGB(44, 62, 80)` or `RGB(51, 51, 51)`
- **Usage**: Body text, secondary elements

**Light Gray** (Optional for UI)
- **Hex**: `#F5F5F5` or `#EFEFEF`
- **RGB**: `RGB(245, 245, 245)` or `RGB(239, 239, 239)`
- **Usage**: Backgrounds, borders, dividers

### Color Applications

**Web Design**:
```css
/* CSS Variables for easy implementation */
:root {
  --color-primary: #FF5533;           /* Judooo Red */
  --color-primary-dark: #E64520;      /* Darker variant */
  --color-primary-light: #FF7A52;     /* Lighter variant */
  --color-white: #FFFFFF;
  --color-dark-gray: #2C3E50;
  --color-light-gray: #F5F5F5;
  --color-border: #EFEFEF;
}
```

**Usage Guide**:
- **Buttons & CTAs**: Use `#FF5533` with white text
- **Hover States**: Use `#E64520` (darker variant)
- **Active States**: Use `#D43A1A` (darkest)
- **Disabled States**: Use `#CCCCCC` or `#F5F5F5`
- **Links**: Use `#FF5533` with underline
- **Borders/Dividers**: Use `#EFEFEF`
- **Backgrounds**: Use `#FFFFFF` or `#F5F5F5`
- **Text**: Use `#2C3E50` (dark) on light backgrounds

---

## Typography

**Font Family**: Nunito Sans
- **Available Weights**: 400 (Regular), 600 (Semi-Bold), 700 (Bold)
- **Character Set**: Latin Extended
- **Import**: Google Fonts or Nunito Sans package

### Font Sizes (Recommended)
- **H1 (Hero)**: 48px - 64px, Bold
- **H2 (Headings)**: 32px - 40px, Bold
- **H3 (Subheadings)**: 24px - 28px, Semi-Bold
- **H4 (Small headings)**: 18px - 20px, Semi-Bold
- **Body**: 16px, Regular
- **Small text**: 14px, Regular
- **Caption**: 12px, Regular

### Google Fonts Import
```html
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Nunito+Sans:ital,wght@0,400;0,600;0,700;1,400&display=swap" rel="stylesheet">
```

---

## Logo Usage

### Primary Logo
- Use on white or light backgrounds
- Minimum size: 120px width
- Clear space: Maintain padding around logo
- Never distort or stretch the logo
- Never change colors (except for specific use cases)

### Favicon
- Red circular badge with white "judooo" text
- Use in browser tabs and bookmarks
- Available sizes: 16x16, 32x32, 64x64, 192x192, 512x512
- SVG version preferred for web

### Logo Variations
- **On White**: Use full color `#FF5533`
- **On Red**: Use white version
- **Monochrome**: Use `#2C3E50` if needed

---

## Visual Style

### Button Styles

**Primary Button**
```css
Background: #FF5533
Color: white
Padding: 12px 24px
Border-radius: 6px
Font-weight: 600
Transition: background 0.3s ease
Hover: background #E64520
Active: background #D43A1A
```

**Secondary Button**
```css
Background: #F5F5F5
Color: #2C3E50
Border: 1px solid #EFEFEF
Padding: 12px 24px
Border-radius: 6px
Font-weight: 600
Hover: background #EFEFEF
```

### Component Styling

**Cards**
- Background: `#FFFFFF`
- Border: `1px solid #EFEFEF`
- Border-radius: `8px`
- Shadow: `0 2px 8px rgba(0,0,0,0.1)`
- Hover shadow: `0 4px 16px rgba(255,85,51,0.15)`

**Inputs & Form Fields**
- Background: `#FFFFFF`
- Border: `1px solid #EFEFEF`
- Border-radius: `6px`
- Focus border: `2px solid #FF5533`
- Padding: `12px`

**Accents & Highlights**
- Badges: Use `#FF5533` background with white text
- Highlights: Use `#FF5533` with 10-20% opacity for backgrounds
- Icons: Use `#FF5533` for primary icons

---

## Accessibility

### Color Contrast
- **Judooo Red (#FF5533) on White**: WCAG AA compliant ✓
- **White on Judooo Red**: WCAG AAA compliant ✓
- **Always test contrast ratios** for accessibility compliance

### Guidelines
- Use high contrast for text (minimum 4.5:1 ratio)
- Don't rely on color alone to convey information
- Include icons, labels, or patterns with color indicators

---

## Implementation

### Frontend Setup

**Step 1: Add CSS Variables**
```css
/* src/styles/variables.css */
:root {
  --color-primary: #FF5533;
  --color-primary-dark: #E64520;
  --color-primary-light: #FF7A52;
  --color-white: #FFFFFF;
  --color-dark-gray: #2C3E50;
  --color-light-gray: #F5F5F5;
  --color-border: #EFEFEF;
  
  /* Typography */
  --font-primary: 'Nunito Sans', sans-serif;
  --font-size-base: 16px;
  --font-weight-regular: 400;
  --font-weight-semi-bold: 600;
  --font-weight-bold: 700;
}
```

**Step 2: Use in Components**
```jsx
// Example React component
import './styles/variables.css';

function Button({ children, variant = 'primary' }) {
  return (
    <button className={`btn btn--${variant}`}>
      {children}
    </button>
  );
}
```

**Step 3: SCSS/CSS Implementation**
```scss
// src/styles/buttons.css
.btn {
  font-family: var(--font-primary);
  font-weight: var(--font-weight-semi-bold);
  padding: 12px 24px;
  border-radius: 6px;
  transition: all 0.3s ease;
  cursor: pointer;
}

.btn--primary {
  background-color: var(--color-primary);
  color: var(--color-white);
  
  &:hover {
    background-color: var(--color-primary-dark);
  }
  
  &:active {
    background-color: #D43A1A;
  }
}

.btn--secondary {
  background-color: var(--color-light-gray);
  color: var(--color-dark-gray);
  border: 1px solid var(--color-border);
  
  &:hover {
    background-color: var(--color-border);
  }
}
```

---

## Branding Assets Reference

- **Logo Design**: [Google Drive - Brand Design](https://drive.google.com/drive/folders/1OY0aoB14R9q8f0m9kvaGWdLE7hACnQAE)
- **Figma Design**: [Judooo Design File](https://www.figma.com/design/RINHgEbIgrd9nGiunic6JM/Untitled)
- **Color Reference**: Primary: `#FF5533` (Judooo Red)

---

## Best Practices

1. **Consistency**: Always use the official Judooo Red for brand elements
2. **Contrast**: Ensure text meets WCAG accessibility standards
3. **Typography**: Use Nunito Sans exclusively for brand consistency
4. **Spacing**: Maintain consistent padding and margins
5. **Logo**: Never modify, distort, or recolor the official logo
6. **Mobile**: Ensure all brand elements are readable on mobile devices
7. **Testing**: Test all color combinations across different devices and browsers

---

## Questions or Updates?

For branding inquiries or to request color/design changes, refer to the REQUIREMENTS.md and Figma design file.

**Version History**:
- v1.0 - Initial brand guidelines with color palette and typography

