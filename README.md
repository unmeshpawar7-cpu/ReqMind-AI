# ReqMind AI – run walkthrough

A screen-by-screen walkthrough of one complete ReqMind AI run: a single business idea (the FieldFlow field-service example) turned into requirements, architecture, user stories, tests, a traceability matrix, a change request and eight project documents.

Open `index.html` to view it. It has no build step and no dependencies.

## What's in the walkthrough

- **24 screens** from the app's web interface, from sign-up to the final project dashboard
- **The input**: the business idea and the answers to ten discovery questions
- **The output**: 65 requirements (31 functional, 14 non-functional, 9 business, 7 rules, 4 technical), searchable and filterable by type
- **What was fixed** in this round of requirement-quality work, and **what is still open**
- **Generated files** you can open or download

> The run used the app's mock AI mode (no Anthropic API key), so the content was produced by the built-in heuristics, not a language model.

## Repository layout

| Path | Contents |
| --- | --- |
| `index.html` | The walkthrough page (HTML, CSS and JS in one file) |
| `shots/` | 24 screenshots, `01-register.webp` to `24-overview.webp` |
| `files/` | BRD, SRS, FSD, TDD, user stories, test plan, traceability matrix and change impact report as PDF, plus `openapi.json` and the Gherkin acceptance criteria |

## View it

**Online with GitHub Pages:** Settings → Pages → Source: *Deploy from a branch* → Branch: `main`, folder `/ (root)`. The page will be at `https://unmeshpawar7-cpu.github.io/ReqMind-AI/`.

**Locally:** serve the folder so the screenshots and downloads load:

```bash
python3 -m http.server 8000
# open http://localhost:8000
```

Keyboard: use ← and → to move between screens. Each screen has its own link (`#step-1` to `#step-24`).

## The app itself

The application code lives in [`unmeshpawar7-cpu/ai-requirements-agent`](https://github.com/unmeshpawar7-cpu/ai-requirements-agent). The rebuilt ReqMind AI version shown here is on the `feature/reqmind-ai-rebuild` branch, which still needs to be pushed to GitHub from the `reqmind-ai-rebuild.bundle` file:

```bash
git clone reqmind-ai-rebuild.bundle reqmind
cd reqmind && git remote set-url origin https://github.com/unmeshpawar7-cpu/ai-requirements-agent.git
git push origin feature/reqmind-ai-rebuild
```
