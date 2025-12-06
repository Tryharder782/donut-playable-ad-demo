# 🍩 The Juicy Donut | High-Performance WebGL Playable Ad

![Project Banner](public/preview.gif)
<!-- ЗАМЕНИ public/preview.gif НА ПУТЬ К ТВОЕЙ ГИФКЕ, ЕСЛИ ОНА В ДРУГОМ МЕСТЕ -->

[![Live Demo](https://img.shields.io/badge/Live_Demo-Vercel-000?style=for-the-badge&logo=vercel&logoColor=white)]([https://donut-playable-ad-demo.vercel.app](https://donut-playable-ad-demo.vercel.app/))
<!-- ЗАМЕНИ ССЫЛКУ ВЫШЕ НА ТВОЮ ФИНАЛЬНУЮ ССЫЛКУ -->

## 🚀 Overview

A production-ready prototype of a **Hyper-Casual Playable Ad** built with **React Three Fiber** and **Three.js**.

Unlike standard Unity WebGL exports (which often suffer from bloat and slow loading times), this project demonstrates a **code-first approach** to create a lightweight, high-performance interactive experience suitable for networks like **AppLovin, Mintegral, IronSource, and Unity Ads**.

## 💎 Key Technical Achievements

*   **📦 Single-File Distribution:** The entire project (Code + 3D Models + Styles) is bundled into a **single `index.html` file**. No external asset folders.
*   **⚡ Ultra-Lightweight:** Total build size is **~1.2 MB** (Base64 encoded assets included). Loads instantly even on 3G networks.
*   **📱 Mobile-First Performance:** Optimized for low-end devices. Stable 60 FPS.
*   **🎨 "Juicy" Game Feel:** Implemented **Squash & Stretch** physics and particle systems to maximize user engagement (CTR).
*   **📢 Ad Network Ready:** Ready for `mraid.open()` and standard CTA (Call to Action) integration.

## 🛠 Tech Stack

*   **Core:** React, TypeScript
*   **3D Engine:** Three.js, React Three Fiber (R3F)
*   **Animation:** GSAP / Custom Physics Math
*   **Bundling:** Vite + `vite-plugin-singlefile`
*   **Asset Pipeline:** GLTF to Base64 optimization

## 🏗 Architecture & Optimization

### The "Single File" Challenge
Ad networks often require a single HTML file delivery. Standard bundlers split assets.
**Solution:**
1.  3D Model (`donut.glb`) is converted to a **Base64 string** and embedded directly into the code.
2.  `vite-plugin-singlefile` inlines all JavaScript and CSS chunks into the HTML entry point.
3.  Result: A drag-and-drop file ready for the marketing dashboard.

### Visual Polish ("The Juice")
To achieve the "Hyper-Casual" aesthetic without heavy physics engines:
*   **Procedural Animations:** Squash and stretch are calculated mathematically on click events, avoiding heavy animation clips.
*   **Materials:** High-specularity physical materials to achieve the "candy/plastic" look.

## 💻 Local Development

1.  **Clone the repo:**
    ```bash
    git clone https://github.com/Tryharder782/donut-playable-ad-demo.git
    ```
2.  **Install dependencies:**
    ```bash
    npm install
    ```
3.  **Run dev server:**
    ```bash
    npm run dev
    ```

## 📦 Building for Production

To generate the single-file build:

```bash
npm run build
