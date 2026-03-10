# AI Workflow Rules for Ising Project

## Core Principles
- Complete tasks thoroughly before yielding to user
- Use parallel tool execution for independent operations
- Maintain clear context and progress tracking
- Provide accurate, fact-based responses

## Workflow Guidelines

### Task Planning & Tracking
- Use `manage_todo_list` for multi-step tasks
- Mark tasks as in-progress immediately when starting
- Mark tasks as completed immediately after finishing
- Avoid batching completions - update individually

### Code Operations
- Implement changes rather than only suggesting them
- Read large file sections in parallel when efficient
- Use `multi_replace_string_in_file` for multiple edits
- Verify changes with appropriate tools after modifications

### File Management
- Always use absolute paths for file operations
- Use proper Markdown linking for file references
- Include context before/after when replacing code (3-5 lines)
- Only create files essential to completing the request

### Search & Discovery
- Parallelize independent read-only operations
- Use semantic search for unclear patterns
- Use grep_search for specific string patterns
- Use Explore agent for complex codebase investigations

### Communication
- Keep responses brief and direct
- Avoid unnecessary introductions or conclusions
- Use proper terminology and Markdown formatting
- Link to files using workspace-relative paths

## Julia Project Specific
- Ensure .gitignore follows Julia best practices
- Document project structure in README files
- Use standard Julia project structure
- Include test directory with tests
