# LIMBIC Engine - Documentation Site

A self-contained static documentation website for sharing with collaborators,
reviewers, and prospective integrators.

## View it

No build step. No server required.

```bash
# Option A - open directly in a browser
xdg-open docs-site/index.html        # Linux
open docs-site/index.html             # macOS

# Option B - serve locally (nicer URLs, no file:// quirks)
cd docs-site && python3 -m http.server 8080
# then visit http://localhost:8080
```

## Pages

- `index.html` - Introduction: what LIMBIC is, the pipeline, a minimal example, how it differs.
- `quickstart.html` - Install, link, hello-agent, run.
- `architecture.html` - Three layers, the SENSE → … → LEARN pipeline, data model, threading.
- `modules.html` - All 30 brain modules grouped by function.
- `api.html` - Full C++ SDK surface: lifecycle, perception, decisions, state, ops, presets, personalities, params.
- `examples.html` - Minimal loop, town scenario, dialogue context, Python and Unity snippets.

## Share

Zip the folder and send it:

```bash
zip -r limbic-docs.zip docs-site
```

The recipient just unzips and opens `index.html` - works fully offline.

## Edit

Plain HTML + one stylesheet (`assets/style.css`). No frameworks, no JS build.
To change content, edit the HTML directly. To change look, edit the CSS.

## Source of truth

This site summarises material that lives in:

- `sdk/README.md` - the full 956-line SDK reference
- `sdk/include/limbic/limbic_engine.hpp` - annotated C++ API header
- `sdk/include/limbic/limbic.h` - annotated C FFI header
- `core/include/modules/` - the 30 brain module headers
- `docs/` - architecture papers and audits

When those move, refresh the site.
