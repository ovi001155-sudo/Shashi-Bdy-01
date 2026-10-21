# 💖 Interactive Love Letter & Certificate of Devotion

An elegant, mobile-optimized, single-page interactive web experience designed as a romantic gift. It guides the user through a sweet storytelling sequence, lists reasons for affection, and culminates in a customizable "Kadoin" (gift box) opening that reveals a personalized Certificate of Love.

---

## ✨ Features

- **📖 Storytelling Slides**: Sequential sticker slides with custom animated text typing effects (`TypeIt.js`) and romantic floating heart particles.
- **🎵 Romantic Background Music**: Integrates user interaction to autoplay background music seamlessly upon entry, bypassing browser autoplay policies.
- **💝 50 Reasons Why I Love You**: An elegant, scrollable glassmorphic list that displays reasons one by one with a staggered fade-in animation.
- **🔄 Smart Auto-Scroll & Floating Controls**:
  - Automatically crawls through the reasons list smoothly for hands-free reading.
  - Floats a custom glassmorphic control bar to play, pause, or manually scroll up/down.
  - Touch-interaction automatically pauses the auto-scroll sequence.
- **🎁 Animated Kadoin Interaction**: A floating, glowing gift box that shakes when tapped and explodes into a shower of romantic particles.
- **📜 Certificate of Love**:
  - A formal, gold-bordered certificate personalized with the recipient and sender names.
  - Interactive "I Love You" response buttons that trigger special heart rain effects and sweet popup alerts.

---

## 🛠️ Technology Stack

- **Core**: HTML5, Vanilla JavaScript (ES6), CSS3 Custom Properties & Keyframes.
- **Libraries**:
  - [TypeIt.js](https://typeitjs.com/) (v8) — Used for smooth, letter-by-letter typing animations.
  - [SweetAlert2](https://sweetalert2.github.io/) (v11) — Used for stylized romantic modal overlays and inputs.
  - [ScrollReveal.js](https://scrollrevealjs.org/) — Used for scroll-triggered entry transitions.

---

## 📂 Project Structure

```directory
D:/I-Love-You-main/I-Love-You-main/
├── assets/                    # Image gifs, stickers, and audio resources
│   ├── 0906-peacegoma.gif     # Panda sticker for reasons header
│   ├── awan3.jpg              # Sky background wallpaper
│   ├── bunga.gif              # Flowers gif for certificate
│   ├── ciumin.gif             # Kissing gif for Swal confirmation
│   ├── cubit.gif              # Teasing sticker
│   ├── emawh.gif              # Hearts kissing sticker
│   ├── fullsenyum.mp3         # Background love track
│   ├── gemoy.gif              # Panda intro sticker
│   ├── gigitin.gif            # Bite panda sticker
│   ├── hiya.gif               # Happy panda sticker
│   ├── kadoin.png             # Closed gift box graphic
│   ├── ledekin.gif            # Playful sticker
│   ├── muah.gif               # Kiss sticker
│   └── terlope.gif            # Heart eyes sticker
├── index.html                 # Main entrypoint (CSS Styles & JS Scripts integrated)
└── README.md                  # This file
```

---

## 📱 Mobile Optimizations

The application implements several mobile-first web engineering practices:

- **Dynamic Viewport Heights (`100dvh`)**: Uses `dvh` units to prevent the browser's dynamic URL bar (iOS Safari / Android Chrome) from cutting off the layout.
- **Auto-Zoom Focus Mitigation**: Custom SweetAlert input text classes use `font-size: 16px` to prevent iOS from zooming in on text input focus.
- **Inertial Scrolling**: Enables `-webkit-overflow-scrolling: touch` for fluid scrolling behavior on iOS.
- **GPU Layer Release**: Resets the scale and translate transitions on `.reasons-card` after pop-in completion, preventing WebKit engines from freezing touch events on the element.
- **Viewport Boundaries**: Enforces `box-sizing: border-box` to avoid container padding pushing components off-screen.

---

## ⚙️ Customization Guide

### 1. Edit the 50 Reasons
Open [index.html](file:///D:/I-Love-You-main/I-Love-You-main/index.html) and locate the `reasons` array around line 970:
```javascript
const reasons = [
  "The way you make me smile just by thinking of you.",
  "Your cute laugh that instantly brightens up my entire day.",
  // Add, edit, or remove lines as desired...
];
```

### 2. Change the Background Music
To change the music track, replace the file at `./assets/fullsenyum.mp3` with your own audio file, or edit the source path in `index.html` (locate the `<audio>` tag or variables representing sound files).

### 3. Adjust the Scrolling Speed
Modify the `autoScrollSpeed` variable in the script block:
```javascript
let autoScrollSpeed = 1.2; // Increase for faster scrolling, decrease for slower
```

---

## 🚀 Running Locally & Deployment

### Local Setup
Simply double-click the `index.html` file to open it in any browser, or run a simple local development server using Python or Node:
```bash
# Using python
python -m http.server 8000

# Using Node.js npx
npx serve .
```

### Deploying to Web
You can host this project for free using popular static site hosters:
1. **GitHub Pages**: Push this directory to a repository, go to **Settings** > **Pages**, and choose the branch to publish.
2. **Netlify**: Drag and drop the project folder directly into the Netlify dropzone.
3. **Vercel**: Deploy via the Vercel CLI by typing `vercel` in the folder root.
