# Future Projection App

Project overview
Future Projection App is a client-side single-page application built with React and TypeScript. It provides an interactive environment for exploring hypothetical future scenarios by projecting trends, visualizing outcomes, and comparing parameter-driven variations.

Core goals
- Provide an approachable UI for turning inputs and datasets into understandable projections.
- Make projections transparent and traceable: inputs, assumptions, and simple models are visible to the user.
- Keep the app lightweight and portable so it can run entirely in the browser.

Key features
- Interactive scenario builder: change parameters and see projection changes in real time.
- Visualizations for comparing multiple scenarios side-by-side.
- Small, deterministic projection models designed for clarity rather than black-box prediction.
- Extensible data layer so sample datasets or user-provided files can be swapped in.

Architecture (high level)
- Frontend: React + TypeScript powering a single-page app. UI is composed of modular components that encapsulate input controls, model logic, and visualization.
- State: local component state and shared context/state modules keep scenario parameters and derived results synchronized across views.
- Models: simple, deterministic functions that compute projections from inputs and optional dataset slices; designed to be auditable and easy to test.
- Assets and data: static sample datasets and configuration live in the project tree under `src/assets` and the `public` folder.

Tech stack
- React
- TypeScript
- Vite for fast bundling during development
- Minimal CSS and small visualization libraries for charts

Data & models
Projections are computed client-side from explicit input parameters and optional sample datasets. Models are intentionally simple (e.g., linear growth, compounded rates, configurable multipliers) so users can see how assumptions affect outcomes. If the project integrates external data later, those sources and any transformation steps should be documented and versioned.

Project layout (important files)
- `src/` — application source code (components, models, styles, assets)
- `src/main.tsx` — app entry
- `src/App.tsx` — top-level application component
- `public/` — static assets served with the app

License
This repository does not include a license file by default. Add a `LICENSE` that reflects how you want the project to be used.

