# Copilot Instructions for AI Agents

## Project Overview
This is a portfolio site built with vanilla JavaScript, HTML, and CSS. The project uses a modular structure under `src/`, with logical separation for UI, world logic, utilities, and assets. Webpack is used for bundling, with configurations in `bundler/`.

## Key Directories & Files
- `src/` — Main source code
  - `js/` — Core JavaScript modules (e.g., `Experience.js`, `Renderer.js`, `World/`, `UI/`)
  - `css/` — All CSS files for different site sections
  - `assets/`, `fonts/` — Static assets
- `bundler/` — Webpack configs (`webpack.dev.js`, `webpack.prod.js`, `webpack.common.js`)
- `static/` — Images, models, and textures
- `readme.md` — Setup and workflow instructions

## Build & Development Workflow
- Install dependencies: `npm install`
- Start local dev server: `npm run dev` (serves at `localhost:8080`)
- Build for production: `npm run build` (outputs to `dist/`)

## Project-Specific Patterns
- **Modular JS:** Each major feature (UI, World, Utils) is a separate module. Example: `src/js/World/` for 3D world logic, `src/js/UI/` for interface components.
- **No Frameworks:** Pure JS/CSS/HTML, no React/Vue/Angular.
- **Asset Management:** Static assets are referenced via relative paths from `src/`.
- **Webpack:** Handles JS/CSS bundling and asset management. Adjust entry/output in `bundler/webpack.*.js` as needed.

## Conventions
- Use ES6 modules and classes for new JS code.
- Keep UI logic (`src/js/UI/`) and world/scene logic (`src/js/World/`) separate.
- Place new assets in the appropriate `src/assets/` or `static/` subfolder.
- CSS is split by page/section for maintainability.

## Integration Points
- No backend; all logic is client-side.
- Webpack is the only build tool; no Gulp/Grunt.
- No automated tests are present.

## Examples
- To add a new UI component: create a new file in `src/js/UI/`, export a class, and import it in `src/js/UI/UI.js`.
- To add a new 3D scene element: add a module in `src/js/World/`, then integrate it in `src/js/World/World.js`.

---
For more, see `readme.md` and the `bundler/` configs. Follow the modular structure and keep logic isolated by concern.
