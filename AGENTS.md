# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a Jekyll-based personal website for Kuristar, built using the Minima theme and deployed via GitHub Pages. The site focuses on astrology consultations and personal content.

## Development Commands

### Setup
```bash
bundle install                    # Install Ruby dependencies
```

### Local Development
```bash
bundle exec jekyll serve         # Start local development server (http://localhost:4000)
jekyll serve                     # Alternative command (if Jekyll is globally installed)
```

### Build
```bash
bundle exec jekyll build         # Build site to _site/ directory
bundle exec jekyll build --baseurl "/path"  # Build with custom base URL
```

## Architecture

### Site Structure
- `_config.yml` - Main Jekyll configuration
- `_layouts/default.html` - Custom site template with header, navigation, and footer
- `_posts/` - Blog posts in Markdown
- `assets/css/main.css` - Custom CSS styling
- `index.markdown` - Homepage content
- `about.markdown` - About page
- `kuristar.png` - Site logo used in header

### Key Configuration
- **Ruby Version**: 3.4.5 (specified in README)
- **Jekyll Theme**: Minima (with custom overrides)
- **Plugins**: jekyll-feed, github-pages
- **Domain**: kuristar.com
- **Base URL**: "/"

### Layout System
The site uses a custom `default.html` layout that includes:
- SEO meta tags and Open Graph support
- Custom header with logo and navigation
- Responsive navigation menu with sections: Home, Readings, Writing, About
- Semantic HTML structure with accessibility features

### Styling
- Custom CSS in `assets/css/main.css`
- CSS custom properties for consistent theming
- Responsive design with container-based layout
- Custom header branding with logo integration

## Deployment

The site is automatically deployed to GitHub Pages via GitHub Actions:
- **Trigger**: Push to `main` branch
- **Workflow**: `.github/workflows/jekyll.yml`
- **Ruby Version**: 3.4.1 (in Actions, differs from local 3.4.5)
- **Build Command**: `bundle exec jekyll build --baseurl`
- **Output**: `_site/` directory

## Important Notes

- The `_site/` directory is the build output and should not be edited directly
- The custom layout overrides the default Minima theme structure
- GitHub Pages deployment is handled automatically - just push to main
- The site excludes `README.md` and `CLAUDE.md` from processing (see `_config.yml`)