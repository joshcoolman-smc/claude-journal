# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a personal writing and notes repository focused on capturing thoughts about AI, technology, and productivity. The project uses a minimalist approach with no dependencies or complex tooling.

## Project Structure

- `README.md`: Main journal with dated entries about AI, creativity, and technology

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