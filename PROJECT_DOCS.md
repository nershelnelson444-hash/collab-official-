# PROJECT_DOCS.md

## Project Overview
**co//ab.** is a high-end digital agency website built with a strict minimalist monochrome design system. It avoids trends associated with depth—such as shadows or blurs—in favor of a flat, high-contrast environment. The UI evokes a sense of "digital luxury" through extreme restraint.

## Tech Stack
- **Framework:** Next.js (App Router)
- **Styling:** Tailwind CSS (strict monochrome config)
- **Animations:** Framer Motion (custom cursor, page transitions, micro-interactions)
- **Icons:** Lucide React

---

## Design System & Rules

### 🎨 Color Palette
The color scheme is strictly monochrome.

| Token | Hex | Usage |
|-------|-----|-------|
| **Background (Primary)** | `#000000` | Primary background (pure black). Used globally. |
| **Background (Alt)** | `#050505` | Alternate background. |
| **Surface** | `#141313` | Base surface / low container. |
| **Primary Text** | `#FFFFFF` | Crisp white for primary headers and active states. |
| **Secondary Text** | `#A3A3A3` | Soft light grey for paragraphs and descriptions. |
| **Border (Subtle)** | `#1A1A1A` | Hair-thin dividers. |
| **Border (Card/Input)** | `#222222` / `#333333` | Card and input borders. |

*Rule:* No geometric gradients, lighter backgrounds, or vibrant accent colors.

### 🔤 Typography
- **Headlines & Body:** Inter
- **Labels (Caps/Tech Stack):** Geist
- *Rule:* Crisp white for headers, muted grey for body.

### 📐 Layout & Spacing
- **Padding:** Generous padding (`min 8rem` between major sections).
- **Navbar:** A fixed component across all pages so it never jumps during routing.

### ✨ Animations & Micro-Interactions
- **Custom Cursor:** A white dot cursor that expands on clickable elements (using Framer Motion).
- **Hover States:** Full color inversion for buttons (background becomes `#FFFFFF` and text becomes `#000000` instantly). Images inside cards scale `1.02x`.
- **Scroll:** Smooth scroll experience.

---

## File Structure & Architecture

The project utilizes the Next.js App Router architecture.

```
/app
  ├── layout.tsx         # Global layout (includes Navbar, CustomCursor, Fonts)
  ├── globals.css        # Global styles (Tailwind + monochrome baseline)
  ├── page.tsx           # Homepage (Hero & Selected Works)
  ├── work/page.tsx      # Selected Works / Case Studies
  ├── services/page.tsx  # Services overview
  ├── marketplace/page.tsx # Digital assets & packages
  └── contact/page.tsx   # Client enquiry form

/components
  ├── layout
  │   ├── Navbar.tsx     # Fixed top navigation
  │   └── Footer.tsx     # Site footer
  ├── ui
  │   ├── CustomCursor.tsx # Framer motion custom cursor
  │   └── Button.tsx     # Reusable button with hover inversion
  └── ...                # Other specific components

/lib
  └── utils.ts           # Utility functions (cn for tailwind-merge)
```

---

## How to Run & Deploy

### Development
1. Install dependencies: `npm install`
2. Run development server: `npm run dev`
3. Open `http://localhost:3000`

### Build & Deploy
1. Build for production: `npm run build`
2. Start production server: `npm run start`

Deploy via Vercel for the most optimized Next.js App Router performance.
