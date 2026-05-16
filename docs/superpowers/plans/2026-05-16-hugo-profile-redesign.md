# Hugo Profile Redesign Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Replace the current Next.js portfolio with a Hugo Profile site containing only hero, About Me, Experience, and Get In Touch sections.

**Architecture:** Use Hugo as the static site generator and `gurusabarish/hugo-profile` as the theme. Keep all homepage content in `hugo.yaml`, use `static/` for assets, and update GitHub Pages to build Hugo output from `public/`.

**Tech Stack:** Hugo, Hugo Profile, YAML, GitHub Actions.

---

### Task 1: Theme And Hugo Configuration

**Files:**
- Create: `.gitmodules`
- Create: `themes/hugo-profile`
- Create: `hugo.yaml`
- Create: `content/_index.md`
- Create: `static/images/profile.svg`
- Copy: `public/Resume.pdf` to `static/Resume.pdf`

- [x] Add the Hugo Profile theme as a git submodule at `themes/hugo-profile`.
- [x] Create `hugo.yaml` with homepage sections enabled only for hero, about, experience, and contact.
- [x] Create `content/_index.md` with minimal front matter for the home page.
- [x] Add a lightweight profile SVG for the hero/about image.
- [x] Copy the resume PDF into Hugo's `static/` directory.

### Task 2: Remove Next.js App Surface

**Files:**
- Delete: Next.js app, component, config, package, and generated-public source files.
- Modify: `.gitignore`

- [x] Remove Next.js-specific files that are no longer used by Hugo.
- [x] Ignore `.superpowers/`, `.hugo_build.lock`, and Hugo's generated `/public/` output.

### Task 3: GitHub Pages Deployment

**Files:**
- Delete: `.github/workflows/nextjs.yml`
- Create: `.github/workflows/hugo.yml`

- [x] Replace the Next.js workflow with a Hugo workflow.
- [x] Ensure checkout initializes submodules.
- [x] Upload Hugo's generated `public/` directory.

### Task 4: Verification

**Files:**
- None

- [x] Run `hugo --minify` if the Hugo CLI is installed.
- [x] Confirm generated HTML contains only the requested homepage sections in navigation.
