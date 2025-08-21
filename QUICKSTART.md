---
title: Quick Start Guide
description: Get up and running with Door43 resources in 5 minutes
---

# Quick Start Guide

Get up and running with the Door43 API Client in 5 minutes!

## 🚀 Getting Started

```bash
# 1. Clone or browse this documentation
git clone <repository-url>
cd door43-bible-translation-docs

# 2. Start with understanding the ecosystem
# Read: docs/why-unfoldingword-translation-resources.md

# 3. Learn the technical architecture  
# Read: unfoldingword-developer-guide.md

# 4. Build applications
# Follow: door43-api-developer-guide.md
```

## 🎯 Documentation Paths

### Understand the Mission

**[Why unfoldingWord Translation Resources](docs/why-unfoldingword-translation-resources.md)**
- Learn about Mother Tongue Translators and their challenges
- Understand how the resource ecosystem helps overcome translation barriers
- See real-world scenarios showing resource benefits

### Learn the Architecture

**[unfoldingWord Developer Guide](unfoldingword-developer-guide.md)**
- Complete technical specification of the resource ecosystem
- Resource types, alignment system, quality assurance
- Interconnections and extensibility frameworks

### Build Applications

**[Door43 API Developer Guide](door43-api-developer-guide.md)**
- API authentication and endpoint usage
- Repository discovery and content access
- CRUD operations and application examples

## 🧪 Explore Specific Repository Types

### Bible Text Repositories
- **UHB, UGNT**: Original language texts
- **ULT, UST**: Gateway language translations with alignment
- **Processing**: USFM format, word alignment, large file handling

### Translation Support Repositories
- **TN**: Verse-specific translation guidance
- **TQ**: Quality assurance questions
- **TW**: Biblical term definitions
- **TWL**: Word-to-definition cross-references
- **TA**: Translation methodology training

## 📝 Documentation Usage

### Reading Path for Different Goals

**Building a Preview App**:
1. Read [Door43 API Developer Guide](door43-api-developer-guide.md) - API patterns
2. Use [Bible Text Repositories Guide](docs/bible-text-repositories-guide.md) - Handle Bible content
3. Add [Translation Notes Guide](docs/translation-notes-repositories-guide.md) - Show verse guidance

**Building a Translation Editor**:
1. Start with [Application Use Cases](door43-api-developer-guide.md#application-use-cases)
2. Use repository-specific guides for content handling
3. Follow [Migration Guides](docs/migration-guides/migration-guide-index.md) for format conversion

**Understanding the Ecosystem**:
1. Begin with [Why unfoldingWord Translation Resources](docs/why-unfoldingword-translation-resources.md)
2. Study [unfoldingWord Developer Guide](unfoldingword-developer-guide.md)
3. Explore specific repository format guides as needed

## 🔧 Implementation Guidance

### API Authentication
- Use Door43 API tokens for higher rate limits (1000+ vs 60 requests/hour)
- Follow authentication patterns in [Door43 API Developer Guide](door43-api-developer-guide.md)
- Implement secure token storage and management

### Performance Optimization
- Cache catalog responses (change infrequently)
- Use raw URLs for large content files
- Implement rate limiting respect
- Use diff patches for large file updates

## 📚 What You Can Do

### Resource Discovery
- Find resources by language (`en`, `es-419`, `fr`, etc.)
- Find resources by subject (`Bible`, `Translation Notes`, etc.)
- Browse organization repositories (`unfoldingWord`, `es-419_gl`, etc.)

### Specification Support
- **Resource Container (RC)** - unfoldingWord standard format
- **Scripture Burrito (SB)** - Alternative Bible resource format
- **TCore Resource Container** - Legacy format support

### Download Options
- Individual files (manifests, specific books)
- Selected resources (choose which books to download)
- Complete repository archives (ZIP format)

### Processing Features
- Automatic specification detection
- Resource relationship mapping
- Metadata extraction
- Cross-reference validation

## 🗂️ File Structure

```
door43-api-client/
├── src/
│   └── door43-client.js          # Main client class
├── test/
│   ├── test-discovery.js         # Discovery tests
│   ├── test-spec-detection.js    # Specification tests
│   ├── test-download.js          # Download tests
│   └── test-runner.js            # Test runner
├── examples/
│   ├── download-english-ult.js   # Download example
│   ├── find-spanish-resources.js # Discovery example
│   ├── process-organization.js   # Processing example
│   └── crud-operations.js        # CRUD operations example
├── tools/
│   └── analyze-translationcore-repo.js # Repository analyzer
├── docs/
│   └── translationcore-format-guide.md # translationCore format guide
├── door43-api-developer-guide.md # Main developer guide
├── README.md                     # API reference
└── QUICKSTART.md                 # This file
```

## 🔍 Common Use Cases

### Download Complete Bible Translation

```bash
node examples/download-english-ult.js all
```

### Download Only New Testament

```bash
node examples/download-english-ult.js nt
```

### Find Resources in Specific Language

```bash
node examples/process-organization.js es-419_gl glt
```

### Get Translation Notes

```bash
node examples/process-organization.js unfoldingWord tn
```

### Analyze translationCore Repository

```bash
npm run analyze:tc
```

### Analyze translationStudio Repositories

```bash
npm run analyze:ts
```

### Analyze Resource Subjects (Comprehensive)

```bash
npm run analyze:subjects
```

## ❓ Troubleshooting

### "Cannot find module" Error
```bash
npm install  # Make sure dependencies are installed
```

### API Connection Issues
```bash
node test-api-live.js  # Test connectivity
```

### Rate Limit Exceeded
- Wait an hour for limits to reset
- Or get an API token for higher limits

### No Resources Found
- Check spelling of organization/repository names
- Verify the resource exists at https://git.door43.org/

## 📖 Next Steps

1. **Read the Full Guide**: [door43-api-developer-guide.md](door43-api-developer-guide.md)
2. **Explore Examples**: Try different parameters with the example scripts
3. **Build Your Own**: Use the client in your own projects
4. **Contribute**: Add new features or fix bugs

## 🆘 Getting Help

- Check the [Complete API Guide](door43-api-access-guide.md)
- Review the [README](README.md) for API reference
- Look at the example files for usage patterns
- Test with `npm run test:live` to verify setup

Happy coding! 🎉
