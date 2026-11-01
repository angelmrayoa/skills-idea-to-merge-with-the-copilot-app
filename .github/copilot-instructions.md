# Copilot instructions

Project context Copilot should apply to every session in this repository.

## Stack

- Framework: Astro (static output).
- Language: TypeScript.
- Styling: plain CSS in the base layout.

## Conventions

- Keep components small and focused.
- Prefer semantic HTML and accessible markup.
- Do not close, or add closing keywords for, the exercise walkthrough issue (issue #1) in any pull request. The exercise's GitHub Actions workflows manage that issue. When you open a pull request for app work, link only the specific app work-item issue you are implementing.

## Persistence and hydration rules

- Bookmarks are persisted in the browser using `localStorage`, with each saved item storing the original URL and its generated short slug so the list survives a reload.
- Browser-only code must run behind a client-side boundary so Astro's static build never touches `localStorage` or other browser APIs during SSR. In this app, that means keeping reads and writes in a client script or a component gated with `client:load`.
