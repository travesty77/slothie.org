# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project overview

Static single-page marketing site for Slothie — a fictional small-batch smoothie brand. No build step, no dependencies, no package manager.

## Local preview

Open `index.html` directly in a browser. That's it.

## Deployment

Hosted on Cloudflare Pages. Push to `master` and it deploys automatically. No build command or output directory is configured — the repo root is served as-is.

## Architecture

Everything lives in one file: `index.html` contains all HTML, CSS (in a `<style>` block), and inline SVG artwork. There are no external JS files, no frameworks, and no bundler. Google Fonts (DM Serif Display + DM Sans) are the only external dependency, loaded via `<link>` in `<head>`.

## Images

Real product photos (`mango-smoothie.jpg`, `green-smoothie.jpg`, `berry-smoothie.jpg`) exist in the repo root. The blend cards currently show SVG placeholder illustrations instead. To swap in real photos:

1. Move or copy the `.jpg` files into an `images/` subdirectory (or adjust the paths).
2. In each `.blend-card` in `index.html`, uncomment the `<img>` tag and delete the `<div class="blend-img-placeholder">` block above it.

The commented-out `<img>` tags reference `images/mango-hang.jpg`, `images/jungle-green.jpg`, and `images/lazy-berry.jpg` — update those `src` values to match the actual filenames.

## CSS conventions

CSS variables for the color palette are defined at the top of the `<style>` block under `:root`. All colors in the page reference these variables (`--bg`, `--green1`–`--green4`, `--text`, `--muted`, etc.). Add new colors there rather than inline.
