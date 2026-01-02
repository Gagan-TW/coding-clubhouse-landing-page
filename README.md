# 🚀 Coding Clubhouse Landing Page

A high-fidelity, responsive landing page for the fictional **Coding Clubhouse** initiative. This project bridges the gap between modern UI design and technical education, utilizing a "code-as-art" aesthetic to engage young learners and donors alike.

---

## 🎨 Design Preview


### 🖥️ View the Full Project
The design focuses on high-impact visuals, custom gradients, and pixel-perfect layout implementation.

![Coding Clubhouse Desktop Preview](assets\img\landing-page.png)

---

## ✨ Key Technical Features

### 1. Advanced Tailwind Layouts
Instead of standard templates, I used **Tailwind CSS arbitrary values** and custom utility classes to achieve the unique brand look:
* **Custom Gradients:** Implemented complex 180-degree linear gradients for section transitions.
* **Responsive Fluidity:** Used a mobile-first approach where navigation and grid systems (hero, programs, and gallery) adapt seamlessly from mobile to 4K displays.

### 2. "OS-Style" UI Components
To reflect the "Coding" theme, several UI elements are designed to look like integrated development environments (IDEs):
* **Syntax Highlighted Cards:** Program descriptions are paired with dark-mode code blocks (`bg-[#161B22]`) featuring custom-colored JavaScript snippets.
* **Traffic Light UI:** Used decorative red, yellow, and green "window dots" to give components a desktop application feel.

### 3. Interactive UX Elements
* **Sticky Navigation:** A glassmorphism-inspired header that stays fixed during scroll for constant access to the "Donate" CTA.
* **Absolute Asset Positioning:** Strategic use of decorative background assets (dots and code snippets like `return 'happy'`) that float behind the content to add depth without clutter.

---

## 🛠️ Tech Stack & Resources

* **Language:** HTML5 (Semantic)
* **Styling:** Tailwind CSS (via Play CDN for rapid prototyping)
* **Typography:** [Poppins](https://fonts.google.com/specimen/Poppins) (Primary)
* **Assets:** Custom SVG icons and transparent PNG layers.

---

## 📂 Project Architecture

```text
project-root/
├─ index.html           # Main structure & Tailwind implementation
├─ assets/
  └─ img/
  