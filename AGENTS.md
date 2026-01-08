# Repository Guidelines

## Project Structure & Module Organization
- `Assignments/`: Quarto `.qmd` files for homework and quizzes, organized by module.
- `Textbook/`: Module chapters and supporting assets (including `images/` subfolders).
- `Templates/`: Required templates for assignments, quizzes, and textbook chapters.
- `Claude-planning/`: Planning notes for module development (one Markdown file per topic).
- `_site/`: Rendered website output (generated).
- `_freeze/`: Quarto execution cache (generated).

## Build, Test, and Development Commands
- `quarto preview`: Serve the site locally with live reload for `.qmd` changes.
- `quarto render`: Build the full site into `_site/`.
- `quarto render Textbook/Module 1 - EDA/chapter-1-eda.qmd`: Render a single page when iterating.

## Coding Style & Naming Conventions
- Content is Quarto Markdown (`.qmd`) with Python 3.12 code blocks.
- Use executable blocks with `{python}` and keep code outputs visible unless noted.
- Prefer descriptive file names that mirror module titles (e.g., `chapter-1-eda.qmd`).
- Follow template structure in `Templates/` for assignments, quizzes, and chapters.

## Testing Guidelines
- No automated test suite is present.
- Validate changes by rendering the relevant page(s) with `quarto render` and reviewing the HTML in `_site/`.

## Commit & Pull Request Guidelines
- Commit messages are short, sentence-case summaries (e.g., "Update course schedule for new 3-module structure").
- PRs should describe what changed, which pages were rendered, and link any related issues.
- If updating content, include a screenshot or link to the rendered `_site/` output for the modified page.

## Agent-Specific Instructions
- Follow `Claude.md` for course-writing rules, templates, and pedagogy constraints.
- When creating assignments or chapters, consult `content-overview.md` and update `Claude-planning/` first.
