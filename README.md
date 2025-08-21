# Door43 Developer Documentation

> **Build applications with Door43 Bible translation resources**  
> Comprehensive guides for APIs, formats, and implementation patterns

[![Documentation](https://img.shields.io/badge/docs-docs.page-blue)](https://docs.page/unfoldingWord-dev/uW-Tools-Collab)
[![License](https://img.shields.io/badge/license-MIT-green)](LICENSE)
[![GitHub Issues](https://img.shields.io/github/issues/unfoldingWord-dev/uW-Tools-Collab)](https://github.com/unfoldingWord-dev/uW-Tools-Collab/issues)

## 🚀 **Quick Start**

### **Building a Bible Reading App?**
```
1. Read: Why unfoldingWord Resources → Understand the ecosystem
2. Implement: Door43 API Guide → Get data from repositories  
3. Handle: Bible Text Format Guide → Display USFM content
4. Add: Translation Notes Guide → Show verse-level helps
```
**Time: ~4 hours** | **Difficulty: ⭐⭐ Intermediate**

### **Creating a Translation Editor?**
```
1. Study: unfoldingWord Developer Guide → Learn resource architecture
2. Implement: Door43 API Guide → CRUD operations for content
3. Handle: All Repository Formats → Support multiple resource types
4. Add: Migration Guides → Convert between formats
```
**Time: ~2-3 days** | **Difficulty: ⭐⭐⭐ Advanced**

## 📚 **What's Inside**

This repository contains comprehensive developer documentation for the Door43 ecosystem:

### **[Getting Started](docs/getting-started/)**
- **Why unfoldingWord Translation Resources** - Mission and ecosystem overview
- Foundation concepts for Bible translation technology

### **[Developer Guides](docs/guides/)**
- **unfoldingWord Developer Guide** - Complete resource architecture
- **Door43 API Developer Guide** - Practical API implementation patterns

### **[Repository Formats](docs/repository-formats/)**
- **Resource Container** - Standard unfoldingWord formats (Bible texts, translation helps)
- **Scripture Burrito** - Alternative Bible resource format  
- **Tool-Generated** - translationCore and translationStudio formats

### **[Migration & Conversion](docs/migration/)**
- Resource Container → Scripture Burrito conversion guides
- Format-specific migration instructions

### **[Automation & MCP](docs/automation/)**
- MCP instructions for AI systems
- Batch processing and repository analysis tools

## 🎯 **Find What You Need**

| Resource Type | What It Contains | Format Guide |
|---------------|------------------|--------------|
| **Bible Texts** | USFM Scripture (UHB, UGNT, ULT, UST) | [Bible Text Guide](docs/repository-formats/resource-container/bible-text-repositories-guide.mdx) |
| **Translation Notes** | Verse-level translation guidance | [Translation Notes Guide](docs/repository-formats/resource-container/translation-notes-repositories-guide.mdx) |
| **Translation Words** | Biblical term definitions | [Translation Words Guide](docs/repository-formats/resource-container/translation-words-repositories-guide.mdx) |
| **Translation Questions** | Quality assurance questions | [Translation Questions Guide](docs/repository-formats/resource-container/translation-questions-repositories-guide.mdx) |
| **Translation Academy** | Translation methodology training | [Translation Academy Guide](docs/repository-formats/resource-container/translation-academy-repositories-guide.mdx) |
| **Open Bible Stories** | 50 key Bible stories | [Open Bible Stories Guide](docs/repository-formats/resource-container/open-bible-stories-repositories-guide.mdx) |

## 🛠️ **For Developers**

### **Common Implementation Patterns**

**Basic Resource Access:**
```
1. Authenticate with Door43 API
2. Discover repositories by language/organization
3. Detect resource specification (RC/SB/Tool)
4. Process content according to format guide
```

**Multi-Resource Applications:**
```
1. Load Bible text as primary content
2. Overlay translation notes for verse guidance
3. Link translation words for term definitions
4. Add translation questions for quality checks
```

### **API Resources**
- **[Door43 Content Service](https://git.door43.org/)** - Live repository browser
- **[Door43 API Swagger](https://git.door43.org/api/swagger)** - Complete API reference
- **[Resource Container Spec](https://resource-container.readthedocs.io/)** - Official RC specification

## 📖 **Documentation Site**

This repository powers a beautiful documentation site built with [docs.page](https://docs.page/):

**🌐 [View Live Documentation](https://docs.page/unfoldingWord-dev/uW-Tools-Collab)**

### **Features:**
- 🔍 **Full-text search** across all guides
- 📱 **Mobile-responsive** design
- 🌙 **Dark/light theme** support
- 🔗 **Cross-referenced** content
- ⚡ **Fast loading** with optimized delivery

## 🤝 **Contributing**

We welcome contributions to improve the documentation!

### **How to Contribute:**

1. **Fork** this repository
2. **Create** a feature branch (`git checkout -b improve-docs`)
3. **Make** your changes following our [style guidelines](docs/assets/frontmatter-schema.md)
4. **Test** your changes locally with docs.page preview
5. **Submit** a pull request

### **Documentation Standards:**
- Use **natural language** instructions (implementation-agnostic)
- Include **real examples** from actual Door43 repositories
- Follow the **frontmatter schema** for metadata
- Add **cross-references** to related guides
- Test all **internal links**

### **Content Guidelines:**
- ✅ Step-by-step instructions that work with any programming language
- ✅ Clear explanations with real-world examples
- ✅ Proper frontmatter with categories and tags
- ❌ Programming language-specific code examples
- ❌ Pseudocode or algorithms

## 🏗️ **Repository Structure**

```
docs/
├── index.mdx                    # Main documentation index
├── getting-started/             # Introduction and concepts
├── guides/                      # Core technical guides
├── repository-formats/          # Format-specific documentation
│   ├── resource-container/      # RC specification guides
│   ├── scripture-burrito/       # SB specification guides
│   └── tool-generated/          # Tool-specific formats
├── migration/                   # Format conversion guides
├── automation/                  # MCP and automation tools
├── reference/                   # Templates and reference materials
└── assets/                      # Icons, schemas, and resources
```

## 📊 **Documentation Stats**

- **📄 29 guides** covering all major Door43 repository types
- **🔧 3 specifications** (Resource Container, Scripture Burrito, Tool-Generated)
- **🔄 6 migration guides** for format conversion
- **🤖 4 automation tools** for MCP systems
- **📋 Comprehensive cross-references** between all guides

## 🆘 **Getting Help**

- **📖 Browse the docs**: [docs.page/unfoldingWord-dev/uW-Tools-Collab](https://docs.page/unfoldingWord-dev/uW-Tools-Collab)
- **🐛 Report issues**: [GitHub Issues](https://github.com/unfoldingWord-dev/uW-Tools-Collab/issues)
- **💬 Ask questions**: [GitHub Discussions](https://github.com/unfoldingWord-dev/uW-Tools-Collab/discussions)
- **🔗 Official API docs**: [git.door43.org/api/swagger](https://git.door43.org/api/swagger)

## 📄 **License**

This documentation is licensed under the [MIT License](LICENSE).

## 🌍 **About unfoldingWord & Open Components**

This documentation supports the [unfoldingWord](https://unfoldingword.org/) mission to provide unrestricted biblical content in every language. The Door43 platform hosts comprehensive Bible translation resources that help Mother Tongue Translators create Scripture translations in their heart languages.

These resources are designed for the [Open Components Ecosystem](https://opencomponents.io/) community, enabling developers to build interoperable Bible translation applications with shared, reusable components.

---

**Ready to build?** Start with the [Door43 API Developer Guide](docs/guides/door43-api-developer-guide.mdx) for practical implementation patterns.