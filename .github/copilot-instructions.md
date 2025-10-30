# Copilot Instructions for GCDimensionPage

## Project Overview
GCDimensionPage is a static portfolio and resume website. The main entry point is `index.html`, which contains all primary content, navigation, and meta tags for SEO/social sharing. Assets are organized under the `assets/` directory, with custom CSS, JavaScript, and SASS for styling and interactivity. No backend or build system is present.

## Directory Structure
- `index.html`: Main HTML file. Contains all page sections (About, Experience, Education, Certifications, Skills, Contact) and meta tags for SEO, Open Graph, Twitter, and Schema.org.
- `assets/css/`: Compiled CSS files. `main.css` is the primary stylesheet; `noscript.css` is loaded for users with JS disabled.
- `assets/sass/`: Source SASS files, modularized by `base/`, `components/`, `layout/`, and `libs/`. Edit here and recompile to update styles.
- `assets/js/`: JavaScript files for interactivity. `main.js` is the entry point; `particles.min.js` and config enable animated backgrounds.
- `assets/config/`: Configuration files, e.g., `particles-js.json` for particle effects.
- `images/`: Static image assets, favicons, and profile images.

## Key Patterns & Conventions
**HTML Structure**: All content is in `index.html`, organized into `<article>` sections for About, Experience, Education, Certifications, Skills, and Contact. Navigation is handled via anchor links and in-page scrolling.

**SASS Organization**: SASS files are modularized by type (`base/`, `components/`, `layout/`, `libs/`). Always recompile SASS to CSS after changes. Example: `sass assets/sass/main.scss assets/css/main.css`.

**JavaScript**: Uses jQuery and custom scripts. `main.js` controls page interactivity; `particles.min.js` loads animated backgrounds using config from `assets/config/particles-js.json`.

**Font & Icons**: FontAwesome is included via `fontawesome-all.min.css` and webfonts in `assets/webfonts/`.

**SEO & Social**: Meta tags for SEO, Open Graph, Twitter, and Schema.org are set in `<head>`. Update these for changes in branding or content.

**Configuration**: Particle effects are controlled via `assets/config/particles-js.json` and loaded in the background div with `particlesJS.load()`.

## Developer Workflows
**SASS Compilation**: Edit SASS files in `assets/sass/` and compile to CSS in `assets/css/` using a manual command:
	```sh
	sass assets/sass/main.scss assets/css/main.css
	```
	No build scripts or automation are present.

**Static Serving**: All files are served statically. No backend, API, or build system is present. Deploy by copying files to a static host (e.g., GitHub Pages, Netlify).

**Debugging**: Use browser dev tools for HTML, CSS, and JS debugging. No automated tests, linting, or CI/CD detected.

## Integration Points
**External Libraries**: jQuery, FontAwesome, and particles.js are included as minified assets in `assets/js/` and `assets/css/`.

**Configurable Effects**: Particle.js background is configured via `assets/config/particles-js.json` and loaded in `index.html`.

## Examples
To add a new SASS component, create a file in `assets/sass/components/` and import it in `main.scss`:
```scss
@import "components/new_component";
```

To update particle effects, edit `assets/config/particles-js.json` and reload the page.

To add new JS functionality, create a file in `assets/js/`, then reference it in `index.html` after existing scripts.

## Recommendations for AI Agents
* Respect the modular SASS structure when editing styles. Always recompile after changes.
* When adding JS, place new scripts in `assets/js/` and reference them in `index.html` after existing scripts.
* Update meta tags in `index.html` for SEO/social changes.
* Document any new conventions in this file for future agents.
* No test or build automation is present; manual workflows only.

---
_Last updated: 30 October 2025_
