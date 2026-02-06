# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a **static HTML email template showcase** for Pampered Chef verification code emails. The project displays three distinct email template designs (plus one final combined design) for account verification with 6-digit numeric codes. This is a **design showcase/preview tool**, not an application that sends emails.

**Key Points:**
- No build system, no tests, no package manager
- Pure HTML/CSS with vanilla JavaScript for navigation
- Opens directly in browser (`index.html`)
- All templates follow the Pampered Chef Cookbook Design System

## Architecture & Design System

### Design System Foundation

The project strictly follows the **Pampered Chef Cookbook Design System** with centralized design tokens in `styles.css`:

```
:root {
  --pc-color-primary: #1a5962;
  --pc-color-primary-dark: #124248;
  --pc-font-family: 'Inter', ...;
  --pc-font-questa: 'Questa', Georgia, ...;
  --pc-spacing-xs through --pc-spacing-xxl
  --pc-radius-sm through --pc-radius-lg
  /* etc. */
}
```

**All custom classes use the `pc-` prefix** (Pampered Chef) to namespace the design system. Never create classes without this prefix.

### Custom Fonts

The project uses two font families:
- **Inter**: Body text and UI elements (loaded from Google Fonts)
- **Questa**: Display headings (loaded from external WOFF2 source in `styles.css`)

Questa is used specifically for `.pc-email-title-questa` elements to match brand guidelines.

### Template Structure

The `index.html` contains **four email templates**:

1. **Template Final** (`#templateFinal`): The production-ready combined design (Template 2 + Template 3 benefits)
2. **Template 1** (`#playground` → `data-playground="template1"`): Direct & Efficient (VTEX-inspired)
3. **Template 2** (`#playground` → `data-playground="template2"`): Trust-Focused & Branded (Target-inspired)
4. **Template 3** (`#playground` → `data-playground="template3"`): Welcoming & Helpful (Layers-inspired)

### Navigation System

- Main navigation switches between "Template Final" and "Playground Templates"
- Playground has a **dropdown submenu** (activated on hover or click) to switch between Templates 1-3
- All navigation is JavaScript-driven with `data-template` and `data-playground` attributes
- Active states use the `.active` class on nav links, sections, and previews

### Countdown Timer

All templates include a **live countdown timer** that shows code expiration:
- Initialized via `data-expiry="1800"` (30 minutes in seconds)
- JavaScript updates `.countdown-timer` elements every second
- Shows minutes remaining, counting down from 30 to 0

## File Structure

```
/
├── index.html                  # Main showcase file with all templates
├── styles.css                  # Complete design system + all template styles
├── assets/
│   ├── pc-logo-color.svg       # Pampered Chef brand logo
│   └── Reset Password/
│       └── email-validation-illustration.svg
├── instructions/
│   └── code-validation-email.md  # Original design brief & requirements
└── references/                 # Reference email screenshots (Amazon, Target, etc.)
```

## Email Template Implementation Pattern

All email templates use a **table-based layout** for maximum email client compatibility:

```html
<table class="pc-email-table" cellpadding="0" cellspacing="0">
  <tr>
    <td class="pc-email-container template-name">
      <!-- Email content here -->
    </td>
  </tr>
</table>
```

**Critical email client requirements:**
- Inline CSS only (not implemented yet, but planned for production)
- Table-based layouts for compatibility
- Minimal external dependencies
- Fallback fonts and colors
- No JavaScript in actual email templates (the countdown timer is for preview only)

## Verification Code Display Patterns

Each template uses different code display strategies:

- **Template 1 (VTEX)**: Simple large monospace display with tint background
- **Template 2 (Target)**: Individual spaced digits with `.pc-code-digit` spans
- **Template 3 (Layers)**: Clean centered display in a card
- **Template Final**: Large code in colored box (`.pc-final-code-box`)

All use the `.pc-verification-code-unified` class as base styling (3rem, monospace, accent color).

## Design Requirements (from instructions/code-validation-email.md)

When modifying templates, ensure they meet:

- **Code Format**: Exactly 6-digit numeric (currently hardcoded as `847291`)
- **Accessibility**: WCAG AA contrast, semantic HTML, min 14px body text
- **Mobile-First**: Responsive at 480px, 768px, 1024px+
- **Email Clients**: Must render in Gmail, Outlook, Apple Mail, Yahoo Mail
- **Security Messaging**: Include "didn't request this?" recovery path
- **Expiration**: Show 30-minute countdown and code expiration notice

### Content Placeholders (Not Implemented)

The design brief specifies these variables for production integration:
- `{USER_NAME}`, `{VERIFICATION_CODE}`, `{EXPIRATION_TIME}`, `{COMPANY_NAME}`, `{SUPPORT_EMAIL}`, `{SECURITY_POLICY_URL}`

Currently, the templates use **hardcoded content** for preview purposes.

## Responsive Breakpoints

The CSS defines three breakpoints:
- **992px**: Switch sidebar to stacked layout
- **640px**: Mobile adjustments for code size, padding, footer layout
- **768px**: (Mentioned in requirements but not explicitly used in current CSS)

## Color Palette

Primary brand colors:
- **Primary**: `#1a5962` (teal - used for buttons, links, code)
- **Success**: `#42af00` (green - used for checkmarks in benefits lists)
- **Text**: `#2f3031` (primary), `#45474a` (secondary), `#6b6c70` (tertiary)
- **Surface**: `#ffffff` (light), `#f3f6f6` (tint), `#e1eef0` (tint-2)

## Working with This Codebase

### To Preview
Open `index.html` directly in a browser. No build process needed.

### To Modify Templates
1. Edit the HTML structure in `index.html` (search for the template section by ID)
2. Update styles in `styles.css` (organized by template and component)
3. Always use `pc-` prefixed classes from the design system
4. Test responsive behavior at all breakpoints

### To Add New Components
1. Define tokens in `:root` if introducing new colors/spacing
2. Create new `.pc-*` classes following the existing pattern
3. Ensure email client compatibility (tables, inline styles for production)

### Common Gotchas
- The **playground dropdown** only shows when "Playground Templates" nav item is active
- Template sections use `display: none` by default, `.active` class shows them
- SVG icons are inline for email compatibility (no external icon libraries)
- Countdown timer won't work in actual email clients (for preview only)
- Email client testing requires export to inline CSS (not currently implemented)

## Brand Voice & Messaging

From the design brief:
- **Template 1**: Fast, efficient, minimal copy
- **Template 2**: Trust-focused, brand personality, reassuring
- **Template 3**: Helpful, generous copy, support-oriented
- **Template Final**: Combines trust/brand (T2) with benefits/support (T3)

All templates include:
- Clear code prominence
- Expiration urgency (30 minutes)
- "Didn't request this?" recovery messaging
- Security reassurance
