# Assets Directory

This directory contains local assets for the docs.page documentation site.

## Required Icons

To complete the icon setup, add the following files to this directory:

### Main Logo & Favicon
- `logo-light.png` - Logo for light theme (recommended: 120-200px height)
- `logo-dark.png` - Logo for dark theme (recommended: 120-200px height)  
- `favicon.ico` - Browser favicon (16x16, 32x32, 48x48 pixels)

### Navigation Icons (SVG format recommended)
Place these in the `icons/` subdirectory:

- `getting-started.svg` - Icon for "Getting Started" section
- `developer-guide.svg` - Icon for "Developer Guides" section
- `repository.svg` - Icon for "Repository Formats" section
- `migration.svg` - Icon for "Migration & Conversion" section
- `automation.svg` - Icon for "Automation & MCP" section
- `reference.svg` - Icon for "Reference" section

## Icon Guidelines

### Size Recommendations
- **Favicon**: 16x16, 32x32, 48x48 pixels
- **Logo**: 120-200px height, maintain aspect ratio
- **Navigation Icons**: 16x16 or 24x24 pixels

### Format Guidelines
- **SVG**: Best for icons (scalable, crisp)
- **PNG**: Good for logos with gradients/complex graphics
- **ICO**: Traditional favicon format

### Naming Convention
- Use kebab-case (lowercase with hyphens)
- Be descriptive and consistent
- Include theme suffix for logos (`-light`, `-dark`)

## Usage

Icons are referenced in `docs.json` using relative paths from the `docs/` directory:

```json
{
  "logo": {
    "light": "/assets/logo-light.png",
    "dark": "/assets/logo-dark.png"
  },
  "favicon": "/assets/favicon.ico"
}
```

For navigation icons:
```json
{
  "title": "Getting Started",
  "icon": "/assets/icons/getting-started.svg"
}
```
