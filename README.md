````markdown
# Coding Clubhouse – Landing Page

A responsive, single-page landing site for the fictional **Coding Clubhouse** initiative.  
Built with semantic HTML and Tailwind CSS (via CDN), this page showcases the program’s mission, featured programs, impact, and a newsletter sign-up.

---

## Overview

The page includes:

- **Sticky header** with logo, navigation, and “Donate” call-to-action.
- **Hero section** with gradient background, hero illustration, and primary buttons.
- **Who We Are** section with gradient left border, value cards, and a mission code card.
- **What We Do** section with a gradient background and three “featured program” cards.
- **In Action** gallery with a 2×2 window-style photo grid and decorative code text.
- **Footer** with navigation, social icons, newsletter form, and copyright.

The layout is responsive for mobile, tablet, and desktop.

---

## Tech Stack

- **HTML5**
- **Tailwind CSS** (CDN)
- **Google Fonts** – Poppins (primary typeface)
- **Local assets** – PNG / JPG / SVG images under `assets/img`

No build tools or JavaScript frameworks are required.

---

## Getting Started

### 1. Prerequisites

You only need a web browser. For easier development, a local HTTP server is recommended (for example, VS Code Live Server).

### 2. Project structure

```text
project-root/
├─ index.html
└─ assets/
   └─ img/
      ├─ TheCoding.png
      ├─ ClubHouse.png
      ├─ hero-background.jpg
      ├─ hero-image.png
      ├─ inclusive-heart.svg / .png
      ├─ community.png
      ├─ impact-disc.png
      ├─ accessible.png
      ├─ dream-frame.png
      ├─ teacher-frame.png
      ├─ feature-3-frame.png
      ├─ in-action-1.png
      ├─ in-action-2.png
      ├─ in-action-3.png
      ├─ in-action-4.png
      ├─ red-dot.png
      ├─ yellow-dot.png
      ├─ green-dot.png
      ├─ violet-dot.png
      ├─ gray-dot.png
      ├─ purple-dot.png
      ├─ RocketLaunch.svg
      ├─ Heart.svg
      └─ (other decorative icons)
````

### 3. Run locally

1. Clone or download the project.
2. Ensure the folder structure above is preserved.
3. Open `index.html` directly in your browser
   **or** start a local server (for example, with VS Code Live Server) and open:

   ```text
   http://localhost:5500/index.html
   ```

The page should render with all sections, gradients, and images.

---

## Key Files and Sections

### `index.html`

Main document containing all sections:

1. **Header (`<header>`)**

   * Sticky navigation bar using `fixed top-0 w-full z-20`.
   * Logo images (`TheCoding.png` and `ClubHouse.png`).
   * Nav links: About Us, Programs, Resources, Get Involved.
   * “Donate” button styled as a pill.

2. **Hero section**

   * Uses inline `style` for the background:

     ```html
     background:
       linear-gradient(#8C52FF, rgba(120, 55, 250, 0.9)),
       url('assets/img/hero-background.jpg') center/cover no-repeat;
     ```

   * Height set with `min-h-[80vh]` (or similar) so hero + pills fit within one screen.

   * Left column: “Foundations First. Futures Forever.” heading, supporting copy, and two CTA buttons.

   * Right column: hero illustration (`hero-image.png`) in a circular card.

3. **“Who We Are” section**

   * Decorative violet dot absolutely positioned with `absolute top-[120px] left-[150px]`.
   * Centered heading row with three small icons.
   * Two-column grid:

     * Left: text box with gradient left border (using `bg-gradient-to-b from-[#184EB4] to-[#8C52FF]`) and four value cards (Inclusive, Community Focused, Impact Driven, Accessible).
     * Right: code-style mission card (`our-mission.js`) plus four statistic tiles (Potential, Inclusive, Barriers, Mission).
   * Bottom quote line:

     > "Coding is not about technology, it's about changing the world"

4. **“What We Do / Featured Programs” section**

   * Background gradient set using Tailwind arbitrary value:

     ```html
     class="bg-[linear-gradient(180deg,_#EAF0FA_0%,_#FFFFFF_52.4%,_#F4E8FF_100%)]"
     ```

   * Heading: “What We Do” (purple) + supporting paragraph + “Featured Programs” label.

   * Three program cards using a responsive grid:

     * Dream Beyond Limits
     * Teacher Training & Youth Empowerment
     * Virtual Summer Classes

   * Each card:

     * Colored frame icon image (`*-frame.png`).
     * Three status dots.
     * Program description.
     * Dark `code.js` block with example JavaScript snippet.

   * “Explore Our Programs” button and small bottom line:

     > Building the future, one line at a time.

5. **“In Action” section**

   * Background color: `#EAF0FA`.

   * Decorative background code text using absolutely positioned `<p>`:

     ```html
     return 'happy';
     return 'fun';
     ```

   * Two-column layout:

     * Left: section title “In Action” plus short description.
     * Right: 2×2 grid of image cards (`in-action-1.png` … `in-action-4.png`).
       Each card has:

       * Blue top bar (`bg-[#1E6CFB]`) with “camera” icon and three dots.
       * Full-width photo (`object-cover`) with rounded corners.

   * Bottom tagline:

     > Building the future, one line at a time…

6. **Footer**

   * Top row:

     * Logo re-used.
     * Footer nav links: About Us, Programs, Volunteer, Donate.
     * Social icons (Instagram, Facebook, X/Twitter, YouTube) implemented as inline SVGs.
   * Middle row:

     * “Get in Touch” label.
     * One-line description.
     * Newsletter form with email input and “Subscribe Now” button.
   * Bottom row:

     * Copyright line:

       ```text
       © 2025 Coding Clubhouse. All rights reserved.
       ```

---

## Customization

### Update text

Edit text directly inside `index.html`. Examples:

* Hero headline and subtitle.
* Program descriptions in “Featured Programs”.
* Copy in “Who We Are”, “In Action”, and footer.

### Change colors

Most colors are defined with Tailwind utility classes:

* Background gradients and brand colors use hex arbitrary values, for example:

  ```html
  bg-[#8C52FF]
  text-[#AD31D9]
  bg-[linear-gradient(180deg,_#EAF0FA_0%,_#FFFFFF_52.4%,_#F4E8FF_100%)]
  ```

Replace the hex values as needed.

### Replace images

Place new images in `assets/img` and update `src` attributes:

```html
<img src="assets/img/hero-image.png" alt="New hero image" />
```

Keep similar aspect ratios for best layout results.

---

## Responsive Behavior

* Uses Tailwind `sm:`, `md:`, and `lg:` breakpoints.
* On small screens:

  * Header navigation stacks vertically.
  * Grids (hero, “What We Do”, “In Action”) collapse to a single column.
* On larger screens:

  * Two-column hero and “Who We Are” layout.
  * Three-column “Featured Programs” and 2×2 photo grid.

You can tweak breakpoints by adjusting classes like `lg:grid-cols-2`, `md:grid-cols-2`, and `lg:grid-cols-3`.

---

## Future Improvements (Optional)

* Add real navigation links and smooth scrolling to sections.
* Extract inline gradient styles into a Tailwind config (if you move from CDN to a build setup).
* Add simple JavaScript for animations (scroll reveal, button hover effects, etc.).
* Hook the newsletter form to a real email service.


```
