# Update Changelog Command

Generate consistent changelog entries based on recent changes and commits.

## Instructions

Analyze recent code changes and create properly formatted changelog entries. Follow these guidelines:

### Change Analysis

- **Review git history**: Examine recent commits since the last release or changelog update
- **Categorize changes**: Group changes by type (features, fixes, improvements, breaking changes)
- **Identify impact**: Determine user-facing vs. internal changes
- **Extract key information**: Pull out relevant details from commit messages and code changes

### Changelog Format

Use semantic changelog formatting with these categories:

- **Added**: New features and functionality
- **Changed**: Changes in existing functionality
- **Deprecated**: Features that will be removed in future versions
- **Removed**: Features removed in this version
- **Fixed**: Bug fixes and corrections
- **Security**: Security improvements and vulnerability fixes

### Entry Guidelines

- **User-focused**: Write entries from the user's perspective
- **Clear and concise**: Use simple, descriptive language
- **Actionable**: Include migration notes for breaking changes
- **Consistent format**: Follow established project conventions
- **Proper versioning**: Use semantic versioning (major.minor.patch)

### Output Requirements

1. Determine the appropriate version number based on change types
2. Generate changelog entries in the project's established format
3. Include dates and version headers
4. Add migration notes for breaking changes
5. Preserve existing changelog history

## Example Output Format

```markdown
## [1.2.0] - 2024-01-15

### Added
- New authentication middleware with JWT support
- Bulk operations API endpoint for efficient data processing

### Changed  
- Updated database schema for improved performance
- Enhanced error messages with more detailed context

### Fixed
- Resolved memory leak in background job processing
- Fixed race condition in concurrent requests

### Deprecated
- Legacy authentication method (will be removed in v2.0)
```
