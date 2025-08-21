# Frontmatter Schema for Documentation

## Standard Frontmatter Template

```yaml
---
title: "Page Title"
description: "Brief description for SEO and navigation"
category: "getting-started|guides|repository-formats|migration|automation|reference"
specification: "resource-container|scripture-burrito|tool-generated|general"
difficulty: "beginner|intermediate|advanced"
related:
  - path: "/path/to/related-guide"
    title: "Related Guide Title"
    description: "Why this is related"
  - path: "/path/to/another-guide" 
    title: "Another Guide"
    description: "Another relationship"
prerequisites:
  - path: "/path/to/prerequisite"
    title: "Prerequisite Guide"
  - path: "/path/to/another-prereq"
    title: "Another Prerequisite"
next_steps:
  - path: "/path/to/next-step"
    title: "Next Step Guide"
  - path: "/path/to/advanced-topic"
    title: "Advanced Topic"
tags: ["api", "resource-container", "bible-text", "usfm"]
last_updated: "2024-01-20"
---
```

## Field Descriptions

- **title**: Page title (required)
- **description**: Brief description for SEO and cards (required)
- **category**: Main section category (required)
- **specification**: Which spec this applies to (optional)
- **difficulty**: Complexity level (optional)
- **related**: Related guides with context (optional)
- **prerequisites**: Required reading before this guide (optional)
- **next_steps**: Logical next guides to read (optional)
- **tags**: Searchable keywords (optional)
- **last_updated**: Last modification date (optional)
