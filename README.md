# Newstyle — Name Style Generator

**68 styles · live preview · PNG download · share link · favorites · settings · analytics**

Live: **https://rewpal5-dotcom.github.io/Newstyle-Web/**

## Pages

App paanch page ka hai, upar ke tabs se switch hota hai (URL hash routing):

| Page | Kya karta hai |
| --- | --- |
| **Home** | Naam input, bada live preview, PNG download, link copy, favorite, WhatsApp share, popular styles |
| **Styles** | Saare 68 styles, search, 15 category filters, card click se apply, heart se favorite |
| **Favorites** | Save kiye hue styles, yahin se hataye ja sakte hain |
| **Settings** | Default naam, preview size, PNG size (banner/DP/story), background, data reset |
| **Analytics** | Local stats — kitne previews, downloads, link copies, shares, aur top 6 styles |

## Styles

68 styles, 15 categories: Neon, 3D, Metallic, Outline, Glow, Retro, Minimal, Gaming, Nature, Fun, Texture, Cyber, Dark, Badge, Pro.

Har style ek config object se banta hai aur do jagah render hota hai — screen par CSS se, aur download ke waqt `<canvas>` par:

```js
S("gold-foil", "Gold Foil", "Metallic", {
  fill: ["#fff8cc", "#b8860b"],   // gradient stops
  angle: 110,
  glow: { c: "#ffd75e", blur: 16 },
  stroke: null, shadow: null, hollow: false
})
```

Gradient wale styles par `text-shadow` ki jagah `drop-shadow` filter use hota hai — warna shadow transparent glyphs ke through dikh jaata hai.

## Data

Sab kuch `localStorage` mein: `newstyle.settings`, `newstyle.favorites`, `newstyle.stats`. Koi backend nahi, koi account nahi, koi data bahar nahi jaata.

## Share link

`?name=Rahul&style=gold-foil` — link kholne par wahi naam aur style load ho jaate hain.

## Tech

Single file, vanilla HTML + CSS + JS. Koi dependency, koi external font, koi build step nahi.

## License

MIT
