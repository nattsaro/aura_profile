# Aura Profile - Style Guide

A comprehensive design system documentation for the Aura Profile (Linktree-style portfolio builder).

---

## Table of Contents

1. [Overview](#overview)
2. [Design Philosophy](#design-philosophy)
3. [Color Palette](#color-palette)
4. [Typography System](#typography-system)
5. [Spacing System](#spacing-system)
6. [Component Styles](#component-styles)
7. [Shadows & Elevation](#shadows--elevation)
8. [Border Radius](#border-radius)
9. [Opacity & Transparency](#opacity--transparency)
10. [Animations & Transitions](#animations--transitions)
11. [Layout & Grid System](#layout--grid-system)
12. [Responsive Design](#responsive-design)
13. [Common Patterns & Best Practices](#common-patterns--best-practices)
14. [Example Component Code](#example-component-code)

---

## Overview

**Project Name:** Aura Profile
**Purpose:** A personal profile and portfolio showcase page inspired by Linktree design patterns
**Framework:** Vanilla HTML/CSS (no dependencies)
**Font:** Geist Mono (monospace font family)
**Layout Type:** Fixed-width (580px) on desktop, responsive full-width on mobile
**Color Scheme:** Minimalist, light-based with selective use of brand colors

### Key Characteristics
- **Minimalist Design:** Clean, spacious layouts with subtle visual hierarchy
- **Fixed-Width Container:** 580px width on desktop for focused content presentation
- **Responsive Mobile:** Full-width adaptation below 640px breakpoint
- **Card-Based Architecture:** Modular card system for content organization
- **Light Typography:** Ultra-thin font weights (100-200) for refined appearance
- **Subtle Shadows:** Dual-layer shadow system for depth without heaviness

---

## Design Philosophy

The Aura Profile design system follows these core principles:

1. **Clarity over Decoration** - Clean surfaces with minimal visual noise
2. **Condensed Typography** - Negative letter-spacing (-0.02em, -0.05em) for tightness
3. **Micro Interactions** - Subtle hover states and transitions (0.2s ease)
4. **Color Restraint** - White base with accent colors from brand platforms
5. **Spatial Breathing** - 4px-based spacing system for consistency
6. **Monospace Aesthetic** - Tech-forward, programmer-friendly typography

---

## Color Palette

### Primary Colors

| Color Name | Hex Code | Usage | RGB |
|-----------|----------|-------|-----|
| **White** | `#ffffff` | Page background, card background | 255, 255, 255 |
| **Black** | `#000000` | Primary text, dark icons | 0, 0, 0 |
| **Blue (Accent)** | `#0B1BFF` | Avatar border, primary accent | 11, 27, 255 |
| **Light Grey** | `#f0f0f0` | Subtle backgrounds, borders | 240, 240, 240 |
| **Medium Grey** | `#999999` | Secondary text, subtitles | 153, 153, 153 |
| **Dark Grey** | `#666666` | Tertiary text, labels | 102, 102, 102 |
| **Very Light Grey** | `#e5e5e5` | Card borders | 229, 229, 229 |
| **Neutral Grey** | `#e8e8e8` | Map placeholder backgrounds | 232, 232, 232 |
| **Light Grey (UI)** | `#e0e0e0` | Placeholder images | 224, 224, 224 |

### Brand Platform Colors

| Platform | Color | Hex | Usage |
|----------|-------|-----|-------|
| **LinkedIn** | Sky Blue | `#007EBB` | Icon background |
| **GitHub** | Black | `#000000` | Icon background |
| **Spotify** | Green | `#1ED760` | Icon & button background |
| **Twitter** | Sky Blue | `#55ACEE` | Icon & button background |
| **YouTube** | Red | `#FF0000` | Icon background |
| **Instagram** | Purple Gradient | `#667eea → #764ba2` | Icon gradient |
| **Behance** | Blue | `#2F65EE` | Icon & button background |
| **Twitch** | Purple | `#9146FF` | Icon background |
| **Figma** | Dark Grey | `#3E3E3E` | Icon background |
| **LeetCode** | Orange | `#FFA500` | Icon background |

### Card Background Gradients

Cards use subtle gradient backgrounds (135° angle) to add visual depth:

| Card | Gradient | Start | End |
|------|----------|-------|-----|
| **LinkedIn** | Light Blue | `#f0f6f9` | `#ffffff` |
| **Spotify** | Light Green | `#edfcf3` | `#ffffff` |
| **Twitter** | Light Blue | `#f5fafe` | `#ffffff` |
| **YouTube** | Light Red | `#fff0f0` | `#ffffff` |
| **Behance** | Light Blue | `#f4f7fe` | `#ffffff` |
| **Twitch** | Light Purple | `#faf0ff` | `#ffffff` |
| **Map** | Light Grey | `#f9f9f9` | `#ffffff` |
| **GitHub** | White (Solid) | `#ffffff` | — |
| **Figma** | White (Solid) | `#ffffff` | — |
| **LeetCode** | White (Solid) | `#ffffff` | — |
| **Instagram** | White (Solid) | `#ffffff` | — |
| **Portfolio** | White (Solid) | `#ffffff` | — |

### Opacity & Color Overlays

```css
/* Modal Overlay */
background-color: rgba(0, 0, 0, 0.5);  /* 50% black transparency */

/* Top Button Background */
background-color: rgba(187, 187, 187, 0.2);  /* #BBBBBB at 20% opacity */

/* Top Button Hover */
background-color: rgba(255, 255, 255, 0.9);  /* White at 90% opacity */
```

---

## Typography System

### Font Family

**Primary Font:** Geist Mono
**Type:** Monospace
**Origin:** Google Fonts
**Import:** `https://fonts.googleapis.com/css2?family=Geist+Mono:wght@400;500;600;700`

### Font Weights & Hierarchy

| Weight | CSS Value | Usage | Visual | Notes |
|--------|-----------|-------|--------|-------|
| **Thin** | `100` | Primary headings, card titles, labels | Very light, refined | Used for h1, card-title, labels |
| **Light** | `200` | Buttons, portfolio text | Light & minimal | card-button, inline text |
| **Regular** | `400` | Body text (not heavily used) | Normal | Fallback weight |
| **Medium** | `500` | Not used in current design | — | Reserved for future use |
| **Semi-Bold** | `600` | Not used in current design | — | Reserved for future use |
| **Bold** | `700` | Not used in current design | — | Reserved for future use |

### Font Size Scale

| Size | Usage | Context |
|------|-------|---------|
| **40px** | Profile name (h1) | Main header, highest prominence |
| **24px** | Portfolio text ("mr") | Large accent text |
| **16px** | Card titles, body text | Primary card content |
| **14px** | Card subtitles, username | Secondary information |
| **13px** | Instagram follower count | Tertiary information |
| **12px** | Not used (reserved) | — |

### Line Height

```css
line-height: 1.5;  /* Applied to profile description paragraphs */
```

### Letter Spacing

| Value | Application | Visual Effect |
|-------|-------------|---------------|
| `-0.02em` | Global body default | Subtle condensing, -2% |
| `-0.05em` | Profile name (h1) | More condensed, -5% |

**Note:** Negative letter-spacing creates a tight, modern appearance consistent with contemporary design trends.

### Typography Combinations

#### Profile Header
```
h1 (Profile Name)
  font-size: 40px
  font-weight: 100
  letter-spacing: -0.05em
  margin-bottom: 0px
  color: #000

p (Username)
  font-size: 14px
  font-weight: 300 (inherited)
  color: #999
  margin-bottom: 24px
  margin-top: -4px

p (Description)
  font-size: 16px
  color: #666
  line-height: 1.5
```

#### Card Title + Subtitle
```
.card-title
  font-size: 16px
  font-weight: 100
  margin-bottom: 6px

.card-subtitle
  font-size: 14px
  color: #999
  margin-bottom: 12px
```

#### Buttons
```
.card-button
  font-size: 14px
  font-weight: 100
  padding: 8px 16px
```

---

## Spacing System

The spacing system is based on a **4px unit increment**, following modern design system standards (similar to Tailwind CSS).

### Base Unit
```
1 unit = 4px
```

### Spacing Scale

| Value | Units | Usage |
|-------|-------|-------|
| **4px** | 1 | Micro-spacing (username top margin) |
| **6px** | 1.5 | Card title bottom margin |
| **8px** | 2 | Button padding, small gaps |
| **12px** | 3 | Medium gaps (card icon margin-bottom) |
| **16px** | 4 | Standard gaps (card padding internal) |
| **20px** | 5 | Grid gaps, gaps between cards |
| **24px** | 6 | Card padding, section spacing |
| **32px** | 8 | Link bento icon-to-text gap |
| **40px** | 10 | Grid margin-bottom, section breaks |
| **60px** | 15 | Header section margin-bottom |

### Padding

| Component | Padding | Notes |
|-----------|---------|-------|
| **Profile Container (Desktop)** | `60px 20px` | 60px vertical, 20px horizontal |
| **Profile Container (Mobile)** | `40px 16px` | Reduced on smaller screens |
| **Card** | `24px` | All sides |
| **Card Button** | `8px 16px` | 8px vertical, 16px horizontal |
| **Play Button (Spotify)** | `10px 24px` | Custom sizing |
| **Modal Content** | `40px` | All sides |

### Margins

#### Vertical Spacing
```css
h1 { margin-bottom: 0px; }
.username { margin-top: -4px; margin-bottom: 24px; }
.header-section { margin-bottom: 60px; }
.grid-container { margin-bottom: 40px; }
.card-icon { margin-bottom: 16px; }
.card-title { margin-bottom: 6px; }
.card-subtitle { margin-bottom: 12px; }
```

#### Grid Gaps
```css
.grid-container { gap: 20px; }
.youtube-card { gap: 20px; }
.instagram-card { gap: 20px; }
.portfolio-card { gap: 20px; }
.instagram-grid { gap: 8px; }
```

---

## Component Styles

### Profile Container

The main wrapper that contains all content.

```css
.profile-container {
  width: 580px;
  padding: 60px 20px;
  background-color: #ffffff;
  border-radius: 24px;
  box-shadow: 0 1px 3px rgba(0, 0, 0, 0.06), 0 4px 12px rgba(0, 0, 0, 0.05);
  position: relative;
}

/* Mobile Override */
@media (max-width: 640px) {
  .profile-container {
    width: 100%;
    padding: 40px 16px;
    border-radius: 0;
    box-shadow: none;
  }
}
```

### Avatar Component

Circular profile image with blue border accent.

**Specifications:**
- **Size:** 120px × 120px
- **Border:** 4px solid `#0B1BFF` (blue)
- **Border Radius:** 50% (perfect circle)
- **Box Shadow:** `0 4px 12px rgba(0, 0, 0, 0.1)`

```css
.avatar {
  width: 120px;
  height: 120px;
  border-radius: 50%;
  margin: 0 auto 24px;
  overflow: hidden;
  border: 4px solid #0B1BFF;
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
}

.avatar img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}
```

### Card Component (Base)

Standard card design used throughout the layout.

**Specifications:**
- **Border Radius:** 24px
- **Padding:** 24px
- **Border:** 1px solid `#e5e5e5`
- **Min Height:** 200px
- **Shadow:** Dual-layer subtle shadow
- **Layout:** Flex column, space-between

```css
.card {
  border-radius: 24px;
  padding: 24px;
  border: 1px solid #e5e5e5;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  min-height: 200px;
  cursor: pointer;
  text-decoration: none;
  color: inherit;
  box-shadow: 0 1px 3px rgba(0, 0, 0, 0.06), 0 4px 12px rgba(0, 0, 0, 0.05);
}
```

### Card Icon

Icon container within cards, provides colored background.

**Specifications:**
- **Size:** 48px × 48px
- **Border Radius:** 12px
- **Margin Bottom:** 16px
- **Font Size:** 24px

```css
.card-icon {
  width: 48px;
  height: 48px;
  border-radius: 12px;
  display: flex;
  align-items: center;
  justify-content: center;
  margin-bottom: 16px;
  font-size: 24px;
}
```

**Platform-Specific Icon Colors:**

```css
.linkedin-icon { background-color: #007EBB; color: white; }
.spotify-icon { background-color: #1ED760; color: white; }
.github-icon { background-color: #000; color: white; }
.twitter-icon { background-color: #55ACEE; color: white; }
.youtube-icon { background-color: #FF0000; color: white; }
.instagram-icon { background: linear-gradient(135deg, #667eea 0%, #764ba2 100%); color: white; }
.behance-icon { background-color: #2F65EE; color: white; }
.twitch-icon { background-color: #9146FF; color: white; }
.figma-icon { background-color: #3E3E3E; color: white; }
.leetcode-icon { background-color: #FFA500; color: white; }
```

### Card Title

Primary content title within cards.

```css
.card-title {
  font-size: 16px;
  font-weight: 100;
  margin-bottom: 6px;
  color: #000;
}
```

### Card Subtitle

Secondary content label within cards.

```css
.card-subtitle {
  font-size: 14px;
  color: #999;
  margin-bottom: 12px;
}
```

### Card Button (Unified Style)

Call-to-action buttons within cards (Follow, Play, etc.). All buttons use unified styling with platform-specific colors.

**Base Button Style:**
```css
.card-button {
  padding: 8px 16px;              /* Consistent padding */
  border-radius: 20px;             /* Pill-shaped */
  border: none;
  font-size: 14px;
  font-weight: 100;                /* Light weight */
  cursor: pointer;
  transition: all 0.2s ease;       /* Smooth transitions */
  margin-top: auto;                /* Push to bottom of card */
  align-self: flex-start;          /* Button width only, not full width */
}
```

**Platform-Specific Colors (Unified Styling):**

| Platform | Color | Hex | Usage |
|----------|-------|-----|-------|
| **GitHub** | Light Grey | `#f0f0f0` | Follow button |
| **Twitter** | Sky Blue | `#55ACEE` | Follow button |
| **Spotify** | Green | `#1ED760` | Play button |
| **Behance** | Blue | `#2F65EE` | Follow button |

```css
/* All buttons use same base style, only background color changes */
.github-card .card-button {
  background-color: #f0f0f0;
  color: #000;
}

.twitter-card .card-button {
  background-color: #55ACEE;
  color: white;
}

.spotify-card .play-button {
  background-color: #1ED760;
  color: white;
}

.behance-card .card-button {
  background-color: #2F65EE;
  color: white;
}
```

**Button Specifications:**
- **Size:** Medium (8px × 16px padding)
- **Shape:** Pill-shaped (20px border-radius)
- **Weight:** Light (100)
- **Text Color:** White (or black for light backgrounds)
- **Position:** Bottom-left of card (margin-top: auto, align-self: flex-start)
- **Transition:** 0.2s ease for smooth hover effects

### Play Button (Spotify Special)

Custom button for Spotify card with branded green.

```css
.play-button {
  background-color: #1ED760;
  color: white;
  padding: 10px 24px;
  border-radius: 20px;
  border: none;
  font-weight: 100;
  cursor: pointer;
  margin-top: 12px;
  transition: all 0.2s ease;
}
```

### Top Buttons

Action buttons positioned at top corners of profile.

**Specifications:**
- **Size:** 48px × 48px
- **Border Radius:** 50% (circle)
- **Background:** `rgba(187, 187, 187, 0.2)` (#BBBBBB at 20%)
- **Backdrop Filter:** Blur 10px
- **Gap:** Space-between (left and right positioning)

```css
.top-buttons {
  position: absolute;
  top: 20px;
  left: 20px;
  right: 20px;
  display: flex;
  justify-content: space-between;
  z-index: 100;
}

.top-button {
  width: 48px;
  height: 48px;
  border-radius: 50%;
  border: none;
  background-color: rgba(187, 187, 187, 0.2);
  cursor: pointer;
  display: flex;
  align-items: center;
  justify-content: center;
  backdrop-filter: blur(10px);
}

.top-button:hover {
  background-color: rgba(255, 255, 255, 0.9);
}

.top-button svg {
  width: 20px;
  height: 20px;
}
```

### Modal Component

Dialog box for sharing profile functionality.

```css
.modal {
  display: none;
  position: fixed;
  z-index: 200;
  left: 0;
  top: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.5);
}

.modal.active {
  display: flex;
  align-items: center;
  justify-content: center;
}

.modal-content {
  background-color: white;
  padding: 40px;
  border-radius: 24px;
  width: 90%;
  max-width: 500px;
  text-align: center;
  position: relative;
}

.modal-close {
  position: absolute;
  top: 20px;
  right: 20px;
  font-size: 28px;
  background: none;
  border: none;
  cursor: pointer;
  color: #666;
}
```

### Specialized Card Components

#### Map Card

Full-width card with interactive map visualization.

```css
.map-card {
  grid-column: span 2;
  background: linear-gradient(135deg, #f9f9f9 0%, #ffffff 100%);
}

.map-container {
  position: relative;
  width: 100%;
  height: 220px;
  border-radius: 12px;
  background: linear-gradient(135deg, #e8e8e8 0%, #f5f5f5 100%);
  margin-bottom: 16px;
  overflow: hidden;
  display: flex;
  align-items: center;
  justify-content: center;
}

.map-pin {
  position: absolute;
  width: 32px;
  height: 32px;
  background-color: #5B9EFF;
  border-radius: 50%;
  border: 3px solid white;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.15);
}

.map-label {
  position: absolute;
  bottom: 12px;
  left: 12px;
  font-size: 14px;
  font-weight: 100;
  color: #666;
}
```

#### YouTube Card

Media card with thumbnail preview.

```css
.youtube-card {
  background: linear-gradient(135deg, #fff0f0 0%, #ffffff 100%);
  grid-column: span 2;
  display: flex;
  gap: 20px;
}

.youtube-content {
  flex: 1;
}

.youtube-thumbnail {
  width: 180px;
  height: 100px;
  border-radius: 12px;
  object-fit: cover;
  background-color: #e0e0e0;
}
```

#### Instagram Card

Social grid card with feed-like layout.

```css
.instagram-card {
  background: linear-gradient(135deg, #ffffff 0%, #ffffff 100%);
  grid-column: span 2;
  display: flex;
  gap: 20px;
}

.instagram-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 8px;
  margin-top: 12px;
}

.instagram-grid-item {
  width: 100%;
  aspect-ratio: 1;
  background-color: #f0f0f0;
  border-radius: 8px;
}
```

#### Portfolio Card

Content showcase card with thumbnail.

```css
.portfolio-card {
  background: linear-gradient(135deg, #ffffff 0%, #ffffff 100%);
  grid-column: span 2;
  display: flex;
  gap: 20px;
  align-items: center;
}

.portfolio-thumbnail {
  width: 200px;
  height: 120px;
  border-radius: 12px;
  background: linear-gradient(135deg, #e0e0e0 0%, #f0f0f0 100%);
  display: flex;
  align-items: center;
  justify-content: center;
  font-weight: 200;
  color: #999;
}
```

---

## Shadows & Elevation

The shadow system creates depth and hierarchy through dual-layer shadows.

### Shadow Specifications

#### Primary Shadow (Subtle)
```css
box-shadow: 0 1px 3px rgba(0, 0, 0, 0.06), 0 4px 12px rgba(0, 0, 0, 0.05);
```
- **First Layer:** 1px vertical offset, 3px blur, 6% black opacity (close shadow)
- **Second Layer:** 4px vertical offset, 12px blur, 5% black opacity (distant shadow)
- **Effect:** Creates soft, minimal elevation
- **Usage:** Cards, profile container

#### Avatar Shadow
```css
box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
```
- **Single Layer:** 4px vertical offset, 12px blur, 10% black opacity
- **Effect:** Subtle definition for circular avatar
- **Usage:** Avatar image

#### Map Pin Shadow
```css
box-shadow: 0 2px 8px rgba(0, 0, 0, 0.15);
```
- **Single Layer:** 2px vertical offset, 8px blur, 15% black opacity
- **Effect:** Emphasizes location pin
- **Usage:** Map pin indicator

#### Modal Backdrop
```css
background-color: rgba(0, 0, 0, 0.5);
```
- **Semi-Transparent Black:** 50% opacity overlay
- **Effect:** Darkens background, focuses attention on modal
- **Usage:** Modal overlay

### Shadow Hierarchy

| Component | Shadow Intensity | Use Case |
|-----------|-----------------|----------|
| **Cards** | Subtle (0.06, 0.05) | Primary content containers |
| **Avatar** | Light (0.1) | Profile image emphasis |
| **Map Pin** | Medium (0.15) | Interactive location marker |
| **Modal** | Heavy (0.5 background) | Full-screen overlay |

---

## Border Radius

Border radius creates the signature rounded aesthetic throughout the design.

### Border Radius Scale

| Value | Usage | Components |
|-------|-------|-----------|
| **0px** | Sharp corners | Mobile profile container |
| **8px** | Subtle rounding | Instagram grid items, thumbnails |
| **12px** | Medium rounding | Card icons, map container, thumbnails |
| **20px** | Pill shape | Buttons (card-button, play-button) |
| **24px** | Signature rounding | Cards, profile container, modal |
| **50%** | Circle | Avatar, top buttons |

### Component Border Radius

```css
/* Profile Container */
border-radius: 24px;

/* Cards */
border-radius: 24px;

/* Card Icons */
border-radius: 12px;

/* Buttons */
border-radius: 20px;  /* Pill-shaped */

/* Avatar */
border-radius: 50%;   /* Perfect circle */

/* Top Action Buttons */
border-radius: 50%;   /* Perfect circle */

/* Map Container */
border-radius: 12px;

/* Thumbnails (YouTube, Portfolio, Instagram) */
border-radius: 12px;  /* YouTube, Portfolio */
border-radius: 8px;   /* Instagram grid items */

/* Modal */
border-radius: 24px;
```

---

## Opacity & Transparency

Opacity creates visual hierarchy and depth through transparency levels.

### Opacity Scale

| Value | Usage | Visual Effect |
|-------|-------|---------------|
| **20%** | Top buttons background | Very subtle, allows background show-through |
| **50%** | Modal overlay | Significant darkening, focus on modal |
| **90%** | Top button hover state | Nearly opaque white, high contrast |
| **100%** | Default colors | Fully opaque, standard colors |

### Specific Implementations

#### Top Button (Base State)
```css
background-color: rgba(187, 187, 187, 0.2);  /* 20% opacity */
```
- Grey tint with light transparency
- Allows subtle visibility with backdrop blur effect
- Creates frosted glass appearance

#### Top Button (Hover State)
```css
background-color: rgba(255, 255, 255, 0.9);  /* 90% opacity */
```
- Nearly opaque white
- High contrast against darker backgrounds
- Clear visual feedback

#### Modal Overlay
```css
background-color: rgba(0, 0, 0, 0.5);  /* 50% opacity */
```
- Darkens entire background
- Focuses user attention on modal content
- Creates visual separation

### Color Opacity Variations

```css
/* Subtle Background Colors (using opacity) */
rgba(0, 0, 0, 0.06)      /* 6% - Lightest shadows */
rgba(0, 0, 0, 0.05)      /* 5% - Very light shadows */
rgba(0, 0, 0, 0.1)       /* 10% - Light shadows */
rgba(0, 0, 0, 0.15)      /* 15% - Medium shadows */
```

---

## Animations & Transitions

The design uses minimal, purposeful animations for micro-interactions.

### Transition Properties

#### Primary Transition
```css
transition: all 0.2s ease;
```
- **Duration:** 200ms (0.2s)
- **Timing Function:** ease (smooth acceleration/deceleration)
- **Properties:** all (applies to all animatable properties)
- **Usage:** Cards, buttons

### Specific Animations

#### Top Button Hover
```css
.top-button:hover {
  background-color: rgba(255, 255, 255, 0.9);
  /* Transitions to nearly opaque white */
  /* Duration: 0.2s */
}
```

#### Card Hover (Future Enhancement)
```css
.card {
  transition: all 0.2s ease;
  /* Can be extended with shadow, scale, or color changes */
}
```

### Animation Guidelines

1. **Timing:** Keep transitions under 300ms for snappy feel
2. **Easing:** Use `ease` or `ease-in-out` for natural motion
3. **Subtlety:** Avoid dramatic changes; subtle color/opacity shifts preferred
4. **Performance:** Limit to CSS properties (avoid JavaScript animations)

---

## Layout & Grid System

### Main Grid Container

The card grid uses CSS Grid with a 2-column layout and fixed-height Bento card system.

**Grid Configuration:**
```css
.grid-container {
  display: grid;
  grid-template-columns: repeat(2, 1fr);  /* 2 equal columns */
  gap: 20px;                              /* 20px gap between items */
  margin-bottom: 40px;
}
```

### Bento Size System

The design uses a **4-tier Bento size system** with fixed heights for consistent, predictable layouts:

#### Size 0.5: Link Bento
- **Grid:** 2 columns (100% width)
- **Height:** 96px (fixed, compact)
- **Layout:** Horizontal flex (icon on left, content on right, left-aligned)
- **Grid Span:** `span 2`
- **Gap:** 32px between icon and text
- **Cards:** Featured link banners, featured content, quick highlights
- **Use Case:** Top-of-page highlights, featured links, quick navigation

```css
.card-size-0-5 {
  grid-column: span 2;
  height: 96px;
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: flex-start;
  gap: 32px;
}

.card-size-0-5 .card-icon {
  margin-bottom: 0;
  flex-shrink: 0;
}
```

**Featured Link Card (X.com Example):**
```css
.featured-link-card {
  background: #ffffff;
}

.featured-link-icon {
  background-color: #000;
  color: white;
}
```

**Visual:**
```
┌────────────────────────────────────┐
│ [Icon] x.com/nattsaro               │
│ 48×48  (32px gap) (16px text)      │
└────────────────────────────────────┘
```

**Implementation Notes:**
- Icon: 48×48px with 12px border-radius
- Inner image: 24×24px, centered in icon, rotated for visual interest
- Text: 16px font size (inherits from .card-title), left-aligned, white background
- Image container uses `overflow: hidden` and `position: relative` for proper rendering

#### Size 1: Standard Single Card
- **Grid:** 1 column (50% width)
- **Height:** 240px (fixed)
- **Layout:** Vertical (flex-column)
- **Grid Span:** `span 1`
- **Cards:** LinkedIn, GitHub, Spotify, Twitter, Behance, Twitch, Figma, LeetCode

```css
.card-size-1 {
  grid-column: span 1;
  height: 240px;
}
```

**Visual:**
```
┌─────────┬─────────┐
│ Size 1  │ Size 1  │
│ 240px   │ 240px   │
└─────────┴─────────┘
```

#### Size 2: Double-Width Card (Content + Media)
- **Grid:** 2 columns (100% width)
- **Height:** 240px (fixed, same as Size 1)
- **Layout:** Horizontal (flex-row) with content on left, media on right
- **Grid Span:** `span 2`
- **Cards:** YouTube, Portfolio

```css
.card-size-2 {
  grid-column: span 2;
  height: 240px;
  flex-direction: row;
}
```

**Visual:**
```
┌────────────────────────┐
│ Content │ Thumbnail    │
│ 240px   │ 240px        │
└────────────────────────┘
```

#### Size 4: Featured Card (Double Height)
- **Grid:** 2 columns (100% width)
- **Height:** 480px (fixed, 2× Size 1)
- **Layout:** Flexible (typically vertical for featured content)
- **Grid Span:** `span 2`
- **Cards:** Map, Instagram
- **Use Case:** Featured content, hero sections, detailed displays

```css
.card-size-4 {
  grid-column: span 2;
  height: 480px;
  flex-direction: column;
}
```

**Visual:**
```
┌──────────────────────┐
│                      │
│     Size 4 Card      │
│     480px (2x)       │
│                      │
└──────────────────────┘
```

### Complete Layout Example

Typical arrangement with mixed Bento sizes:

```
├──────────────────┤
│  Link Bento      │  Row 1: Compact banner at top
├─────────┬─────────┤
│ Size 1  │ Size 1  │  Row 2: 2 standard cards
├─────────┼─────────┤
│ Size 1  │ Size 1  │  Row 3: 2 standard cards
├──────────────────┤
│      Size 2       │  Row 4: 1 double-width card
├──────────────────┤
│                  │  Row 5: 1 featured card (2x height)
│     Size 4       │
│                  │
├──────────────────┤
│      Size 2       │  Row 6: Another double-width card
├─────────┬─────────┤
│ Size 1  │ Size 1  │  Row 7: 2 standard cards again
└─────────┴─────────┘
```

### Grid Column Span Reference

```css
/* Size 1: Single-column cards */
grid-column: span 1;  /* Takes up 1 of 2 columns (50% width) */

/* Size 2 & 4: Full-width cards */
grid-column: span 2;  /* Takes up both columns (100% width) */
```

### Height System

| Size | Fixed Height | Ratio | Usage |
|------|------------|-------|-------|
| **Link Bento (0.5)** | 96px | 0.4x | Featured link banners, quick navigation |
| **Size 1** | 240px | 1x | Standard cards, default content |
| **Size 2** | 240px | 1x | Media cards (same height as Size 1) |
| **Size 4** | 480px | 2x | Featured/hero cards, detailed content |

**Note:** All heights are fixed (`height: 96px`/`height: 240px`/`height: 480px`), never using `min-height`, ensuring consistent alignment and layout predictability.

**Height Relationships:**
- Link Bento = 96px (compact with breathing room for icon)
- Size 1 = 240px (2.5× Link Bento)
- Size 2 = 240px (same as Size 1)
- Size 4 = 480px (2× Size 1)

---

## Responsive Design

### Breakpoints

| Breakpoint | Width | Device Type | Profile Container |
|-----------|-------|-------------|-------------------|
| **Desktop** | 640px+ | Large screens, tablets (landscape) | 580px fixed width |
| **Mobile** | Below 640px | Phones, tablets (portrait) | 100% full width |

### Mobile Adjustments

When viewport width ≤ 640px:

```css
@media (max-width: 640px) {
  .profile-container {
    width: 100%;              /* Full width */
    padding: 40px 16px;       /* Reduced padding (40px vertical, 16px horizontal) */
    border-radius: 0;         /* Remove rounded corners */
    box-shadow: none;         /* Remove shadow */
  }

  body {
    padding: 0;               /* Remove body padding */
    align-items: flex-start;  /* Top-align instead of center */
  }
}
```

### Design Adjustments by Screen Size

| Element | Desktop (640px+) | Mobile (<640px) |
|---------|-----------------|-----------------|
| **Container** | 580px centered | 100% full width |
| **Border Radius** | 24px rounded | 0px sharp edges |
| **Shadow** | Subtle 2-layer | None |
| **Padding** | 60px 20px | 40px 16px |
| **Grid Gaps** | 20px | 20px (preserved) |
| **Card Layout** | Maintained | Maintained |

---

## Common Patterns & Best Practices

### Pattern 1: Card with Icon + Title + Subtitle

Used by most single-width cards (LinkedIn, GitHub, Spotify, etc.)

```html
<a href="#" class="card linkedin-card">
  <div>
    <div class="card-icon linkedin-icon">in</div>
    <div class="card-title">Luis Alvarez</div>
    <div class="card-subtitle">linkedin.com</div>
  </div>
</a>
```

**Key Features:**
- Flex column layout with space-between
- Icon provides visual brand identification
- Subtle subtitle (grey color, smaller font)
- Links to external platform

### Pattern 2: Card with Media (Thumbnail)

Used by media cards (YouTube, Portfolio)

```html
<a href="#" class="card youtube-card">
  <div class="youtube-content">
    <div class="card-icon youtube-icon">▶</div>
    <div class="card-title">Video Title</div>
    <div class="card-subtitle">youtube.com</div>
  </div>
  <img src="..." alt="..." class="youtube-thumbnail">
</a>
```

**Key Features:**
- Flex row layout (horizontal)
- Content on left, media on right
- Fixed media width (180-200px)
- Full-width spanning

### Pattern 3: Card with Grid (Instagram)

Social media card with grid layout

```html
<a href="#" class="card instagram-card">
  <div class="instagram-content">
    <div class="card-icon instagram-icon">📷</div>
    <div class="card-title">@username</div>
    <div style="font-size: 13px; color: #999;">67 followers</div>
    <div class="instagram-grid">
      <div class="instagram-grid-item"></div>
      <div class="instagram-grid-item"></div>
      <div class="instagram-grid-item"></div>
    </div>
  </div>
</a>
```

**Key Features:**
- 3×1 grid of placeholder images
- Small 8px gaps between items
- Follower count as secondary info
- Gradient icon

### Pattern 4: Card with Action Button

Buttons for Call-to-Action

```html
<a href="#" class="card github-card">
  <div>
    <div class="card-icon github-icon">⚙</div>
    <div class="card-title">Luis Alvarez</div>
  </div>
  <button class="card-button">Follow</button>
</a>
```

**Key Features:**
- Button aligned to bottom (margin-top: auto)
- Platform-specific colors
- Pillow-shaped (border-radius: 20px)
- Light typography (font-weight: 100)

### Pattern 5: Full-Width Media Container (Map)

Location/map visualization

```html
<a href="#" class="card map-card">
  <div>
    <div class="map-container">
      <div class="map-pin"></div>
      <div class="map-label">Mexico City</div>
    </div>
    <div style="font-size: 14px; color: #999;">Mexico</div>
  </div>
</a>
```

**Key Features:**
- 220px height container
- Positioned map pin (absolute)
- Label in bottom-left corner
- Full-width spanning (grid-column: span 2)

---

## Example Component Code

### Complete Card Examples

#### Example 0: Link Bento (X.com)

```html
<a href="https://x.com/nattsaro" class="card featured-link-card card-size-0-5" target="_blank">
  <div class="card-icon featured-link-icon" style="overflow: hidden; position: relative; display: flex; align-items: center; justify-content: center;">
    <div style="width: 24px; height: 24px; position: relative; transform: rotate(327.393deg);">
      <img src="http://localhost:3845/assets/a99953e99e3955ac18f039912cf770c84520f8ce.png" alt="X Logo" style="width: 100%; height: 100%; object-fit: cover;">
    </div>
  </div>
  <div class="card-title" style="margin-bottom: 0; text-align: left;">x.com/nattsaro</div>
</a>
```

**CSS:**
```css
.featured-link-card {
  background: #ffffff;
}

.featured-link-icon {
  background-color: #000;
  color: white;
}

.card-size-0-5 {
  grid-column: span 2;
  height: 96px;
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: flex-start;
  gap: 32px;
}

.card-size-0-5 .card-icon {
  margin-bottom: 0;
  flex-shrink: 0;
}
```

**Key Features:**
- Featured link banner at top of profile
- Icon contains image asset (24×24px) centered in 48×48px icon
- Image rotated 327.393° for visual interest
- Text left-aligned with 32px spacing from icon
- Full-width spanning (2 grid columns)
- Compact height (96px) for quick navigation links

---

#### Example 1: Simple Icon Card (LinkedIn)

```html
<a href="https://linkedin.com/in/example" class="card linkedin-card" target="_blank">
  <div>
    <div class="card-icon linkedin-icon">in</div>
    <div class="card-title">Full Name</div>
    <div class="card-subtitle">linkedin.com</div>
  </div>
</a>
```

**CSS:**
```css
.linkedin-card {
  background: linear-gradient(135deg, #f0f6f9 0%, #ffffff 100%);
}

.linkedin-icon {
  background-color: #007EBB;
  color: white;
}
```

---

#### Example 2: Card with Button (Twitter)

```html
<a href="https://twitter.com/example" class="card twitter-card" target="_blank">
  <div>
    <div class="card-icon twitter-icon">𝕏</div>
    <div class="card-title">Twitter</div>
    <div class="card-subtitle">@example</div>
  </div>
  <button class="card-button">Follow</button>
</a>
```

**CSS:**
```css
.twitter-card {
  background: linear-gradient(135deg, #f5fafe 0%, #ffffff 100%);
}

.twitter-icon {
  background-color: #55ACEE;
  color: white;
}

.twitter-card .card-button {
  background-color: #55ACEE;
  color: white;
  margin-top: auto;
}
```

---

#### Example 3: Media Card (YouTube)

```html
<a href="https://youtube.com/watch?v=..." class="card youtube-card" target="_blank">
  <div class="youtube-content">
    <div class="card-icon youtube-icon">▶</div>
    <div class="card-title">Video Title Here</div>
    <div class="card-subtitle">youtube.com</div>
  </div>
  <img src="thumbnail.jpg" alt="Video" class="youtube-thumbnail">
</a>
```

**CSS:**
```css
.youtube-card {
  background: linear-gradient(135deg, #fff0f0 0%, #ffffff 100%);
  grid-column: span 2;
  display: flex;
  gap: 20px;
}

.youtube-card .card-icon {
  background-color: #FF0000;
  color: white;
}

.youtube-thumbnail {
  width: 180px;
  height: 100px;
  border-radius: 12px;
  object-fit: cover;
}
```

---

#### Example 4: Grid Card (Instagram)

```html
<a href="https://instagram.com/example" class="card instagram-card" target="_blank">
  <div class="instagram-content">
    <div class="card-icon instagram-icon">📷</div>
    <div class="card-title">@example</div>
    <div style="font-size: 13px; color: #999; margin-bottom: 8px;">1.2K followers</div>
    <div class="instagram-grid">
      <div class="instagram-grid-item"></div>
      <div class="instagram-grid-item"></div>
      <div class="instagram-grid-item"></div>
    </div>
  </div>
</a>
```

**CSS:**
```css
.instagram-card {
  grid-column: span 2;
  display: flex;
  gap: 20px;
}

.instagram-icon {
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  color: white;
}

.instagram-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 8px;
  margin-top: 12px;
}

.instagram-grid-item {
  aspect-ratio: 1;
  background-color: #f0f0f0;
  border-radius: 8px;
}
```

---

#### Example 5: Full-Width Media (Map)

```html
<a href="https://maps.google.com/..." class="card map-card" target="_blank">
  <div>
    <div class="map-container">
      <div class="map-pin" style="top: 50%; left: 50%; transform: translate(-50%, -50%);"></div>
      <div class="map-label">Location Name</div>
    </div>
    <div style="font-size: 14px; color: #999;">Country</div>
  </div>
</a>
```

**CSS:**
```css
.map-card {
  grid-column: span 2;
  background: linear-gradient(135deg, #f9f9f9 0%, #ffffff 100%);
}

.map-container {
  position: relative;
  width: 100%;
  height: 220px;
  border-radius: 12px;
  background: linear-gradient(135deg, #e8e8e8 0%, #f5f5f5 100%);
  margin-bottom: 16px;
  overflow: hidden;
}

.map-pin {
  position: absolute;
  width: 32px;
  height: 32px;
  background-color: #5B9EFF;
  border-radius: 50%;
  border: 3px solid white;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.15);
}

.map-label {
  position: absolute;
  bottom: 12px;
  left: 12px;
  font-size: 14px;
  color: #666;
}
```

---

### Top Buttons Implementation

```html
<div class="top-buttons">
  <button class="top-button" onclick="openModal()" title="Share">
    <svg><!-- Icon SVG --></svg>
  </button>
  <button class="top-button" title="Share Profile">
    <svg><!-- Icon SVG --></svg>
  </button>
</div>
```

**CSS:**
```css
.top-buttons {
  position: absolute;
  top: 20px;
  left: 20px;
  right: 20px;
  display: flex;
  justify-content: space-between;
  z-index: 100;
}

.top-button {
  width: 48px;
  height: 48px;
  border-radius: 50%;
  border: none;
  background-color: rgba(187, 187, 187, 0.2);
  cursor: pointer;
  display: flex;
  align-items: center;
  justify-content: center;
  backdrop-filter: blur(10px);
  transition: all 0.2s ease;
}

.top-button:hover {
  background-color: rgba(255, 255, 255, 0.9);
}

.top-button svg {
  width: 20px;
  height: 20px;
}
```

---

### Modal Implementation

```html
<div id="shareModal" class="modal">
  <div class="modal-content">
    <button class="modal-close" onclick="closeModal()">&times;</button>
    <h2 style="margin-bottom: 20px;">Share Your Profile</h2>
    <p style="color: #666; margin-bottom: 30px;">Share this profile with your network.</p>
  </div>
</div>
```

**CSS:**
```css
.modal {
  display: none;
  position: fixed;
  z-index: 200;
  left: 0;
  top: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.5);
}

.modal.active {
  display: flex;
  align-items: center;
  justify-content: center;
}

.modal-content {
  background-color: white;
  padding: 40px;
  border-radius: 24px;
  width: 90%;
  max-width: 500px;
  text-align: center;
  position: relative;
}

.modal-close {
  position: absolute;
  top: 20px;
  right: 20px;
  font-size: 28px;
  background: none;
  border: none;
  cursor: pointer;
  color: #666;
}
```

**JavaScript:**
```javascript
function openModal() {
  document.getElementById('shareModal').classList.add('active');
}

function closeModal() {
  document.getElementById('shareModal').classList.remove('active');
}
```

---

## Design System Rules & Guidelines

### Do's ✅

1. **Use 4px spacing increments** for consistency
2. **Keep font weights light** (100-200) for refined look
3. **Apply subtle shadows** for depth without heaviness
4. **Use branded platform colors** for platform-specific elements
5. **Maintain 24px border radius** on primary containers
6. **Keep transitions under 300ms** for snappy interactions
7. **Use gradient backgrounds** on cards for visual interest
8. **Maintain 580px width** on desktop for focused presentation
9. **Test responsive design** at 640px breakpoint
10. **Use negative letter-spacing** for condensed typography

### Don'ts ❌

1. **Don't use heavy font weights** (500+) unless specifically needed
2. **Don't add loud animations** or dramatic transitions
3. **Don't change the primary shadow system** without reason
4. **Don't use additional font families** (stick to Geist Mono)
5. **Don't create shadow depth above primary shadow** system
6. **Don't break the 4px spacing grid** without justification
7. **Don't remove rounded corners** on desktop view
8. **Don't add hover animations** to cards without transitions
9. **Don't use opacity beyond 90%** without purpose
10. **Don't ignore mobile responsive design** considerations

---

## Future Enhancements

Potential improvements to the design system:

1. **Dark Mode Support** - CSS variables for theme switching
2. **Animation Library** - More sophisticated hover states
3. **Component Library** - Reusable React/Vue components
4. **Extended Color Palette** - Additional accent colors
5. **Accessibility Standards** - WCAG AA compliance
6. **Icon System** - Custom icon set instead of Unicode
7. **Micro-Interactions** - Loading states, skeleton screens
8. **Form Components** - Input styling guide
9. **Utility Classes** - CSS helper classes
10. **Design Tokens** - Figma/Sketch integration

---

## Resources

### Font Resources
- **Geist Mono Font:** https://fonts.googleapis.com/css2?family=Geist+Mono:wght@400;500;600;700

### Design References
- **Linktree Design System** - Inspiration source
- **Bento.me** - Card-based UI patterns
- **Tailwind CSS** - 4px spacing system reference

### Tools & Technologies
- **Vanilla HTML/CSS** - No framework dependencies
- **CSS Grid** - Layout system
- **CSS Flexbox** - Component layout
- **CSS Transitions** - Animation system

---

**Last Updated:** 2025-11-26
**Version:** 1.0
**Maintained By:** Natt Saro Design System Team
