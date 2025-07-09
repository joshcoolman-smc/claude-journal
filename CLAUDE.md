# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a personal writing and notes repository focused on capturing thoughts about AI, technology, and productivity. The project uses a minimalist approach with no dependencies or complex tooling.

## Project Structure

- **Markdown Files**: Primary content consists of timestamped journal entries and essays
  - `README.md`: Main journal with dated entries about AI, creativity, and technology
  - `archive.md`: Stream-of-consciousness notes about note-taking systems
  - `my-first-post.md`: Essay on productivity systems and personal knowledge management

## Development Commands

Currently, no build, test, or lint commands are configured. The project intentionally avoids complex tooling in line with the author's philosophy of simple text capture.

## Special Instructions

### "Capture This" Command
When the user says "capture this", "save that", "add this to the README" or similar:
1. Read README.md and find the first dated entry (pattern like "Monday, January 1, 2025")
2. Extract ALL text above that first dated entry as the staging area content
3. If no dated entries exist, treat the entire document as staging area
4. Process the staging area content:
   - Perform a light editorial pass to fix spelling, punctuation, and odd sentence construction
   - Get the current date/time using bash command `date`
   - Create a descriptive title that captures the essence of the content
   - Format as a proper journal entry following the existing pattern:
     - Add timestamp header (e.g., "Sunday, June 22, 2025 at 08:00 AM")
     - Add a blank line
     - Add "## [Descriptive Title]"
     - Add a blank line
     - Add the edited content
     - Add a blank line
     - Create bullet point summaries of key points
     - Add a blank line
     - Add "---" separator
     - Add a blank line before the previous entry
5. Replace the staging area with the formatted entry (preserving any blank lines at the very top)
6. Git commit with a descriptive message and push after each capture

### "New Document" Command
When the user says "save as a new document", "save this as a new document", or similar phrases containing "new document":
1. Create a new markdown file separate from the README.md journal
2. If filename not provided, suggest a descriptive name based on the content
3. Format the content as a standalone document (not as a journal entry):
   - Include appropriate title and headers
   - Structure content with clear sections
   - Apply proper markdown formatting
4. Save the file in the project directory
5. Git commit with a descriptive message and push

**Key distinction:**
- "Capture this" → Adds timestamped entry to README.md
- "New document" → Creates separate .md file with compiled/researched content

### "Blog Post" Command
When the user asks to "write a blog post" or similar (THIS IS SEPARATE FROM README.md UPDATES):
1. Create a new standalone markdown file in the root directory (NOT the README.md)
2. This format is specifically for blog posts, not for journal entries or README updates
3. If providing content directly or writing to a file, use the following frontmatter format:
```markdown
---
title: "Your Post Title"
date: "2024-01-15"
description: "A brief description of your post"
tags: ["tag1", "tag2", "tag3"]
published: true
---

Your content goes here in markdown format.

## Headers work as expected

Regular paragraphs with **bold** and *italic* text.

- Bullet points
- Work great

1. Numbered lists
2. Also supported

> Blockquotes for emphasis

```javascript
// Code blocks with syntax highlighting
const example = "Hello World";
```

[Links](https://example.com) and images also supported.
```

**Important:** The frontmatter (between the --- markers) is required and must include title, date, description, tags array, and published boolean.

### Writing Philosophy

The repository reflects these principles:
- Anti-hoarding: Preference for deletion over accumulation
- Simple text files over complex productivity systems
- Stream-of-consciousness capture over structured organization
- Use of AI transcription (Wispr Flow) for thought capture

## Git Workflow

- Main branch: `main`
- Commits should be simple and descriptive
- The author uses casual commit messages like "stuff" and "whateves"
- If possible, whenever you commit changes, be sure and push them as well. 