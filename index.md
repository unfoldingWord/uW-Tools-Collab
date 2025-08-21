---
title: Door43 Bible Translation Resources Documentation
description: Complete documentation for understanding and building applications with Door43 Bible translation resources
---

# Door43 Bible Translation Resources: Complete Developer Documentation

Welcome to the comprehensive documentation for understanding and building applications with Door43 Bible translation resources. This documentation provides everything from the foundational concepts of the unfoldingWord ecosystem to practical API implementation guides.

## What You'll Find Here

### 🌍 Understanding the Ecosystem
Start here to understand the purpose and design of Bible translation resources:

- **[Why unfoldingWord Translation Resources](docs/why-unfoldingword-translation-resources.md)** - The mission and real-world impact
- **[unfoldingWord Developer Guide](unfoldingword-developer-guide.md)** - Complete technical specification of the resource ecosystem
- **[Resource Ecosystem Overview](PROJECT_SUMMARY.md)** - Project summary and architecture

### 🚀 Getting Started with Door43 API
Practical guides for building applications:

- **[Quick Start Guide](QUICKSTART.md)** - Get up and running in 5 minutes
- **[Door43 API Developer Guide](door43-api-developer-guide.md)** - API patterns, workflows, and application examples

### 📚 Repository Format Guides
Learn how to handle each specific type of Door43 repository:

- **[Bible Text Repositories](docs/bible-text-repositories-guide.md)** - UHB, UGNT, ULT, UST
- **[Translation Notes Repositories](docs/translation-notes-repositories-guide.md)** - TN, OBS-TN
- **[Translation Questions Repositories](docs/translation-questions-repositories-guide.md)** - TQ
- **[Translation Words Repositories](docs/translation-words-repositories-guide.md)** - TW
- **[Translation Words Links Repositories](docs/translation-words-links-repositories-guide.md)** - TWL
- **[Translation Academy Repositories](docs/translation-academy-repositories-guide.md)** - TA
- **[Open Bible Stories Repositories](docs/open-bible-stories-repositories-guide.md)** - OBS

### 🛠️ Tool-Generated Formats
Handle repositories created by translation tools:

- **[translationCore Format](docs/translationcore-format-guide.md)** - Single-book projects
- **[translationStudio Format](docs/translationstudio-format-guide.md)** - Chapter/story projects

### 🌯 Alternative Specifications
Work with different resource specifications:

- **[Scripture Burrito Repositories](docs/scripture-burrito-repositories-guide.md)** - Scripture Burrito format

### 🔄 Migration Guides
Convert Resource Container repositories to Scripture Burrito format:

- **[Migration Guide Index](docs/migration-guides/migration-guide-index.md)** - Complete migration reference
- **[Bible Text Migration](docs/migration-guides/bible-text-rc-to-sb-migration.md)** - UHB, UGNT, ULT, UST
- **[Translation Notes Migration](docs/migration-guides/translation-notes-rc-to-sb-migration.md)** - TN, OBS-TN
- **[Translation Words Migration](docs/migration-guides/translation-words-rc-to-sb-migration.md)** - TW
- **[Translation Academy Migration](docs/migration-guides/translation-academy-rc-to-sb-migration.md)** - TA

### 🤖 MCP Instructions
Automated analysis and guide generation:

- **[MCP Repository Analyzer](mcp-instructions/door43-repository-analyzer-mcp.md)** - Automated analysis instructions
- **[MCP Task Specifications](mcp-instructions/mcp-task-specifications.md)** - Specific analysis tasks
- **[MCP Implementation Example](mcp-instructions/mcp-implementation-example.md)** - Concrete examples
- **[Door43 API Reference for MCP](mcp-instructions/door43-api-reference-for-mcp.md)** - API optimization

## Key Features

### 🎯 Natural Language Instructions
All guides use conversational, step-by-step instructions that work with any programming language:

- ✅ "How to..." section headers
- ✅ Clear explanations of each step
- ✅ Implementation-agnostic guidance
- ❌ No programming language specifics
- ❌ No pseudocode or algorithms

### 🔧 Comprehensive Coverage
Every major Door43 repository type has dedicated documentation:

- **Resource Container formats** (9 types)
- **Tool-generated formats** (2 types)  
- **Alternative specifications** (1 type)
- **Migration paths** (4 specific guides)

### 🌍 Real-World Examples
All guides include examples from actual Door43 repositories:

