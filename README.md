# Easely.js

**Easely.js** is a lightweight, declarative GSAP wrapper designed for creative frontend developers. Transform static HTML into a high-end, "Awwwards-level" experience using simple data attributes. No complex JavaScript required.

---

## ✨ Core Features

* **Declarative Syntax:** Control animations directly in your HTML.
* **Scroll-Triggered:** High-performance scroll detection powered by GSAP.
* **Liquid Parallax:** Smooth "scrub" effects that tie motion to the scrollbar.
* **Zero Layout Thrash:** Built-in GPU optimization and memory hygiene.
* **Fresher Friendly:** Designed to be used without writing a single line of GSAP logic.

---

## 🛠️ Quick Start

### 1. Installation

**Using CDN (Easiest Way):**
Add these to your HTML just before the closing `</body>` tag:

```html
<script src="https://cdnjs.cloudflare.com/ajax/libs/gsap/3.12.5/gsap.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/gsap/3.12.5/ScrollTrigger.min.js"></script>

<script src="https://cdn.jsdelivr.net/npm/@pstarz7/easely@1.0.4/dist/easely.umd.js"></script>
```

**Using NPM:**

```bash
npm install @pstarz7/easely
```

### 2. Initialization

Initialize the engine in your main script file:

```javascript
window.addEventListener('load', () => {
    Easely.init({
        duration: 1.5,
        ease: "power4.out"
    });
});
```

### 3. Usage

Simply add the `data-ez` attribute to any element:

```html
<h1 data-ez="blur-up">Hello World</h1>

<section data-ez="slide-up" data-ez-scroll="true">
    I animate when you see me.
</section>
```

---

## 📖 Attributes Reference

| Attribute | Value | Description |
| :--- | :--- | :--- |
| `data-ez` | `fade`, `blur-up`, `slide-up`, `slide-down`, `zoom-in` | Sets the animation preset type. |
| `data-ez-duration` | `number` (e.g., `2`) | Speed of the animation in seconds. |
| `data-ez-delay` | `number` (e.g., `0.5`) | Delay before the animation starts. |
| `data-ez-scroll` | `true` / `false` | Enables scroll-triggered animation. |
| `data-ez-start` | `string` (e.g., `top 80%`) | Sets the scroll trigger position. |
| `data-ez-scrub` | `true` / `number` | Locks animation to scrollbar (Parallax). |
| `data-ez-stagger` | `number` (e.g., `0.2`) | Delays between children animations. |
| `data-ez-once` | `true` / `false` | If false, animation repeats on scroll back. |

---

## 📂 Project Structure

The library logic is organized into clean, modular files:

```plaintext
src/
├── core/
│   ├── config.js    # Default settings & prefixes
│   ├── engine.js    # DOM Scanner & Scanner Logic
│   └── registry.js  # Memory management & Tween tracking
└── modules/
    ├── animator.js  # GSAP Tween execution
    ├── parser.js    # HTML Attribute Reader
    └── scroll.js    # ScrollTrigger orchestration
```

---

## 🎨 Best Practices

- **The Safety Layer:** To avoid "flashing" before the JS loads, add this to your CSS:
    ```css
    [data-ez] { opacity: 0; visibility: hidden; }
    .ez-ready [data-ez] { visibility: visible; }
    ```
- **Performance:** For complex pages, use `data-ez-scroll="true"` to ensure elements only animate when they are in view.
- **Refined Motion:** Use `data-ez-duration="2"` for headings to give them a premium, cinematic feel.

---

## 📜 License

MIT © **Papu Badatya**

---

## 🚀 To-Do List

- [x] Production Engine v1.0.4
- [x] NPM Package Release
- [ ] Add Custom Timeline Support
- [ ] Built-in Markers for Debugging (Coming Soon)

**Happy Building! ✨**
```
