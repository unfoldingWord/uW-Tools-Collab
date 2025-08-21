# Door43 Bible Translation Resources Documentation

Comprehensive documentation for understanding and building applications with Door43 Bible translation resources. This documentation covers the unfoldingWord ecosystem, Door43 API integration, and all major repository formats and specifications.

## Documentation Features

- **Complete Ecosystem Coverage**: From mission understanding to practical implementation
- **Three-Level Learning Path**: Conceptual → Architectural → Practical
- **Natural Language Instructions**: Implementation-agnostic, step-by-step guidance
- **Comprehensive Repository Coverage**: All major Door43 repository types documented
- **Migration Guidance**: Complete RC to Scripture Burrito conversion instructions
- **MCP Integration**: Automated analysis and guide generation instructions
- **Professional Documentation Site**: Organized with docs.page for beautiful presentation

## Quick Start

### For New Users

**Step 1: Understand the Ecosystem**
```
Start with: Why unfoldingWord Translation Resources
Learn about: Translation challenges and ecosystem benefits
Understand: How resources work together to help translators
```

**Step 2: Learn the Architecture**
```
Read: unfoldingWord Developer Guide
Understand: Resource types, alignment system, quality assurance
Learn: Technical specifications and interconnections
```

**Step 3: Build Applications**
```
Follow: Door43 API Developer Guide
Implement: API patterns and workflows
Build: Preview apps, editing tools, or custom applications
```

### For Experienced Developers

