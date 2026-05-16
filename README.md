# Miftahun Najat Portfolio

This is a Hugo portfolio site using the [Hugo Profile](https://github.com/gurusabarish/hugo-profile) theme.

## Development

Install Hugo, then run:

```bash
hugo server
```

Open [http://localhost:1313](http://localhost:1313) in your browser.

## Build

```bash
hugo --minify
```

The generated static site is written to `public/`.

## Content

Homepage content and section configuration live in `hugo.yaml`.

## Deployment

GitHub Actions builds the Hugo site and deploys `public/` to GitHub Pages.
