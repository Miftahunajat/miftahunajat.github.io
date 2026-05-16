# Hugo Profile Redesign Design

## Goal

Migrate the portfolio from Next.js to Hugo using `gurusabarish/hugo-profile`, matching the simple one-page structure of `howico.de`.

## Scope

The site will expose only these homepage sections:

- Hero intro: `Hi, I'm`
- `About Me`
- `Experience`
- `Get In Touch`

Projects, achievements, education, blog, gallery, and extra navigation sections are out of scope.

## Content

Content is rewritten from `public/Resume.pdf` into a hybrid backend engineer and systems/product impact profile. Experience entries cover Tiket.com, Bukalapak, GDPLabs, and Mekari.

## Architecture

The repository becomes a Hugo site. `hugo.yaml` owns site configuration and homepage content. The Hugo Profile theme is added under `themes/hugo-profile`. Static assets live under `static/` and GitHub Pages builds the generated `public/` artifact.

## Verification

No tests are required by request. Verification is limited to running a Hugo build when the Hugo CLI is available.
