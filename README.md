# 🎄 2025 Christmas Greeting Webpage

A festive, interactive 3D webpage built with **Three.js**. It features a glowing particle Christmas tree, a built-in music player, real-time photo hanging, and a magical "wish moment". Just open the file, add your favourite Christmas songs, and share the holiday spirit!

---

## ✨ Live Demo

Simply open `index.html` in any modern browser (Chrome, Edge, Firefox recommended).  
No server required – it runs entirely client‑side.

> **Note:** Music files **must** be placed in the same folder as `index.html` for the playlist to work.

---

## 🎵 Prepare Your Music

Place your `.mp3` files in the same directory and update the `playlist` array inside `index.html` with the exact filenames:

```javascript
const playlist = [
    "Frank Sinatra - Let It Snow!.mp3",
    "We Wish You a Merry Christmas.mp3",
    "Wham! - Last Christmas.mp3",
    "Your Song Here.mp3"
];
```

The built‑in playlist is just an example – replace it with your own songs.

---

## 🚀 How to Use

1. **Clone or download** this repository.
2. Put your music files (`.mp3`) next to `index.html`.
3. Open `index.html` with a browser.
4. Use the controls:
   - **⏮ ⏭** – Previous / next song
   - **▶/⏸** – Play / pause the current track
   - **📷 挂上照片** – Upload a photo to pin it onto the tree
   - **✨ 许愿时刻** – Toggle a gold flash effect for 3 seconds (the tree then returns to its original colors)
5. Click on the gift boxes at the bottom for a surprise message!

---

## 🌟 Features

- **3D Particle Tree** – 50,000 red, green, and silver particles arranged in a cone shape with additive blending.
- **Neon Ribbons** – Two spiral tube lights that continuously cycle through rainbow hues.
- **Festive Decorations** – Ornaments, a glowing star, and interactive gifts.
- **Music Player** – Custom playlist with previous/next controls and error handling for missing files.
- **Photo Hanging** – Upload any image to place it on the tree as a textured quad.
- **Magic Wish Moment** – Turns the entire tree gold for a few seconds, then smoothly restores its original colors.
- **Responsive & Touch‑friendly** – Works on desktop and mobile devices.
- **Auto‑rotate OrbitControls** – Drag to rotate, pinch to zoom.

---

## 📁 File Structure

```
your-project/
├── index.html          # Main webpage
├── README.md           # This file
├── *.mp3               # Your Christmas songs (not included)
└── (optional) photos you upload are only displayed in the browser
```

All 3D libraries are loaded from CDN, so an internet connection is required on first load (they will be cached afterwards).

---

## 🔧 Customization

- **Change the playlist**: Edit the `playlist` array in `<script>`.
- **Adjust particle count**: Modify `particleCount` inside `buildTriColorTree()` (be careful with performance on mobile).
- **Change the fog/ambient colour**: Look for `scene.fog` and `AmbientLight`.
- **Replace the wish message**: `triggerMagic()` shows a toast – you can change the text there.

---

## ⚠️ Important Notes

- **Autoplay policy**: Modern browsers often block autoplay until the user interacts with the page. The first click on the play button will start the music.
- **Music filenames**: They must match exactly (including spaces, punctuation, and `.mp3` extension). If a file is missing, a toast will warn you.
- **Performance**: The pixel ratio is capped to `2` to avoid high GPU usage on mobile devices. If you have a very large number of particles, test on your target devices.

---

## ❤️ Credits

- 3D engine: [Three.js](https://threejs.org/) (r128)
- Controls: OrbitControls from Three.js examples
- Design and code: your own festive creation 😊

---

> “If you’re coming from WeChat, come find me for a mysterious gift!” 🎅

**Merry Christmas 2025 – and best wishes for 2026!**
