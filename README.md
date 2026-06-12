# 🪨 Lithos — Layers Hold Tales of Time

[![React](https://img.shields.io/badge/React-19.0-blue?style=flat-square&logo=react)](https://react.dev/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.x-blue?style=flat-square&logo=typescript)](https://www.typescriptlang.org/)
[![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-3.4-38bdf8?style=flat-square&logo=tailwind-css)](https://tailwindcss.com/)
[![Vite](https://img.shields.io/badge/Vite-8.0-646cff?style=flat-square&logo=vite)](https://vite.dev/)

**Lithos** is an immersive, highly interactive web application designed to showcase Earth's geological layers through deep-time exploration. Combining smooth web animation, custom HTML5 Canvas mask processing, and a high-end editorial design system, Lithos offers a unique window into the history written beneath our feet.

Developed with a premium, sleek aesthetic featuring **Inter** and **Playfair Display** typography, glassmorphism navigation, and responsive layouts.

---

## ✨ Features

*   **Interactive Spotlight Reveal**: Move your mouse across the hero section to see a real-time radial spotlight mask that transitions between different states of Earth's layers.
*   **Immersive Micro-Animations**: Smooth intro zooms, fading layout blocks, and text reveals powered by fine-tuned CSS cubic-bezier transitions.
*   **Custom Mask Engine**: Built with a React-wrapped `<canvas>` renderer that dynamically generates and handles custom transparency masks based on pointer coordinates.
*   **Premium Editorial Design**: Optimized typographic hierarchy, carefully curated color palettes, and glassmorphic elements.
*   **Fully Responsive**: Styled with fluid layouts to look exceptional on mobile devices, tablets, and ultra-wide screens.

---

## 🛠️ Tech Stack & Architecture

- **Framework**: [React 19](https://react.dev/)
- **Language**: [TypeScript](https://www.typescriptlang.org/) (Strictly typed)
- **Styling**: [Tailwind CSS](https://tailwindcss.com/) + Custom CSS animations
- **Build Tool**: [Vite](https://vite.dev/)
- **Icons**: [Lucide React](https://lucide.dev/)

---

## 🚀 Getting Started

Follow these instructions to run the project locally on your machine.

### Prerequisites

Make sure you have [Node.js](https://nodejs.org/) installed (v18+ recommended).

### Installation

1.  **Clone the Repository**
    ```bash
    git clone https://github.com/YOUR_USERNAME/Lithos.git
    cd Lithos
    ```

2.  **Install Dependencies**
    ```bash
    npm install
    ```

3.  **Run Development Server**
    ```bash
    npm run dev
    ```
    Once the server is running, open [http://localhost:5173](http://localhost:5173) in your browser.

4.  **Build for Production**
    ```bash
    npm run build
    ```
    The production-ready assets will be built in the `dist/` folder.

---

## 📂 Project Structure

```text
├── public/                # Static assets
│   ├── favicon.svg        # Site favicon
│   └── icons.svg          # SVG icons
├── src/
│   ├── assets/            # Component-specific assets
│   ├── App.tsx            # Main application layout and state logic
│   ├── RevealLayer.tsx    # Canvas spotlight mask overlay logic
│   ├── index.css          # Base styles and keyframe animations
│   ├── main.tsx           # React entry point
│   └── vite-env.d.ts      # TypeScript declarations
├── index.html             # Application entry point
├── package.json           # Scripts and dependencies
├── tailwind.config.js     # Tailwind setup
├── tsconfig.json          # TypeScript configurations
└── vite.config.ts         # Vite build configuration
```

---

## 🧠 How It Works: The Reveal Effect

The highlight of the project is the dynamic spotlight overlay:
1. **Mouse Tracking**: `App.tsx` captures pointer coordinates (`mousemove`) and applies a **smooth easing interpolation** using `requestAnimationFrame`.
2. **Dynamic Masking**: Coordinates are passed down to `<RevealLayer />`, which draws a radial gradient on a hidden `<canvas>`.
3. **GPU-Accelerated Mask**: The canvas is converted to a base64 DataURL and assigned to the CSS `-webkit-mask-image` property of the top layer, revealing the under-layer with beautiful anti-aliased feathering.

---

## 👤 Credits & Author

Developed by **Dipangshu**.