- Live repository links and structures
- Real manifest and metadata examples
- Actual content samples and patterns
- Current API endpoints and responses

## Quick Navigation

### By Repository Name
Looking for a specific repository? Find the right guide:

| Repository Pattern | Guide | Type |
|-------------------|-------|------|
| `{lang}_ult`, `{lang}_ust` | [Bible Text](docs/bible-text-repositories-guide.md) | Gateway Translation |
| `hbo_uhb`, `el-x-koine_ugnt` | [Bible Text](docs/bible-text-repositories-guide.md) | Original Language |
| `{lang}_tn` | [Translation Notes](docs/translation-notes-repositories-guide.md) | Verse Guidance |
| `{lang}_tq` | [Translation Questions](docs/translation-questions-repositories-guide.md) | Quality Questions |
| `{lang}_tw` | [Translation Words](docs/translation-words-repositories-guide.md) | Term Definitions |
| `{lang}_twl` | [Translation Words Links](docs/translation-words-links-repositories-guide.md) | Word Cross-References |
| `{lang}_ta` | [Translation Academy](docs/translation-academy-repositories-guide.md) | Training Materials |
| `{lang}_obs` | [Open Bible Stories](docs/open-bible-stories-repositories-guide.md) | Bible Stories |

### By Use Case
What are you trying to build?

- **Preview App**: Browse published Bible resources → Start with [Complete Developer Guide](door43-api-developer-guide.md)
- **Translation Editor**: Create/edit Bible translations → See [Application Use Cases](door43-api-developer-guide.md#application-use-cases)
- **Format Conversion**: Convert RC to Scripture Burrito → See [Migration Guides](docs/migration-guides/migration-guide-index.md)
- **Repository Analysis**: Understand repository structures → See [Repository Format Guides](#repository-format-guides)

## Documentation Flow and Hierarchy

### 📖 Start with Understanding (Recommended Path)

**1. [Why unfoldingWord Translation Resources](docs/why-unfoldingword-translation-resources.md)**
- **Purpose**: Understand the mission and real-world impact
- **Audience**: Everyone - provides essential context
- **Content**: Translation challenges, ecosystem benefits, Mother Tongue Translator support

**2. [unfoldingWord Developer Guide](unfoldingword-developer-guide.md)**
- **Purpose**: Complete technical specification of the resource ecosystem
- **Audience**: Developers, technical decision makers, content creators
- **Content**: Resource architecture, alignment system, quality assurance, extensibility

**3. [Door43 API Developer Guide](door43-api-developer-guide.md)**
- **Purpose**: Practical API implementation patterns and workflows
- **Audience**: Developers building applications
- **Content**: API endpoints, authentication, CRUD operations, application examples

### 🔧 Then Choose Your Implementation Path

**For Preview Applications**: Use repository format guides to understand content structure
**For Translation Editors**: Use migration guides to convert and manage resources
**For Tool Builders**: Use MCP instructions for automated analysis and maintenance

## About This Documentation

### Comprehensive Coverage
This documentation provides **three levels of understanding**:

1. **Conceptual**: Why these resources exist and how they help translators
2. **Architectural**: How the resource ecosystem is designed and interconnected
3. **Practical**: How to build applications that use these resources

### Relationship to Official Documentation
These guides serve as a **comprehensive companion** to the [official Door43 API documentation](https://git.door43.org/api/swagger):

- **Official API Docs**: Complete endpoint reference, parameters, response schemas
- **These Guides**: Practical patterns, workflows, real-world examples, and implementation guidance

### Natural Language Approach
All implementation guides use:
- ✅ **Step-by-step instructions** that work with any programming language
- ✅ **Natural language** explanations without code specifics
- ✅ **Real examples** from actual Door43 repositories
- ✅ **Implementation-agnostic** guidance

### Maintenance and Quality
Documentation is maintained through:
- **Manual analysis** of Door43 repositories for accuracy
- **Automated validation** tools and analyzers
- **MCP-based systems** for continuous updates and pattern detection
- **Community feedback** and contributions

---

**New to Bible Translation Resources?** Start with [Why unfoldingWord Translation Resources](docs/why-unfoldingword-translation-resources.md)

**Ready to Build Applications?** Jump to [Quick Start Guide](QUICKSTART.md) or [Door43 API Developer Guide](door43-api-developer-guide.md)

**Need Deep Technical Understanding?** See [unfoldingWord Developer Guide](unfoldingword-developer-guide.md)