**Jump to Implementation**:
- **[Door43 API Developer Guide](door43-api-developer-guide.md)** - API patterns and workflows
- **[Repository Format Guides](#repository-format-guides)** - Specific repository handling
- **[Migration Guides](#migration-guides)** - RC to Scripture Burrito conversion

## Documentation

### Main Guides
- **[Complete Developer Guide](door43-api-developer-guide.md)** - Step-by-step guide for Door43 API integration
- **[API Reference](#api-reference)** - Detailed method documentation
- **[Examples](#examples)** - Practical usage examples

### Repository Format Guides
- **[Bible Text Repositories](docs/bible-text-repositories-guide.md)** - UHB, UGNT, ULT, UST handling
- **[Translation Notes Repositories](docs/translation-notes-repositories-guide.md)** - TN handling
- **[Translation Questions Repositories](docs/translation-questions-repositories-guide.md)** - TQ handling
- **[Translation Words Repositories](docs/translation-words-repositories-guide.md)** - TW handling
- **[Translation Words Links Repositories](docs/translation-words-links-repositories-guide.md)** - TWL handling
- **[Translation Academy Repositories](docs/translation-academy-repositories-guide.md)** - TA handling
- **[Open Bible Stories Repositories](docs/open-bible-stories-repositories-guide.md)** - OBS, OBS-TN, OBS-TWL handling
- **[Scripture Burrito Repositories](docs/scripture-burrito-repositories-guide.md)** - Scripture Burrito format
- **[translationCore Format](docs/translationcore-format-guide.md)** - translationCore projects
- **[translationStudio Format](docs/translationstudio-format-guide.md)** - translationStudio projects

### Migration Guides
- **[Migration Guide Index](docs/migration-guides/migration-guide-index.md)** - Complete migration reference
- **[Bible Text RC to SB Migration](docs/migration-guides/bible-text-rc-to-sb-migration.md)** - Bible text conversion
- **[Translation Notes RC to SB Migration](docs/migration-guides/translation-notes-rc-to-sb-migration.md)** - Notes conversion
- **[Translation Words RC to SB Migration](docs/migration-guides/translation-words-rc-to-sb-migration.md)** - Words conversion
- **[Translation Academy RC to SB Migration](docs/migration-guides/translation-academy-rc-to-sb-migration.md)** - Academy conversion

## Documentation Organization

### Three-Level Understanding
This documentation provides **three levels of understanding**:

1. **Conceptual Level**: [Why unfoldingWord Translation Resources](docs/why-unfoldingword-translation-resources.md)
   - Mission and purpose of Bible translation resources
   - Real-world translation challenges and solutions
   - How resources work together to help Mother Tongue Translators

2. **Architectural Level**: [unfoldingWord Developer Guide](unfoldingword-developer-guide.md)
   - Complete technical specification of the resource ecosystem
   - Resource types, alignment system, quality assurance
   - Interconnections and extensibility

3. **Practical Level**: [Door43 API Developer Guide](door43-api-developer-guide.md)
   - API patterns, workflows, and application examples
   - Authentication, CRUD operations, best practices
   - Real-world application use cases

### Professional Documentation Site

**Publish with docs.page**:
```bash
# Configure docs.page to point to this repository
# Documentation automatically deploys from main branch
# Available at: https://your-domain.docs.page
```

**Features**:
- Beautiful, responsive design
- Full-text search across all guides
- Hierarchical navigation
- Cross-reference linking
- Mobile-friendly interface

## API Categories

Door43 provides two distinct categories of API endpoints:

### Catalog API (Read-Only)
- **Purpose**: Discovery of published and pre-released resources
- **HTTP Methods**: GET only
- **Use Cases**: Preview apps, resource discovery, language statistics
- **Target Resources**: Published resources following supported specifications
- **Authentication**: Optional (higher rate limits with token)

### Gitea API (Full CRUD)
- **Purpose**: Complete repository and content management
- **HTTP Methods**: GET, POST, PUT, PATCH, DELETE
- **Use Cases**: Content management, authoring tools, repository administration
- **Target Resources**: All repositories (published, draft, private)
- **Authentication**: Required for write operations

## API Reference

### Door43Client

Main client class for interacting with Door43 API.

#### Constructor

```javascript
const client = new Door43Client(options);
```

**Options:**
- `baseUrl` - Base URL for Door43 (default: 'https://git.door43.org')
- `token` - API token for authentication (optional)
- `cacheTTL` - Cache time-to-live in milliseconds (default: 3600000)
- `requestsPerHour` - Rate limit (default: 60)

#### Discovery Methods

**Catalog API (Published Resources Only):**
```javascript
// Discover published resources by language
const resources = await client.discoverByLanguage('en', 'prod');

// Discover published resources by subject
const bibles = await client.discoverBySubject('Bible', 'prod');

// Get language statistics
const languageStats = await client.getLanguageStatistics();
```

**Gitea API (All Repositories):**
```javascript
// Discover all repositories by organization
const repos = await client.discoverByOrganization('unfoldingWord');

// Search repositories
const searchResults = await client.searchRepositories('ult');

// Get user repositories
const userRepos = await client.getUserRepositories('username');

// Get repository information
const repoInfo = await client.getRepositoryInfo('unfoldingWord', 'en_ult');
```

#### Specification Detection

```javascript
// Detect resource specification type
const spec = await client.detectSpecification('unfoldingWord', 'en_ult');
console.log(spec.type); // 'Resource Container', 'Scripture Burrito', or 'TCore Resource Container'
```

#### Processing Methods

```javascript
// Complete repository processing
const result = await client.discoverAndProcessRepository('unfoldingWord', 'en_ult');

// Process organization resources
const results = await client.processOrganizationResources('unfoldingWord', {
    language: 'en',
    resourceType: 'ult'
});
```

#### CRUD Methods (Requires Authentication)

```javascript
// Create repository
const repo = await client.createRepository({
    name: 'my-resource',
    description: 'My Bible resource',
    private: false
});

// Update repository
await client.updateRepository('owner', 'repo', {
    description: 'Updated description'
});

// Create or update file
await client.createOrUpdateFile('owner', 'repo', 'manifest.yaml', content, 'Add manifest');

// Delete file
await client.deleteFile('owner', 'repo', 'file.txt', 'Remove file', sha);

// Delete repository
await client.deleteRepository('owner', 'repo');
```

#### Download Methods

```javascript
// Download single file
await client.downloadResource('unfoldingWord', 'en_ult', 'manifest.yaml', './manifest.yaml');

// Download selected resources
const downloads = await client.downloadSelectedResources(
    'unfoldingWord', 
    'en_ult', 
    resourceList, 
    './downloads'
);

// Download repository archive
const archiveBuffer = await client.downloadRepositoryArchive('unfoldingWord', 'en_ult');
```

## Supported Specifications

### Resource Container (RC)

- **Detection**: `manifest.yaml` with `dublin_core.conformsto` field
- **Structure**: Flat USFM files, TSV data files, nested Markdown articles
- **Examples**: unfoldingWord English resources (`en_ult`, `en_ust`, `en_tn`, etc.)

### Scripture Burrito (SB)

- **Detection**: `metadata.json` with `meta.format: 'scripture burrito'`
- **Structure**: Ingredients-based file organization
- **Examples**: Various Scripture Burrito compliant repositories

### TCore Resource Container

- **Detection**: `manifest.json` with `resource_container` section
- **Structure**: Content-based organization
- **Examples**: TCore-specific implementations

## Rate Limiting

The client includes built-in rate limiting:

- **Anonymous**: 60 requests/hour
- **Authenticated**: 1000+ requests/hour (requires API token)

```javascript
const client = new Door43Client({
    token: 'your-api-token',
    requestsPerHour: 1000
});
```

## Caching

Intelligent caching reduces API calls:

- **Catalog responses**: Cached for 1 hour by default
- **Repository metadata**: Cached with TTL
- **File content**: Not cached (downloaded fresh each time)

```javascript
const client = new Door43Client({
    cacheTTL: 1800000 // 30 minutes
});
```

## Error Handling

The client includes robust error handling:

- **Automatic retries** with exponential backoff
- **Rate limit handling** with automatic waiting
- **Network error recovery**
- **Graceful degradation** for missing resources

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Run tests: `npm test`
5. Submit a pull request

## License

MIT License - see LICENSE file for details.

## Related Resources

- **[Door43 Content Service](https://git.door43.org/)** - Main platform
- **[unfoldingWord](https://unfoldingword.org/)** - Organization behind the resources
- **[Resource Container Specification](https://resource-container.readthedocs.io/)** - RC format documentation
- **[USFM Specification](https://docs.usfm.bible/)** - Bible markup format
- **[Scripture Burrito](https://docs.burrito.bible/)** - Alternative resource format