# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a Jekyll-based GitHub Pages personal website for Fahad Murtaza (fahdi.github.io). The site showcases personal information, GitHub repositories, and links to various profiles.

## Development Commands

### Local Development
```bash
bundle install          # Install Ruby dependencies
bundle exec jekyll serve # Start local development server (usually on http://localhost:4000)
```

### Deployment
The site automatically deploys to GitHub Pages when changes are pushed to the master branch.

## Architecture

### Jekyll Structure
- `_config.yml`: Main configuration file containing site settings, social media links, and feature toggles
- `_layouts/`: HTML templates (default, home, page, post)
- `_includes/`: Reusable HTML components (header, footer, about, blog-posts, github)
- `_sass/`: SCSS stylesheets organized by purpose
- `css/main.scss`: Main stylesheet entry point

### Key Features
- **GitHub Integration**: Dynamically fetches and displays GitHub repositories via API (js/github.js)
- **Social Profiles**: Configured links to Twitter, GitHub, Facebook, Flickr, Quora, LeetCode, HackerRank
- **Blog Integration**: Links to external blog (fahdmurtaza.com)
- **Responsive Design**: Uses Jekyll's minima theme

### Configuration Points
- GitHub repository display controlled by `github.repo_count` and `github.show_profile_link`
- About section toggle via `about.showMe`
- All social media URLs and usernames centrally managed in `_config.yml`

### JavaScript Components
- GitHub API integration in `js/github.js` fetches user repositories dynamically
- Uses jQuery for DOM manipulation and AJAX requests