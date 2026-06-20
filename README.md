# 🌟 Portfolio Creation Guide

A modern, highly performant, server-side rendered (SSR) portfolio project scaffolding. Built using **Astro 5**, styled with **Tailwind CSS**, and optimized for deployment to **Cloudflare Workers/Pages** (Edge SSR).

---

## 🚀 Stack

- **Framework:** [Astro 5](https://docs.astro.build/en/getting-started/) (configured for hybrid/SSR)
- **Deployment Platform:** [Cloudflare Pages](https://docs.astro.build/en/guides/integrations-guide/cloudflare/) (using `@astrojs/cloudflare` adapter)
- **Styling:** [Tailwind CSS](https://tailwindcss.com/)
- **Runtime:** Cloudflare Workers (SSR on the Edge)

---

## 📁 Project Structure

```text
├── src/
│   ├── layouts/
│   │   └── Layout.astro   # Main HTML page shell and layout configuration
│   └── pages/
│       └── index.astro    # Home page with responsive sections (Hero, About, Work, Skills, Contact)
├── astro.config.mjs       # Astro configuration with Tailwind and Cloudflare adapter
├── package.json           # Project metadata, scripts, and dependencies
└── wrangler.toml          # Cloudflare Pages deployment configuration
```

---

## ⚙️ Development & Scripts

Inside the sandbox, dependencies are pre-installed. You can manage and run the project using the following scripts:

### Development Server
Starts a local development server with hot-module reloading (HMR).
```bash
npm run dev
```

### Build for Production
Compiles and bundles the application for a production environment.
```bash
npm run build
```

### Local Preview
Previews the compiled production build locally.
```bash
npm run preview
```

### Deploy to Cloudflare
Deploys the production build folder (`dist`) directly to Cloudflare Pages.
```bash
npm run deploy
```

---

## 🎨 Layout & Design Choices

The home page layout (`src/pages/index.astro`) has been tailored using modern design patterns:
- **Responsive Layouts:** Implemented with Tailwind breakpoints (`md:`, `lg:`) to look striking on mobile, tablet, and desktop viewports.
- **Color Gradients:** Subtle, modern gradient transitions from light slate to white (dark mode compatible with slate-900 to slate-950).
- **Semantics & Accessibility:** Built using clean, native HTML tags with descriptive classes, focus ring styling, and readable typography.
- **Edge Integration:** Fully ready to plug in Cloudflare KV, D1 databases, or R2 buckets using `Astro.locals.runtime.env` in Astro frontmatter for dynamic content.
