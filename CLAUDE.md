# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Single-file static portfolio/profile webpage with a cyberpunk/neon aesthetic. The entire site lives in `index.html` — no build system, no package manager, no tests.

## Development

Open `index.html` directly in a browser. No build step or server required.

## Architecture

- **Single-file app**: All HTML, CSS, and JS are in `index.html`
- **Language**: Japanese (lang="ja") — all UI text and code comments are in Japanese
- **Theming**: CSS custom properties on `:root` (`--text-main`, `--text-muted`, `--accent-color`, `--glass-bg`, `--glass-border`)
- **Layout**: CSS Grid (2-column, collapses to 1-column at 768px) with Flexbox for alignment
- **Design**: Glassmorphism cards with backdrop-filter blur, 3D transforms (preserve-3d, translateZ), neon glow effects

## External Dependencies (CDN-hosted, not local)

- **Three.js r134** — required by Vanta.js
- **Vanta.js 0.5.24** — `VANTA.NET` animated network background on `#vanta-bg`
- **Vanilla Tilt 1.8.0** — 3D tilt/glare effect on `.card` elements (configured via `data-tilt` attributes + JS init)
- **Google Fonts** — "M PLUS Rounded 1c" (400, 700)

## Key Conventions

- Color scheme: cyan accent `#00ffff` on dark navy `#0f172a`
- Cards use both HTML data attributes (`data-tilt`, `data-tilt-glare`, `data-tilt-max-glare`, `data-tilt-scale`) and JS initialization for Vanilla Tilt
- Vanta.js is applied to the `body` element via `id="vanta-bg"`

## Communication

- **返信は日本語で行うこと** — ユーザーへの応答はすべて日本語で記述する
