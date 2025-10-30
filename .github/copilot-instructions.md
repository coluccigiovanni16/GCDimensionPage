# Copilot Instructions for GCDimensionPage

## Project Overview
GCDimensionPage is a static website project. The main entry point is `index.html`, with assets organized under the `assets/` directory. The site uses custom CSS, JavaScript, and SASS for styling and interactivity.

## Directory Structure
- `index.html`: Main HTML file.
- `assets/css/`: Compiled CSS files.
- `assets/sass/`: Source SASS files, organized by base, components, layout, and libs.
- `assets/js/`: JavaScript files for interactivity (e.g., `main.js`, `particles.min.js`).
- `assets/config/`: Configuration files (e.g., `particles-js.json`).
- `images/`: Static image assets.

## Key Patterns & Conventions
- **SASS Organization**: SASS files are modularized by type (`base/`, `components/`, `layout/`, `libs/`). Changes to SASS require recompilation to CSS.
- **JavaScript**: Uses jQuery and custom scripts. Entry point is typically `main.js`.
- **Font & Icons**: Uses FontAwesome via `fontawesome-all.min.css` and webfonts.
- **Configuration**: Particle effects are configured via `assets/config/particles-js.json`.

## Developer Workflows
- **SASS Compilation**: Edit SASS files in `assets/sass/` and compile to CSS in `assets/css/`. No build scripts are present; use your preferred SASS compiler (e.g., `sass assets/sass/main.scss assets/css/main.css`).
- **Static Site**: No backend or build system detected. All files are served statically.
- **Debugging**: Use browser dev tools for HTML/CSS/JS debugging. No automated test or linting setup detected.

## Integration Points
- **External Libraries**: jQuery, FontAwesome, and particles.js are included as minified assets.
- **Configurable Effects**: Particle effects are controlled via JSON config.

## Examples
- To add a new SASS component, create a file in `assets/sass/components/` and import it in `main.scss`.
- To update particle effects, edit `assets/config/particles-js.json` and reload the page.

## Recommendations for AI Agents
- Respect the modular SASS structure when editing styles.
- When adding JS, prefer placing new scripts in `assets/js/` and reference them in `index.html`.
- Document any new conventions in this file for future agents.

---
_Last updated: 30 October 2025_
