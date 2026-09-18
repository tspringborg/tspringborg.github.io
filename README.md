# lab

Personal creative coding lab. Built with [Astro](https://astro.build), deployed to GitHub Pages.

## Pages

| Route | Description |
|-------|-------------|
| `/` | Landing — particle field hero |
| `/lab` | Experiment index grid |
| `/about` | Bio, stack, contact |

## Local dev

```bash
npm install
npm run dev
```

## Deploy

The GitHub Actions workflow in `.github/workflows/deploy.yml` handles deployment automatically on push to `main`.

**One-time setup:**
1. Go to your repo → Settings → Pages
2. Set Source to **GitHub Actions**
3. Update `site` in `astro.config.mjs` to your GitHub Pages URL

## Adding experiments

Edit the `experiments` array in `src/pages/lab.astro`. Each entry:

```js
{
  slug: 'my-experiment',
  title: 'My Experiment',
  description: 'One sentence description.',
  tags: ['webgl', 'canvas'],
  date: '2024-07',
  status: 'live', // or 'wip'
  href: '/lab/my-experiment', // or external URL
}
```
