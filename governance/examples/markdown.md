# Markdown Standards

This document provides guidelines for using Markdown in Norwegian Red Cross GitHub repositories.

## Text Formatting

- Use Markdown formatting consistently
- Prefer ATX-style headers (`#` syntax) over underline-style
- Use backticks for inline code and code blocks with language specification
- Use bold for emphasis or important information
- Use bullet lists for unordered items and numbered lists for sequences

### Examples

#### Headers

```markdown
# Level 1 Header (Document Title)
## Level 2 Header (Major Section)
### Level 3 Header (Subsection)
#### Level 4 Header (Minor Subsection)
```

#### Code Formatting

Inline code: `const example = "This is inline code";`

Code block with language specification:

```javascript
function example() {
  const greeting = "Hello World";
  console.log(greeting);
  return greeting;
}
```

#### Emphasis

- **Bold text** for important information (`**Bold text**`)
- *Italic text* for emphasis (`*Italic text*`)
- ~~Strikethrough~~ for deprecated items (`~~Strikethrough~~`)

#### Lists

Unordered list:
```markdown
- Item 1
- Item 2
  - Nested item 2.1
  - Nested item 2.2
- Item 3
```

Numbered list:
```markdown
1. First step
2. Second step
   1. Substep 2.1
   2. Substep 2.2
3. Third step
```

## Documentation Structure

- Organize documentation with clear hierarchical headings
- Use a logical progression from general to specific information
- Include a table of contents for longer documents (>1000 words)
- Keep line length reasonable (typically <120 characters)

### Example Table of Contents

```markdown
## Table of Contents
- [Introduction](#introduction)
- [Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
- [Usage](#usage)
- [Advanced Features](#advanced-features)
- [Troubleshooting](#troubleshooting)
- [FAQ](#faq)
```

## Tables

Use tables to present structured data:

```markdown
| Name | Type | Description | Default |
|------|------|-------------|---------|
| id | string | Unique identifier | N/A |
| enabled | boolean | Whether feature is enabled | false |
| count | number | Number of items | 0 |
```

## Links

Use descriptive link text:

```markdown
[Norwegian Red Cross GitHub Standards](https://github.com/norwegianredcross/governance)
```

For internal document references:

```markdown
See the [Installation Guide](./docs/installation.md) for setup instructions.
```

## Images

Include alt text for all images:

```markdown
![Norwegian Red Cross Logo](./images/logo.png "Norwegian Red Cross Logo")
```