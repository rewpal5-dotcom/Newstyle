# ✨ Newstyle

**Name style generator — apna naam likhein, 40 styles mein dekhein, PNG download karein ya shareable link copy karein.**

Live site: **https://rewpal5-dotcom.github.io/Newstyle/**

Ek single-file static web app. Koi build step nahi, koi dependency nahi, koi backend nahi — sab kuch browser mein chalta hai.

## Features

- **40 styles**, 10 categories mein — Neon, 3D, Metallic, Outline, Glow, Retro, Minimal, Gaming, Nature, Fun
- Live preview — naam type karte hi har card aur bada preview update
- Search aur category filter
- 🎲 Random style button
- **PNG download** (1600×600, WhatsApp DP / thumbnail / banner ke liye)
- **Shareable link** — `?name=Rahul&style=gold-foil` jaisa URL, jise koi bhi khol sakta hai
- WhatsApp share button
- Poora responsive, mobile-first

## Styles kaise kaam karte hain

Har style ek hi config se do jagah render hota hai — screen par CSS se, aur download ke waqt `<canvas>` par:

```js
S("gold-foil", "Gold Foil", "Metallic", {
  fill: ["#fff8cc", "#b8860b"],   // gradient stops
  angle: 110,
  glow: { c: "#ffd75e", blur: 16 },
  stroke: null,
  shadow: null,
  hollow: false
})
```

- `fill` — gradient ke do rang (gradient text `background-clip: text` se banta hai)
- `stroke` — text outline
- `glow` — neon jaisa glow (multiple text-shadows / canvas shadowBlur)
- `shadow` — hard 3D shadow
- `hollow` — sirf outline, andar khaali
- `bg` — us style ka stage background

Naya style add karne ke liye `STYLES` array mein ek entry daal dein — grid, preview, PNG export sab apne aap update ho jayenge.

## Local run

```bash
git clone https://github.com/rewpal5-dotcom/Newstyle.git
cd Newstyle
python3 -m http.server 8080
# open http://localhost:8080
```

`index.html` ko seedha browser mein bhi khol sakte hain.

## Tech

Vanilla HTML + CSS + JavaScript. Fonts system ke hain, koi external request nahi — page offline bhi chalta hai.

## License

MIT
