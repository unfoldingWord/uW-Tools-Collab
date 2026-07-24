# Door43 Developer Documentation

> **Build applications with Door43 Bible translation resources**  
> Guides for APIs, formats, and implementation patterns

[![Documentation](https://img.shields.io/badge/docs-docs.page-blue)](https://docs.page/unfoldingWord/uW-Tools-Collab)
[![License](https://img.shields.io/badge/license-MIT-green)](LICENSE)
[![GitHub Issues](https://img.shields.io/github/issues/unfoldingWord/uW-Tools-Collab)](https://github.com/unfoldingWord/uW-Tools-Collab/issues)

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

This repository contains developer documentation for the Door43 ecosystem:

### **[Getting Started](docs/)**
- **[Why unfoldingWord Translation Resources](docs/1-why-unfoldingword-translation-resources.mdx)** - Mission and ecosystem overview
- **[Getting Started Guide](docs/0-getting-started.mdx)** - Foundation concepts for Bible translation technology

### **[Developer Guides](docs/)**
- **[unfoldingWord Developer Guide](docs/2-unfoldingword-developer-guide.mdx)** - Complete resource architecture
- **[Door43 API Developer Guide](docs/3-door43-api-developer-guide.mdx)** - Practical API implementation patterns

### **[Repository Formats](docs/4-repository-formats/)**
- **[Resource Container](docs/4-repository-formats/resource-container/)** - Standard unfoldingWord formats (Bible texts, translation helps)
- **[Scripture Burrito](docs/4-repository-formats/scripture-burrito/)** - Alternative Bible resource format  
- **[Tool-Generated](docs/4-repository-formats/tool-generated/)** - translationCore and translationStudio formats

### **[Migration & Conversion](docs/5-migration/)**
- **[Resource Container → Scripture Burrito](docs/5-migration/rc-to-sb/)** conversion guides
- **[Format-specific migration instructions](docs/5-migration/migration-guide-index.mdx)**

### **[Automation & MCP](docs/automation/)**
- **[MCP instructions for AI systems](docs/automation/mcp-implementation-example.mdx)**
- **[Batch processing and repository analysis tools](docs/automation/door43-repository-analyzer-mcp.mdx)**

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

## 🤖 **For AI Developers & Automation**

Do you build AI tools or automated systems? See our AI developer guide:

**📋 [AI Developer Guide](AI_DEVELOPER_GUIDE.md)** - Complete roadmap for AI systems, MCP implementations, and automated tools

## 📖 **Documentation Site**

This repository powers a documentation site built with [docs.page](https://docs.page/):

**🌐 [View Live Documentation](https://docs.page/unfoldingWord/uW-Tools-Collab)**

### **Features:**
- 🔍 **Full-text search** across all guides
- 📱 **Mobile-responsive** design
- 🌙 **Dark/light theme** support
- 🔗 **Cross-referenced** content
- ⚡ **Fast loading** with optimized delivery

## 🤝 **Contributing**

We welcome contributions that improve the documentation.

### **How to Contribute:**

1. **Fork** this repository
2. **Create** a feature branch (`git checkout -b improve-docs`)
3. **Make** your changes. Follow our [style guidelines](docs/assets/frontmatter-schema.md)
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
├── index.mdx                           # Main documentation index
├── 0-getting-started.mdx               # Introduction and learning paths
├── 1-why-unfoldingword-translation-resources.mdx  # Mission and ecosystem
├── 2-unfoldingword-developer-guide.mdx # Complete technical specification
├── 3-door43-api-developer-guide.mdx    # Practical API implementation
├── 4-repository-formats/               # Format-specific documentation
│   ├── resource-container/             # RC specification guides
│   ├── scripture-burrito/              # SB specification guides
│   └── tool-generated/                 # Tool-specific formats
├── 5-migration/                        # Format conversion guides
├── automation/                         # MCP and automation tools
└── assets/                             # Icons, schemas, and resources
AI_DEVELOPER_GUIDE.md                   # AI systems implementation guide
```

## 📊 **Documentation Stats**

- **📄 29 guides** covering all major Door43 repository types
- **🔧 3 specifications** (Resource Container, Scripture Burrito, Tool-Generated)
- **🔄 6 migration guides** for format conversion
- **🤖 4 automation tools** for MCP systems
- **📋 Cross-references** between all guides

## 🆘 **Getting Help**

- **📖 Browse the docs**: [docs.page/unfoldingWord/uW-Tools-Collab](https://docs.page/unfoldingWord/uW-Tools-Collab)
- **🐛 Report issues**: [GitHub Issues](https://github.com/unfoldingWord/uW-Tools-Collab/issues)
- **💬 Ask questions**: [GitHub Discussions](https://github.com/unfoldingWord/uW-Tools-Collab/discussions)
- **🔗 Official API docs**: [git.door43.org/api/swagger](https://git.door43.org/api/swagger)

## 📄 **License**

This documentation is licensed under the [MIT License](LICENSE).

## 🌍 **About unfoldingWord & Open Components**

This documentation supports the [unfoldingWord](https://unfoldingword.org/) mission. The mission provides unrestricted biblical content in every language. The Door43 platform hosts Bible translation resources. These resources help Mother Tongue Translators create Scripture translations in their heart languages.

These resources are designed for the [Open Components Ecosystem](https://opencomponents.io/) community. They let developers build interoperable Bible translation applications with shared, reusable components.

---

**Ready to build?**
- **Human developers**: Start with the [Door43 API Developer Guide](docs/3-door43-api-developer-guide.mdx) for practical implementation patterns
- **AI systems**: Begin with the [AI Developer Guide](AI_DEVELOPER_GUIDE.md) for automation guidance
