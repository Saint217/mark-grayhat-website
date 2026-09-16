# Grayhat Global — Cybersecurity & Digital Forensics Consultant Website

A premium, deploy-ready static website for a cybersecurity and digital forensics consultant. Built with clean HTML5, CSS3, and vanilla JavaScript — no build tools required.

---

## 🚀 Features Implemented

| Feature | Status |
|---|---|
| Responsive navbar with mobile hamburger menu | ✅ |
| Sticky navbar with scroll-blur effect | ✅ |
| Full-screen hero with matrix rain canvas animation | ✅ |
| Animated floating security shield with orbiting rings | ✅ |
| Animated floating stat cards | ✅ |
| Proof strip with counter animation | ✅ |
| Services section (6 cards with feature lists) | ✅ |
| Industries section (8 audience cards) | ✅ |
| Results / Case Studies section (4 portfolio items) | ✅ |
| Process section (4-step with connector line) | ✅ |
| FAQ accordion with smooth animation | ✅ |
| Contact form with validation & Formspree ready | ✅ |
| Active nav-link via IntersectionObserver | ✅ |
| Scroll-to-top button | ✅ |
| AOS (Animate on Scroll) integration | ✅ |
| Full accessibility (skip link, ARIA labels, keyboard nav) | ✅ |
| `prefers-reduced-motion` support | ✅ |
| SEO meta tags + JSON-LD schema | ✅ |
| Footer with social links and nav columns | ✅ |
| Current year auto-update in footer | ✅ |
| Premium dark cyberpunk theme with CSS variables | ✅ |

---

## 📁 Project Structure

```
/
├── index.html              ← Main entry point
├── css/
│   └── style.css           ← Full premium stylesheet
├── js/
│   └── script.js           ← All interactivity and hooks
├── images/                 ← (add your images here)
│   └── og-cover.png        ← Open Graph cover image
└── README.md
```

---

## 🔌 Setup & Deployment

### 1. Deploy as-is (zero configuration)
The site is 100% static. Simply upload all files to any static host:
- **Genspark Publish tab** — one-click deploy (recommended)
- GitHub Pages
- Netlify (drag & drop)
- Vercel
- Any web server or CDN

### 2. Enable the Contact Form (required for live inquiries)

The form submits to a third-party backend configured in the `FORM_CONFIG` block near the top of `js/script.js`. Pick ONE option:

**Option A — Formspree (recommended):**
1. Go to [https://formspree.io](https://formspree.io) and create a free account
2. Create a new form and copy your **Form ID** (looks like `mzbnqkrv`)
3. In `js/script.js`, keep `provider: 'formspree'` and paste the ID into `formspreeId: 'mzbnqkrv'`
4. Save and redeploy

**Option B — Web3Forms:**
1. Go to [https://web3forms.com](https://web3forms.com), enter your email, and copy the **Access Key**
2. In `js/script.js`, set `provider: 'web3forms'` and paste the key into `accessKey: '...'`
3. Save and redeploy

**Option C — any custom JSON API:** set `provider: 'custom'` and fill `customEndpoint` with your endpoint URL.

Until a key is set, the form shows a clear notice with a direct-email fallback instead of failing silently. With JavaScript disabled, the form falls back to a `mailto:` submission.

### 3. Update your personal information

Search and replace across `index.html`:
- `contact@grayhatglobal.com` → your real email
- Social media links in the footer → your real profiles
- `https://linkedin.com/`, `https://github.com/`, `https://twitter.com/` → real URLs
- Meta tags `og:image` URL → your deployed domain
- Canonical URL (if you add one)

---

## 🧩 JavaScript Hooks Preserved

All hooks required by the original specification are present:

| Hook | Purpose |
|---|---|
| `#navbar` | Scroll class injection |
| `#mobileMenuToggle` | Hamburger toggle button |
| `#navMenu` | Mobile slide-in nav |
| `.nav-link` | Active state via IntersectionObserver |
| `#scrollTopBtn` | Scroll-to-top visibility toggle |
| `#contactForm` | Form submit handler |
| `#formStatus` | Alert messages (info/success/error) |
| `#name` | Form field: full name |
| `#email` | Form field: email address |
| `#phone` | Form field: phone |
| `#company` | Form field: organization |
| `#service` | Form field: service dropdown |
| `#message` | Form field: project details |
| `#urgent` | Form checkbox: urgent flag |
| `.btn-submit` | Submit button (loading state) |
| `#matrixRain` | Canvas for matrix rain effect |
| `#currentYear` | Auto-filled year in footer |

---

## 📚 External Libraries

| Library | Version | Purpose |
|---|---|---|
| Google Fonts (Orbitron, Rajdhani, JetBrains Mono) | Latest | Typography |
| Font Awesome | 6.5.1 | Icons |
| AOS (Animate on Scroll) | 2.3.4 | Scroll animations |

All loaded via CDN — no npm or build step needed.

---

## ♿ Accessibility

- Skip link for keyboard navigation
- All interactive elements have ARIA labels
- `aria-expanded` on mobile menu toggle
- `aria-live="polite"` on form status
- FAQ items keyboard-navigable (Enter / Space)
- Color contrast meets WCAG 2.1 AA on all text
- `prefers-reduced-motion`: matrix canvas disabled, animations muted

---

## 🛠 Customization Tips

### Colors
All colors are defined as CSS custom properties in `:root {}` in `css/style.css`. Change `--primary`, `--accent`, and `--bg` to retheme the entire site.

### Sections
Each section has a unique `id` matching the nav links. Add/remove sections freely — the IntersectionObserver will automatically pick up new section IDs if they have `data-section` attributes on their matching nav links.

### Stats
The proof counter targets are defined in `js/script.js` in the `initCounters()` function. Update the `targets` array to match your real numbers.

---

## 📋 Features Not Yet Implemented

- Blog/articles section
- Downloadable PDF case studies
- Calendly / booking widget integration
- Dark/light mode toggle (site is dark-mode only)
- Multi-language support

---

## 🔮 Recommended Next Steps

1. **Wire up the contact form** → Set your Formspree ID in `js/script.js`
2. **Update personal details** → Email, social links, canonical URL
3. **Add real case study content** → Replace placeholder text in the Results section
4. **Add OG cover image** → Create `images/og-cover.png` (1200×630px)
5. **Deploy** → Use the Publish tab or upload to your preferred host
6. **Test on mobile** → Verify all breakpoints at 320px, 375px, 768px, 1024px
7. **Run Lighthouse audit** → Aim for 90+ on all categories

---

*Built with precision. Designed for trust.*
