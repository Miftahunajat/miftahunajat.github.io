# Content Cleanup Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Generalize current-role experience bullets and remove extra bottom/contact content.

**Architecture:** The Hugo Profile site is configured through `hugo.yaml`; footer visibility is adjusted through theme params and CSS in `static/style.css` if needed. Verification is a Hugo build plus generated HTML checks.

**Tech Stack:** Hugo, YAML, CSS.

---

### Task 1: Generalize Current Experience Bullets

**Files:**
- Modify: `hugo.yaml`

- [x] Replace the three Gojek bullets with generic backend/system ownership bullets that do not mention case-specific product names.
- [x] Preserve impact metrics: 5% booking lift, 20,000 streaming messages per second, 18,000 transactions per minute, $5,000/month cost reduction, 50% incident reduction, 200ms latency reduction.

### Task 2: Remove Contact And Bottom Footer Extras

**Files:**
- Modify: `hugo.yaml`
- Modify: `static/style.css`
- Create: `layouts/partials/sections/footer/index.html`

- [x] Clear `params.contact.content` so the Get In Touch section shows only the heading and email button.
- [x] Remove footer social network links from `params.footer.socialNetworks`.
- [x] Override the footer partial so no bottom logo/photo or attribution area is rendered below the page content.

### Task 3: Verify

**Files:**
- None

- [ ] Run `hugo --minify`.
- [ ] Confirm generated `public/index.html` contains the generalized bullets.
- [ ] Confirm generated `public/index.html` does not contain the removed contact paragraph or footer social links.
