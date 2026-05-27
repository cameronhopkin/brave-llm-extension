# brave-llm-extension

A Brave browser extension that integrates ChatGPT via a Flask backend. Built in April 2023 as an early LLM browser integration experiment.

## Why this exists in 2026

This repo predates the current generation of LLM tooling. It is preserved as an honest record of where I was experimenting with browser-integrated LLM workflows before MCP, Anthropic skills, browser-native AI APIs, and broader agentic frameworks existed.

If you are looking for current AI security work, see:
- [`isc2-2026-agentic-ai-defense`](https://github.com/cameronhopkin/isc2-2026-agentic-ai-defense)
- [`isc2-2026-ai-code-review-workshop`](https://github.com/cameronhopkin/isc2-2026-ai-code-review-workshop)

## Original description

The extension opens a popup where the user types text and receives a response from the OpenAI ChatGPT API. A small Flask server (in `server/`) holds the API key, proxies requests to OpenAI, and returns the model output to the extension UI (in `extension/`). Docker support is included for the server.

This is a single-purpose proof-of-concept, not a maintained tool. Modern equivalents (browser AI sidebars, MCP-based clients, IDE-integrated agents) cover the same use case better.

## Original setup

The original setup instructions live in the [first commit's README](https://github.com/cameronhopkin/brave-llm-extension/blob/main/README.md). At a minimum it required an OpenAI API key in a `.env` file, Python 3.6+ with Flask, Flask-CORS, and the OpenAI Python library, and loading the unpacked extension via `brave://extensions` developer mode.

## License

MIT License, original license preserved. See [LICENSE](LICENSE).
