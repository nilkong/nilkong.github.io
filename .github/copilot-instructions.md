# Copilot Instructions for nil_main_website

## Project Overview

This is a Hugo static site generator blog deployed to GitHub Pages. It uses the **PaperMod** theme as a git submodule and is configured for mathematical expression rendering via MathJax.

## Build, Test, and Serve Commands

### Development Server
```bash
hugo server -D              # Start local server with drafts (default: http://localhost:1313)
hugo server                 # Start without drafts
```

### Build for Production
```bash
hugo build                  # Generate static site in ./public
hugo build --minify         # Build with minification
```

### Configuration and Debugging
```bash
hugo config                 # Display site configuration
hugo env                    # Display Hugo version and environment
hugo list all              # List all content
```

### Create New Content
```bash
hugo new content/posts/my-post.md    # Create new post with frontmatter template
hugo new content/notes/my-note.md    # Create new note page
```

## Architecture and Key Directories

### Site Structure
- **content/** - Markdown content files (posts, notes, special pages)
  - `posts/` - Blog articles
  - `search.md` - Search page
  - `archives.md` - Archives page
- **layouts/** - Custom Hugo layout overrides
  - `_partials/math.html` - MathJax configuration for LaTeX rendering
- **themes/PaperMod/** - Git submodule containing the PaperMod theme
- **static/** - Static assets (CSS, JS, images)
- **assets/** - Hugo pipeline assets
- **public/** - Generated site output (do not commit)
- **i18n/**, **data/** - Empty directories for future i18n/data usage

### Site Configuration
- **hugo.yaml** - Main configuration file
  - Base URL: `https://nilkong.github.io`
  - Theme: PaperMod
  - Outputs: HTML, RSS, JSON
  - LaTex: Enabled via Goldmark passthrough for block (`$$...$$`, `\[...\]`) and inline (`$...$`, `\(...\)`) math

## Key Conventions

### Content Structure
1. **YAML Front Matter** - All posts use YAML front matter with these fields:
   - `title`: Page title
   - `date`: Publication date (ISO 8601 format)
   - `tags`: List of tags
   - `categories`: List of categories (optional)
   - `author`: Author name(s)
   - `draft`: Boolean to exclude from builds
   - `showToc`: Show table of contents
   - Standard PaperMod fields: `comments`, `hidemeta`, `description`, etc.

2. **Math Rendering**
   - Block math: Use `$$...$$ ` or `\[...\]`
   - Inline math: Use `$...$` or `\(...\)`
   - MathJax is automatically loaded via custom partial

3. **Menu System** - Configured in hugo.yaml:
   - Search: weight 10
   - Archive: weight 20
   - Categories: weight 30
   - Tags: weight 40
   - Lower weights appear first

### Theme Customization
- Override PaperMod layouts by creating files in `layouts/` (mirroring theme structure)
- Custom partials go in `layouts/_partials/`
- Current customization: Math support via `_partials/math.html`

### Git Workflow
- PaperMod theme is a git submodule; clone with `git clone --recurse-submodules`
- Do not commit the `public/` directory
- Do not modify theme files directly; use layout overrides instead

## Development Tips

- Use `hugo server -D` to preview drafts locally before publishing
- Use draft: true in frontmatter to hide posts during development
- Check `hugo config` output to verify settings are loading correctly
- Run `hugo build` before committing to catch any build errors
