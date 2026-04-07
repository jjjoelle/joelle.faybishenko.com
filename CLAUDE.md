# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Overview

Static personal academic website for Joelle Faybishenko. No build system, no dependencies — plain HTML and CSS, deployed via GitHub Pages (CNAME: `faybishenko.com`).

## Structure

- `index.html` — About page (bio, education, publications, awards, skills)
- `projects.html` — Research projects and publications
- `blog.html` — Blog (currently empty, template comment included)
- `style.css` — All styles for all pages

## Design System

All CSS lives in `style.css`. Key CSS custom properties (defined in `:root`):
- `--color-accent: #F78E69` — primary accent color (links, highlights, timeline dots)
- `--color-bg: #fafaf9`, `--color-text: #1c1917`, `--color-text-secondary: #57534e`
- `--max-width: 820px` — single-column centered layout
- `--font-sans: 'Inter'`, `--font-serif: 'Lora'` — sans for body, serif for headings/logo

## Reusable Patterns

**Cards** (projects): `.card` inside `.card-grid` with `.card-label`, `h3`, `p`, and `.tags`/`.tag`

**Timeline** (education, experience): `.timeline-item` with `h3`, `.meta`, optional `p`

**Publication groups** (index.html): `.pub-group` > `.pub-group-title` + `.pub-item`

**Blog posts**: `.blog-post-preview` with `.date`, `h3 > a`, `p` — template comment in `blog.html`

**Active nav link**: add `class="active"` to the `<a>` matching the current page

## Navigation

The hamburger menu toggle works via inline `onclick` that toggles `.open` on `.nav-links`. No JavaScript files — all behavior is inline.
