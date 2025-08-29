# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a Jekyll-based GitHub Pages personal website for Fahad Murtaza (fahdi.github.io). The site showcases personal information, GitHub repositories, and links to various profiles.

## Development Commands

### Local Development
```bash
# Set Ruby PATH (required on macOS with Homebrew Ruby)
export PATH="/opt/homebrew/opt/ruby/bin:/opt/homebrew/lib/ruby/gems/3.4.0/bin:$PATH"

# Install dependencies (if using bundler - may have compatibility issues)
bundle install

# Start development server (recommended approach)
jekyll serve --host 127.0.0.1 --port 4001 --livereload

# Alternative if bundler has issues (remove Gemfile temporarily)
mv Gemfile Gemfile.bak
jekyll serve --host 127.0.0.1 --port 4001 --livereload
mv Gemfile.bak Gemfile
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
- **GitHub Integration**: Dynamically fetches and displays GitHub repositories via fetch API in `_includes/head.html`
- **Social Profiles**: Configured links to Twitter, GitHub, Facebook, Flickr, Quora, LeetCode, HackerRank
- **Blog Integration**: Links to external blog (fahdmurtaza.com)
- **Responsive Design**: Uses Jekyll's minima theme

### Configuration Points
- GitHub repository display controlled by `github.repo_count` and `github.show_profile_link`
- About section toggle via `about.showMe`
- All social media URLs and usernames centrally managed in `_config.yml`

### JavaScript Components
- GitHub API integration implemented in `_includes/head.html` using modern fetch API
- Dynamically fetches and displays GitHub repositories from GitHub API
- Repository display limited to 90 items as configured in `_config.yml`
- Error handling for API failures with fallback messages
- Note: `js/github.js` is legacy and no longer used - actual implementation is in head.html

### Development Notes
- GitHub integration moved from `js/github.js` to `_includes/head.html` using fetch API
- Bundler may have compatibility issues with newer Ruby versions
- Port 4001 is used to avoid conflicts with other local servers
- LiveReload is enabled for automatic browser refresh during development
- Some Sass deprecation warnings are expected but don't affect functionality