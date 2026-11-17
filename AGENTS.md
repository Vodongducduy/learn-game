# Repository Guidelines

## Project Structure & Module Organization

`index.html` contains the entire Wildroot farming game: page markup, inline CSS, and browser JavaScript. Pixel art and item icons are drawn with Canvas; there are no external assets, dependencies, or separate source and test directories.

JavaScript is organized into classes including `Inventory`, `Hotbar`, `InventoryUI`, `Input`, `Collision`, `World`, `Player`, `Camera`, `Farming`, `Foraging`, `UI`, and `Game`. Keep changes within the relevant class. Keep gameplay updates separate from rendering, and preserve the distinction between inventory contents and hotbar references.

## Build, Test, and Development Commands

- Open `index.html` in a modern browser to run the game directly.
- Alternatively, run `python -m http.server 8000` from the repository root, then visit `http://localhost:8000`. This requires Python and serves the files locally.

There is no build step, package manifest, lint command, or automated test runner. Do not assume `npm` scripts exist.

## Coding Style & Naming Conventions

Follow the surrounding compact HTML, CSS, and JavaScript style. Use two-space indentation for JavaScript class members, single-quoted JavaScript strings, and semicolons. Use PascalCase for classes, camelCase for functions and variables, and uppercase names for shared constants such as `TILE` and `CROPS`.

Preserve UTF-8 text, including Vietnamese interface strings. Retain integer-aligned Canvas drawing and pixelated scaling. No formatter or linter is configured; avoid broad formatting changes unrelated to the task.

## Testing Guidelines

Validate changes manually in the browser and check the developer console for errors. Exercise movement and collisions, hotbar selection, inventory dragging, planting and watering, harvesting and pickup, quest completion, and restart as relevant. Confirm that opening the inventory pauses gameplay. For interface changes, check narrow layouts and touch controls where available.

No testing framework, test naming convention, or coverage threshold currently exists. Describe the checks performed when submitting changes.

## Commit & Pull Request Guidelines

No Git history is available in this checkout, so established commit conventions cannot be inferred. Use concise, imperative commit subjects, for example `Fix hotbar item selection`.

Pull requests should explain the behavior changed, list manual validation, and link related issues when applicable. Include screenshots for visual changes and reproduction steps for bug fixes.