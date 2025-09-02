# Firebender Command Cookbooks

Ready-to-use command configurations for common development workflows. Copy the `firebender.json` and command files to
your project to get started quickly.

## Available Commands

### 1. Quick Question

- **Purpose**: Get rapid answers to development questions
- **Model**: `fast` - Optimized for speed
- **Mode**: `read` - Analysis and explanation only
- **Use Case**: Quick clarifications, explanations, and guidance

### 2. Review Pull Request

- **Purpose**: Structured code reviews with consistent feedback
- **Model**: `claude-3.5-sonnet` - Balanced speed and quality
- **Mode**: `read` - Code analysis and review
- **Use Case**: Comprehensive PR reviews, security checks, best practices

### 3. Update Changelog

- **Purpose**: Generate consistent changelog entries from git history
- **Model**: `gpt-4.1` - Advanced reasoning for categorization
- **Mode**: `write` - File modifications and git operations
- **Use Case**: Release preparation, documentation updates

### 4. Create Design Document

- **Purpose**: Generate technical design documents for features
- **Model**: `claude-sonnet-4-20250514` - Best general purpose model
- **Mode**: `write` - Document creation and collaboration
- **Use Case**: Feature planning, system architecture, project documentation

## Setup

1. Copy `firebender.json` to your project root
2. Copy the command directories you want to use
3. Modify paths in `firebender.json` if needed
4. Customize command files to match your project's specific needs

## Customization

Each command file can be customized for your specific workflow:

- Modify the instructions to match your coding standards
- Adjust the model selection based on your performance needs
- Change the mode based on whether you need read-only analysis or write operations
- Add project-specific context and requirements

## Usage

Once configured, access commands in Firebender chat by typing `/` followed by the command name:

- `/quick question`
- `/review pr`
- `/update changelog`
- `/create design doc`

## Model Recommendations

- **fast**: Quick responses, basic tasks
- **claude-3.5-sonnet**: Balanced performance for most tasks
- **gpt-4.1**: Complex reasoning and analysis
- **claude-sonnet-4-20250514**: Best overall capability
