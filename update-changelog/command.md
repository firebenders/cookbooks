# Update Changelog Command

Generate consistent changelog entries based on commits since the last release.

## Instructions

Follow this systematic approach to update the changelog:

### Step 1: Find Last Release Commit

- **Search for release tags**: Use `git tag --sort=-version:refname` to find the most recent release tag
- **Identify release commit**: Use `git log --oneline --grep="release\|bump\|version"` to find release commits
- **Fallback to changelog**: If no clear release commit, examine the existing CHANGELOG.md to determine the last
  documented release date and find the corresponding commit

### Step 2: Analyze Changes Since Last Release

- **Get commit range**: Use `git log <last-release-commit>..HEAD --oneline` to see all commits since the last release
- **Review detailed changes**: Use `git log <last-release-commit>..HEAD --pretty=format:"%h %s%n%b"` for full commit
  messages
- **Examine file changes**: Use `git diff <last-release-commit>..HEAD --name-only` to see which files were modified
- **Categorize commits**: Group changes by type (features, fixes, improvements, breaking changes)

### Step 3: Reference Existing Changelog Style

- **Read current CHANGELOG.md**: Study the last 2-3 entries to understand:
    - Entry length and level of detail
    - Writing style and tone
    - Technical depth vs. user-friendly language
    - How similar changes were previously described
- **Match established patterns**: Follow the same format, terminology, and level of detail
- **Maintain consistency**: Use similar phrasing for similar types of changes

### Step 4: Generate User-Focused Entries

Follow the project's changelog format with these categories:

- **Added**: New features and functionality
- **Changed**: Changes in existing functionality
- **Deprecated**: Features that will be removed in future versions
- **Removed**: Features removed in this version
- **Fixed**: Bug fixes and corrections
- **Security**: Security improvements and vulnerability fixes

### Entry Guidelines

- **User-focused**: Write from the user's perspective, not developer's
- **Concise but informative**: Match the brevity style of existing entries
- **Skip internal changes**: Omit refactoring, test updates, and other non-user-facing changes unless they impact
  performance or behavior
- **Group related changes**: Combine similar commits into single, coherent entries
- **Use active voice**: "Added new feature" not "New feature was added"

### Step 5: Version and Format Output

1. **Determine version bump**:
    - Major: Breaking changes
    - Minor: New features (backward compatible)
    - Patch: Bug fixes only
2. **Use project's date format**: Follow existing changelog date formatting
3. **Maintain structure**: Keep the same heading levels and markdown formatting
4. **Position correctly**: Add new entry at the top, below any "Unreleased" section

## Example Workflow Commands

```bash
# Find the last release tag
git tag --sort=-version:refname | head -5

# Get commits since last release
git log v1.2.0..HEAD --oneline

# See detailed commit messages
git log v1.2.0..HEAD --pretty=format:"%h %s%n%b%n"

# Check what files changed
git diff v1.2.0..HEAD --name-only
```

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

