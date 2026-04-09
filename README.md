# jamestannahill-fonts

Self-hosted WOFF2 font files served via [fonts.jamestannahill.com](https://fonts.jamestannahill.com) — a dedicated CloudFront CDN backed by S3.

Used across [jamestannahill.com](https://www.jamestannahill.com), [plocamium.com](https://plocamium.com), and related properties.

---

## Fonts

### Neue Haas Grotesk Display (NHG Display)

| File | Weight | Style |
|------|--------|-------|
| `NHGDisplay-Roman.woff2` | 400 | Normal |
| `NHGDisplay-Light.woff2` | 300 | Normal |
| `NHGDisplay-Medium.woff2` | 500 | Normal |
| `NHGDisplay-Bold.woff2` | 700 | Normal |
| `NeueHaasDisplayRoman.woff2` | 400 | Normal |
| `NeueHaasDisplayRomanItalic.woff2` | 400 | Italic |
| `NeueHaasDisplayMediu.woff2` | 500 | Normal |
| `NeueHaasDisplayBold.woff2` | 700 | Normal |
| `NeueHaasDisplayBoldItalic.woff2` | 700 | Italic |

### Avenir LT Std

| File | Weight | Style |
|------|--------|-------|
| `Avenir-85-Heavy.woff2` | 800 | Normal |
| `AvenirLTStd-Heavy.woff2` | 800 | Normal |

### Bergoom

| File | Weight | Style |
|------|--------|-------|
| `Bergoom-Regular.woff2` | 400 | Normal |
| `Bergoom-Italic.woff2` | 400 | Italic |
| `Bergoom-Semibold.woff2` | 600 | Normal |
| `Bergoom-Bold.woff2` | 700 | Normal |
| `Bergoom-BoldItalic.woff2` | 700 | Italic |

---

## Usage

### CDN (recommended)

Link the hosted CSS:

```html
<link rel="stylesheet" href="https://fonts.jamestannahill.com/nhg-display.css">
```

Then use in CSS:

```css
font-family: 'NHG Display', sans-serif;
font-weight: 400; /* Roman */
font-weight: 500; /* Medium */
font-weight: 700; /* Bold */
```

### Direct `@font-face`

```css
@font-face {
  font-family: 'NHG Display';
  src: url('https://fonts.jamestannahill.com/NHGDisplay-Roman.woff2') format('woff2');
  font-weight: 400;
  font-style: normal;
  font-display: swap;
}

@font-face {
  font-family: 'NHG Display';
  src: url('https://fonts.jamestannahill.com/NHGDisplay-Medium.woff2') format('woff2');
  font-weight: 500;
  font-style: normal;
  font-display: swap;
}

@font-face {
  font-family: 'NHG Display';
  src: url('https://fonts.jamestannahill.com/NHGDisplay-Bold.woff2') format('woff2');
  font-weight: 700;
  font-style: normal;
  font-display: swap;
}

@font-face {
  font-family: 'Avenir Heavy';
  src: url('https://fonts.jamestannahill.com/Avenir-85-Heavy.woff2') format('woff2');
  font-weight: 800;
  font-style: normal;
  font-display: swap;
}
```

---

## Infrastructure

- **S3 bucket:** `fonts.jamestannahill.com`
- **CDN:** Amazon CloudFront
- **Origin:** S3 with public read access
- **CORS:** Enabled for cross-origin font loading
- **Cache:** Long TTL (1 year) — files are content-addressed
