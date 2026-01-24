# CLAUDE.md - AI Assistant Guide

This document provides comprehensive guidance for AI assistants working on the mikethemelanson.github.io repository.

## Repository Overview

**Repository Name:** mikethemelanson.github.io
**Type:** GitHub Pages Personal Website
**Purpose:** Personal website hosted on GitHub Pages
**URL:** https://mikethemelanson.github.io
**Current State:** Early development - minimal placeholder content

## Project Structure

```
mikethemelanson.github.io/
├── .git/                 # Git repository metadata
├── README.md             # Repository introduction
├── index.htm             # Main entry point for the website
└── CLAUDE.md            # This file - AI assistant guide
```

### Key Files

- **index.htm** - Main HTML file served as the homepage. Currently contains a simple "Hello world" placeholder.
- **README.md** - Repository readme visible on GitHub, contains basic project description.

## Technology Stack

- **Frontend:** Plain HTML (no framework currently)
- **Hosting:** GitHub Pages
- **Version Control:** Git/GitHub

## Development Workflow

### Branch Strategy

- **Main Branch:** Production branch that deploys to GitHub Pages
  - All code on main is automatically deployed
  - Keep main branch stable and deployable

- **Feature Branches:** Use `claude/` prefix for AI-assisted development
  - Pattern: `claude/description-sessionid`
  - Example: `claude/claude-md-mksfmqd1hz6tkjb0-htzBR`
  - Always develop on feature branches, never directly on main

### Git Operations

**Committing Changes:**
- Use clear, descriptive commit messages
- Follow conventional commits format when possible:
  - `feat:` for new features
  - `fix:` for bug fixes
  - `docs:` for documentation changes
  - `style:` for formatting changes
  - `refactor:` for code refactoring
  - `test:` for adding tests

**Pushing Changes:**
- Always use: `git push -u origin <branch-name>`
- Branch names MUST start with `claude/` and include the session ID
- On network failures, retry up to 4 times with exponential backoff (2s, 4s, 8s, 16s)

**Creating Pull Requests:**
- Use `gh pr create` with descriptive title and body
- Include a summary of changes
- Add a test plan when applicable
- Reference any related issues

### Deployment

- GitHub Pages automatically deploys from the main branch
- Changes pushed to main go live immediately
- No build process currently configured
- Files are served as-is from the repository

## Key Conventions

### HTML Standards

- Use semantic HTML5 elements
- Keep markup clean and accessible
- Include proper DOCTYPE declaration
- Use lowercase for element names and attributes
- Quote all attribute values
- Close all tags properly

### File Naming

- Use lowercase for filenames
- Use hyphens for multi-word filenames (kebab-case)
- HTML files: `.html` or `.htm` extension
- CSS files: `.css` extension
- JavaScript files: `.js` extension

### Code Style

- **Indentation:** Use 4 spaces (current convention based on index.htm)
- **Line Length:** No strict limit, but prefer readability
- **Formatting:** Keep code clean and well-formatted
- **Comments:** Add comments for complex logic, but prefer self-documenting code

### File Organization

As the site grows, follow this structure:
```
/
├── index.html           # Homepage
├── about.html           # About page
├── css/                 # Stylesheets
│   └── style.css
├── js/                  # JavaScript files
│   └── main.js
├── images/              # Image assets
├── assets/              # Other static assets
└── pages/               # Additional HTML pages
```

## Guidelines for AI Assistants

### Before Making Changes

1. **Always read files before modifying** - Never propose changes to code you haven't seen
2. **Check current conventions** - Match existing code style and patterns
3. **Understand the context** - Read related files to understand dependencies
4. **Verify file paths** - Ensure paths exist before creating new files

### When Writing Code

1. **Keep it simple** - This is a static site, avoid over-engineering
2. **No unnecessary frameworks** - Only add libraries if explicitly requested
3. **Maintain accessibility** - Follow WCAG guidelines
4. **Responsive design** - Ensure mobile compatibility
5. **Browser compatibility** - Use widely supported features
6. **Performance** - Optimize images, minimize assets
7. **Security** - Sanitize any user inputs, avoid XSS vulnerabilities

### What to Avoid

- ❌ Don't add features that weren't requested
- ❌ Don't refactor code unnecessarily
- ❌ Don't add comments to code you didn't change
- ❌ Don't add complexity for hypothetical future needs
- ❌ Don't push directly to main branch
- ❌ Don't skip reading files before editing
- ❌ Don't add build tools without explicit request

### Task Management

- Use TodoWrite tool to plan and track multi-step tasks
- Mark todos as completed immediately after finishing
- Only one task should be in_progress at a time
- Break complex tasks into smaller, manageable steps

### Communication

- Be concise and clear in responses
- Use markdown formatting for readability
- Reference files with `file:line` pattern (e.g., `index.htm:3`)
- Output text directly - never use bash echo to communicate
- Don't use emojis unless explicitly requested

## Common Tasks

### Adding a New Page

1. Create HTML file following naming conventions
2. Link from index.htm or navigation menu
3. Ensure consistent header/footer structure
4. Test all links work correctly
5. Commit with descriptive message
6. Create PR if on feature branch

### Adding Styles

1. Create `css/` directory if it doesn't exist
2. Create or edit CSS file
3. Link stylesheet in HTML `<head>` section
4. Use mobile-first responsive design
5. Test across different screen sizes

### Adding JavaScript

1. Create `js/` directory if it doesn't exist
2. Create JavaScript file
3. Link script before closing `</body>` tag (or in `<head>` with `defer`)
4. Use vanilla JavaScript unless framework requested
5. Handle errors gracefully
6. Test functionality thoroughly

### Adding Images

1. Create `images/` or `assets/` directory
2. Optimize images before adding (compress, resize)
3. Use appropriate formats (WebP, PNG, JPG, SVG)
4. Add descriptive alt text for accessibility
5. Use relative paths in HTML

### Updating Content

1. Read current file first
2. Use Edit tool for precise changes
3. Preserve existing formatting and style
4. Test changes don't break layout
5. Commit with clear description of what changed

### Testing Locally

To test the site locally before pushing:
```bash
# Simple HTTP server with Python 3
python3 -m http.server 8000

# Or with Python 2
python -m SimpleHTTPServer 8000

# Then visit http://localhost:8000
```

## Repository Status

**Current Commits:**
- `c4f60d2` - create index.htm and readme
- `a6c2944` - Initial commit

**Recent Activity:**
- Repository just created
- Basic placeholder content in place
- Ready for full development

## Resources

### GitHub Pages Documentation
- [GitHub Pages Basics](https://docs.github.com/en/pages)
- [Custom Domains](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site)

### Web Development Standards
- [MDN Web Docs](https://developer.mozilla.org/)
- [HTML5 Specification](https://html.spec.whatwg.org/)
- [Web Accessibility (WCAG)](https://www.w3.org/WAI/WCAG21/quickref/)

### Tools
- `gh` CLI for GitHub operations
- Git for version control
- Standard web browsers for testing

## Questions?

When uncertain about:
- **Architecture decisions** - Ask the user for preferences
- **Design choices** - Request mockups or examples
- **Feature scope** - Clarify requirements before implementing
- **Breaking changes** - Always confirm with user first

## Version History

- **2026-01-24** - Initial CLAUDE.md creation
  - Documented repository structure
  - Established development workflows
  - Defined key conventions
  - Added AI assistant guidelines
