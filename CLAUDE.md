# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a **wiki/documentation site** built with **MkDocs Material** that serves as a learning platform with interactive exercises. The site is deployed via GitHub Pages and includes custom Python macros for creating interactive learning components.

## Architecture

### Core Components

1. **MkDocs Configuration** ([mkdocs.yml](mkdocs.yml))
   - Uses Material theme with custom color scheme (amber primary, deep orange accent)
   - Configures markdown extensions for advanced features (admonitions, code annotation, MathJax, Mermaid diagrams)
   - Includes custom CSS/JS files for styling and functionality
   - Uses `macros` plugin to enable Python-based template functions

2. **Python Macros** ([main.py](main.py))
   - Custom MkDocs macros that generate interactive learning components:
     - `task()`: Creates collapsible exercise cards with questions, tips, and solutions
     - `youtube_video()`: Embeds YouTube videos in styled admonitions
     - `python_tutor()`: Generates interactive Python Tutor iframe embeds
     - `python_tutor_button()`: Creates buttons linking to Python Tutor
     - `link()`: Generates external links with icons and new tab behavior
   - These macros are used in Markdown files via `{{ macro_name(...) }}` syntax

3. **Content Structure**
   - `docs/index.md`: Main landing page with grid layout and navigation
   - `docs/content/`: Contains topic pages with exercises
   - `tasks/`: YAML files defining exercise parameters (title, question, solution, tip, difficulty)

4. **Custom Styling** ([docs/stylesheets/](docs/stylesheets/))
   - `grid.css`: Custom card styling with hover effects and animations
   - `video_admonition.css`: Custom styling for video admonitions (red theme)
   - `python_tutor_admonition.css`: Custom styling for Python Tutor embeds (yellow theme)
   - `logo.css`: Logo styling
   - `mermaid.css`: Mermaid diagram centering

5. **JavaScript** ([docs/javascripts/mathjax.js](docs/javascripts/mathjax.js))
   - MathJax configuration for rendering mathematical expressions
   - Supports inline (`\(...\)`) and display (`\[...\]`) math

### Deployment Pipeline

**CI/CD** ([.github/workflows/ci.yml](.github/workflows/ci.yml))
- Triggers on push to `main` or `master` branches
- Deploys to GitHub Pages using `mkdocs gh-deploy --force`
- Uses Python 3.x with caching for MkDocs Material

## Development Commands

### Local Development

```bash
# Create virtual environment (Windows)
python -m venv venv
.\venv\Scripts\Activate.ps1

# Install dependencies
pip install -r requirements.txt

# Serve locally
mkdocs serve
```

### Content Creation

**Adding a new exercise/task:**
1. Create a YAML file in `tasks/` directory (e.g., `tasks/02_00_01.yaml`)
2. Define exercise parameters:
   ```yaml
   title: Exercise Title
   question: |
     Question text with optional MathJax: $x^2$
   solution: |
     ```csharp
     // Code solution
     ```
   solution_video: https://youtube.com/embed/...
   tip: Optional hint
   difficulty: 1  # Number of chili peppers
   ```
3. Reference in Markdown: `{{ task(file="tasks/02_00_01.yaml") }}`

**Adding Python Tutor embeds:**
- Inline iframe: `{{ python_tutor("code_string", "Title") }}`
- Button link: `{{ python_tutor_button("code_string", "Title") }}`

**Adding YouTube videos:**
- `{{ youtube_video("https://youtube.com/embed/...", "Video Title") }}`

**Adding external links:**
- `{{ link("Link Text", "https://example.com") }}`

### Testing & Validation

```bash
# Check for broken links (if using mkdocs-linkcheck plugin)
# Note: This project doesn't have a specific test command
# The CI pipeline automatically validates deployment
```

## Key Patterns

### Exercise Structure
- Exercises use collapsible admonitions (`??? question "..."`)
- Solutions are hidden by default but expandable
- Difficulty is shown with chili pepper icons (🌶)
- Videos can be embedded in both question and solution sections

### MathJax Usage
- Inline math: `\(...\)` or `$...$` (configured in mkdocs.yml)
- Display math: `\[...\]` or `$$...$$`
- Processed by MathJax via custom JavaScript

### Mermaid Diagrams
- Use fenced code blocks with `mermaid` language
- Diagrams are automatically centered via CSS

### Custom Admonitions
- `video`: Red-themed for YouTube embeds
- `python_tutor`: Yellow-themed for Python Tutor embeds
- `info`, `success`, `tip`: Standard MkDocs admonitions

## Important Files

- **[main.py](main.py)**: Python macros for interactive components
- **[mkdocs.yml](mkdocs.yml)**: MkDocs configuration and theme settings
- **[docs/index.md](docs/index.md)**: Main landing page with grid layout
- **[tasks/](tasks/)**: YAML exercise definitions
- **[docs/stylesheets/](docs/stylesheets/)**: Custom CSS for styling
- **[.github/workflows/ci.yml](.github/workflows/ci.yml)**: GitHub Actions deployment workflow

## Notes

- The site is in **German** - all content and UI text is in German
- The project uses **Material for MkDocs** theme
- Custom macros are registered via `@env.macro` decorators in `main.py`
- The `watch` configuration in mkdocs.yml includes the `tasks` directory for live reload
- The site includes social links to Qualidy GmbH in the footer
- MathJax is configured to process HTML elements with class `arithmatex`