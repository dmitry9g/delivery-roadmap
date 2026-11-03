# Delivery Roadmap

Delivery Roadmap is a Codex skill for planning and tracking software delivery with clear evidence, honest estimates, and explicit readiness for the next step. It helps keep one compact, current roadmap aligned with the project’s scope, ownership, constraints, and existing authorization.

## What it does

- Creates or updates a roadmap using an included template.
- Tracks stable step IDs, outcomes, owners, dependencies, acceptance criteria, evidence, issues, and successors.
- Distinguishes planned, ready, implementing, awaiting review, blocked, and complete work based on evidence.
- Preserves original estimates while separately recording elapsed or active effort and forecasting remaining work.
- Checks whether a successor is ready, including whether a nominal successor is already complete or blocked.
- Keeps effort forecasts separate from calendar forecasts, budgets, and recorded expenditure.
- Continues an already authorized next step when its readiness conditions pass.

## Package contents

- `SKILL.md` — the skill instructions and invocation metadata.
- `assets/roadmap-template.md` — a reusable roadmap format.
- `agents/openai.yaml` — Codex display name, description, and default prompt.
- `LICENSE` — MIT License.

## Installation

Copy the `delivery-roadmap` folder into your Codex skills directory:

```text
~/.codex/skills/delivery-roadmap/
```

The folder should contain `SKILL.md`, `agents/openai.yaml`, and `assets/roadmap-template.md`. Start a new Codex conversation and invoke the skill with `$delivery-roadmap`.

## Usage

Ask Codex to create a delivery roadmap, update an existing one, report progress against it, replan based on new evidence, or advance an approved roadmap. Give it the relevant goal, acceptance criteria, constraints, owners, permissions, and any user-set budget or deadline. It will use the template for a new roadmap and preserve the existing source of truth where one already exists.

## Limitations

This skill organizes and advances work within existing authorization. A roadmap does not itself authorize implementation, extra workers, messages to other people, or external actions. It is not a scheduler or background worker and cannot promise unattended continuation. Its progress and estimates depend on available evidence and any time measurements the project provides; unmeasured effort remains unknown.

The package is designed for Codex’s skill folder format. Other assistants may need adaptation.

## License

This project is licensed under the MIT License. See [LICENSE](LICENSE).
