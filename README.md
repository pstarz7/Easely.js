
# 🚀 Welcome to Easely.js (Beta)
**Easely.js** is a simple tool designed to help you add professional animations to your website without writing complex JavaScript. If you can write HTML, you can animate like a pro.

> **Note:** This library is currently in active development. It is perfect for personal portfolios and freelance projects. We are working hard to make it 100% production-ready!

---

## 🛠️ Step 1: Add it to your site
Copy and paste these lines into your HTML file just before the closing `</body>` tag.

```html
<script src="https://cdnjs.cloudflare.com/ajax/libs/gsap/3.12.5/gsap.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/gsap/3.12.5/ScrollTrigger.min.js"></script>

<script src="https://cdn.jsdelivr.net/npm/@pstarz7/easely@1.0.4/dist/easely.umd.js"></script>

<script>
  // Initialize the engine
  Easely.init();
</script>
```

---

## 🎨 Step 2: Pick your "Movement"
Just add the `data-ez` attribute to any tag (like `<h1>`, `<div>`, or `<img>`).

| Attribute | What it does |
| :--- | :--- |
| `data-ez="fade"` | Smoothly fades in from 0% to 100% opacity. |
| `data-ez="blur-up"` | Starts blurry and clear up (Premium aesthetic). |
| `data-ez="slide-up"` | Slides up from the bottom into position. |
| `data-ez="slide-down"` | Slides down from the top into position. |
| `data-ez="zoom-in"` | Scales up from a small size to normal. |

---

## ⚙️ Step 3: All Attributes (The Control Panel)
Want to fine-tune your motion? Add these extra attributes to your HTML tags.

| Attribute | Value | Description |
| :--- | :--- | :--- |
| `data-ez-duration` | `number` | How many seconds the animation takes (e.g., `2`). |
| `data-ez-delay` | `number` | How many seconds to wait before starting (e.g., `0.5`). |
| `data-ez-scroll` | `true` | Element only animates when you scroll down to it. |
| `data-ez-start` | `string` | Where on the screen to trigger (e.g., `top 80%`). |
| `data-ez-scrub` | `number` | Links animation to your scroll speed (Smooth parallax). |
| `data-ez-stagger` | `number` | Animates children one-by-one (e.g., `0.2`). |
| `data-ez-once` | `false` | Set to `false` if you want it to repeat every time you scroll. |

---

## 🩺 Troubleshooting & Bug Fixes
If things don't look right, try these simple solutions:

**1. The "Flashing" Problem**
* **Issue:** Elements appear for a split second before the animation starts.
* **Fix:** Add this CSS to your stylesheet:
    ```css
    [data-ez] { opacity: 0; }
    ```

**2. Animation Starts Too Early**
* **Issue:** The element animates before you can see it.
* **Fix:** Use `data-ez-start="top 60%"` to move the trigger point higher on the screen.

**3. Blank Screen on Load**
* **Issue:** Nothing appears.
* **Fix:** Check your console (F12). Make sure you included the GSAP scripts *before* the Easely script.

---

## 📩 Report a Bug / Give Feedback
Since this library is in the **development phase**, your feedback is very important! 

If you find a bug, have an idea for a new animation, or want to use this in a big production project, please reach out:

* **Email:** [Papubadatya355@gmail.com]
* **Portfolio:** [https://pstarz.vercel.app/]

**Thank you for using Easely.js. Let's make the web move together! ✨**

---
**What's next?** I am currently working on adding more advanced features like **Custom Timelines** and **Path Animations** to make it even easier for beginners to build world-class websites.
