# Little World — The Creative Internet Café

An original, pixel-inspired isometric portfolio office built by **haammkaki** as a frontend learning experiment.

[Live demo on GitHub Pages](https://trustnopeps.github.io/trustNOpeps/apps/little-world/)

## What works

- Isometric office rendered entirely with Canvas 2D; no downloaded sprites or borrowed game assets.
- Four clickable project desks linking to existing portfolio apps and anonymous studies.
- Three simulated coworkers with time-based routines, selectable roles and user-assigned tasks.
- Local fictional coin rewards, clock speed controls, activity feed, save/download and reset.
- Responsive UI, keyboard-accessible project links, and no account, API key, or backend requirement.

## Run

Open `index.html` through a local static server. Because it uses JavaScript ES modules, opening through `file://` may be blocked by browser security policies.

```bash
python3 -m http.server 8000
```

Then open `http://localhost:8000/` when running the server from this standalone repository root.

Run pure logic tests with `node --test core.test.mjs` from the repository root.

## Work orders

The local AI workflow downloads Qwen2.5-0.5B-Instruct on demand (approximately 786 MB of model weights). A module worker uses Transformers.js and WebAssembly. Nova scopes the brief, Byte plans the work, and Miso drafts the deliverable using the earlier sections. Each completed section is saved locally. Stop or reset terminates the worker. Reloading the page interrupts inference.

The offline budget tool performs integer arithmetic directly in the browser. Enter one line per item as `label | quantity | unit price in IDR`. Both modes export Markdown. Simulated desk visits and their fictional rewards run separately from work orders.
