# GlassScholar Academic Homepage

[![LICENSE](https://img.shields.io/github/license/yaoyao-liu/minimal-light?style=flat-square&logo=creative-commons&color=EF9421)](https://github.com/yaoyao-liu/minimal-light/blob/main/LICENSE)

EN / [简体中文](README_cn.md)

This is an academic homepage deeply rebuilt from [Minimal Light](https://github.com/yaoyao-liu/minimal-light). It aims to be a more modern, data-driven personal page solution suitable for everyone from undergraduates to researchers. It retains the lightweight deployment experience of Jekyll + GitHub Pages while adding capabilities such as project experience, competition awards, education cards, timelines, glassmorphism UI, interactive enhancements, and modular configuration.

This repository is already organized for public showcase and further customization. The default content uses a set of sample data that you can directly replace, making it easy to fork and quickly turn into your own homepage.

**Click to see the demo 👇**

[![1776421447735-3ex3o1.png](https://img.130923.xyz/pic/2026/1776421447735-3ex3o1.png)](https://lsqkk.github.io/GlassScholar)

## Who is it for?

- Undergraduates, graduate students, and early-career researchers who want to quickly build a personal academic homepage
- Students who may not have formal publications yet but have accumulated projects, competitions, blogs, or engineering practice
- Those who want to keep the lightweight static site deployment while enjoying a richer visual and interactive experience

## Current Version Features

### Content Structure

- Supports `About Me`, `Technical Skills`, `Education`, `Project Experience`, `Competitions & Awards`, `News`, `Publications`, `Services`, and `Repository Board` – all modularized
- The main homepage structure is defined in `index.md`, with specific content driven by `_data/*.yml`
- Education, projects, news, services, skills, etc., each have their own data files for easy maintenance
- Module visibility is controlled via `_config.yml`

### UI & Interaction

- Projects are displayed in a reverse-chronological timeline, showing the latest 5 entries by default with expand/collapse support
- News uses a distinct timeline style that remains consistent with the project section without being repetitive
- Education is presented as clickable cards, with the whole card linking to the institution page
- Competitions & awards section has uniform image widths and stable text alignment
- The entire page features a mouse-following ambient glow and subtle background gradients
- Glassmorphism cards use semi-transparent backgrounds, blur, inner highlights, and ambient lighting effects
- All images support click-to-enlarge lightbox with fade-in zoom, click outside to close, close button in the top-right corner, and `Esc` key to close
- The left sidebar (profile info) stays fixed on desktop, remaining visible while scrolling through long pages
- The top profile area includes a looping typewriter animation

### Open Source & Repository Display

- The footer can dynamically fetch a repository board via the GitHub API
- The default repository board configuration can be directly replaced in `_config.yml`
- Clear attribution that this template is a deep modification of the open-source Minimal Light theme

### Engineering & Deployment

- Maintains the Jekyll / GitHub Pages static deployment approach
- Automatically adapts to light/dark mode
- Retains basic SEO configuration, social links, avatar, favicon, custom fonts, etc.
- Supports local preview with `bundle exec jekyll serve --livereload`

## Project Structure

```text
.
├── _config.yml                 # Site config, module visibility, repo board settings
├── _data
│   ├── awards.yml              # Awards data
│   ├── education.yml           # Education data
│   ├── news.yml                # News/updates data
│   ├── profile.yml             # About & Skills data
│   ├── project.yml             # Project experience data
│   ├── publications.yml        # Publications data
│   └── services.yml            # Services/reviewing data
├── _includes
│   ├── about.md
│   ├── awards.md
│   ├── education.md
│   ├── news.md
│   ├── project.md
│   ├── publications.md
│   ├── repo-board.md
│   ├── services.md
│   ├── services-section.md
│   └── skills.md
├── _layouts
│   └── homepage.html           # Homepage layout template
├── _sass
│   ├── minimal-light.scss
│   └── minimal-light-no-dark-mode.scss
├── assets
│   ├── css
│   │   ├── style.scss
│   │   └── style-no-dark-mode.scss
│   ├── img
│   ├── files
│   └── js
│       └── homepage-ui.js      # Expand/collapse, glow, typewriter, lightbox, GitHub API board
└── index.md                    # Homepage module entry
```

## Quick Start

### Option 1: Fork directly

1. Fork this repository to your GitHub account
2. Rename the repository to `your-username.github.io`, or name it as needed for your Pages setup
3. Enable deployment in GitHub Pages
4. Modify the content in `_config.yml` and `_data/*.yml`

### Option 2: Preview locally before deploying

After installing Ruby, run in the project directory:

```bash
bundle install
bundle exec jekyll serve --livereload
```

Open in your browser:

```text
http://127.0.0.1:4000/
```

To only generate static files:

```bash
bundle exec jekyll build
```

For more details and troubleshooting, refer to the original [Minimal Light](https://github.com/yaoyao-liu/minimal-light) theme documentation.

## How to Edit Content

### Personal Info & Skills

Edit:

- `_config.yml`
- `_data/profile.yml`

Where:

- `_config.yml` controls name, institution, avatar, email, social links, and module visibility
- `_data/profile.yml` controls `About Me` and `Technical Skills`

### Education

Edit `_data/education.yml`. Supported fields:

- `school`
- `program`
- `period`
- `start_date`
- `focus`
- `summary`
- `link`
- `highlights`

### Project Experience

Edit `_data/project.yml`. Supports:

- Detailed `date`
- Project title, description, tech stack, outcomes, image, and link

Projects are automatically sorted in reverse chronological order.

### News & Updates

Edit `_data/news.yml` and maintain entries by date.

### Awards

Edit `_data/awards.yml`.

### Publications & Services

Edit:

- `_data/publications.yml`
- `_data/services.yml`

These two modules are hidden by default in the current version. To enable them, simply toggle the switches in `_config.yml`.

## Module Visibility Control

It is recommended to control module visibility centrally via `_config.yml`:

```yaml
section_visibility:
  about: true
  education: true
  projects: true
  awards: true
  publications: false
  services: false
  skills: true
  news: true
  repo_board: true
```

## Repository Board Configuration

The GitHub API repository board in the footer is also configured via `_config.yml`:

```yaml
repo_board:
  owner: yaoyao-liu
  name: minimal-light
  url: https://github.com/yaoyao-liu/minimal-light
```

You can replace this with your own repository details, and the page will automatically display your project repository data.

## Additional Notes

- The default person, project, experience, and news content in this repository are organized as sample data that can be directly replaced, making it suitable for public repository display
- To deploy as your own site, prioritize replacing `_config.yml` and `_data/*.yml`
- If you have your own avatar, CV, or PDF attachments, place the corresponding files in `assets/img` or `assets/files`

## Based on Open Source Projects

This project builds upon the following open-source work:

- [yaoyao-liu/minimal-light](https://github.com/yaoyao-liu/minimal-light)
- [pages-themes/minimal](https://github.com/pages-themes/minimal)
- [orderedlist/minimal](https://github.com/orderedlist/minimal)
- [al-folio](https://github.com/alshedivat/al-folio)

## License

This project inherits the licensing system of the original theme. The original theme is licensed under [Creative Commons Zero v1.0 Universal](https://github.com/yaoyao-liu/minimal-light/blob/master/LICENSE).

## Acknowledgements

If this template helps you, feel free to Star, Fork, or continue to customize it in your own direction. It works great as a lightweight yet not简陋 (bare-bones) starting point for an academic homepage.