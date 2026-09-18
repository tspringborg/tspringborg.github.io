# lab — creative coding site

Personal creative lab site. Astro, static, deployed to GitHub Pages.

## Structure

```
src/
├── layouts/Base.astro        # html shell, nav, font imports
├── pages/
│   ├── index.astro           # hero — live canvas particle field
│   ├── lab.astro             # experiment grid
│   └── about.astro           # bio, stack, contact
├── styles/global.css         # design tokens, reset, utilities
public/
└── favicon.svg
.github/workflows/deploy.yml  # pushes dist/ to GitHub Pages on main
```

## Design tokens

- Background: `#0a0a0f`, surface: `#111118`, border: `#1e1e2e`
- Accent: `#7b61ff`, accent-hi: `#a599ff`
- Fonts: JetBrains Mono (structural/mono) + Inter (body) via Google Fonts

## Adding experiments

Edit the `experiments` array in `src/pages/lab.astro`:

```js
{
  slug: 'my-thing',
  title: 'My Thing',
  description: 'One sentence.',
  tags: ['webgl', 'canvas'],
  date: '2024-07',       // YYYY-MM
  status: 'live',        // 'live' | 'wip'
  href: '/lab/my-thing', // or external URL
}
```

## Deploy

Push to `main` — the Actions workflow handles the rest.

First-time setup:
1. Repo Settings → Pages → Source: **GitHub Actions**
2. Update `site` in `astro.config.mjs` to your actual Pages URL

## Local dev

```bash
npm install
npm run dev
```
