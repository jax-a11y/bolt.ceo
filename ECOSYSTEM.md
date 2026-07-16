# Ecosystem Position: bolt.ceo

> This repository is part of the [SkinTwin-AI ecosystem](https://github.com/jax-a11y/skintwin-ecosystem-design).
> Its machine-readable manifest lives at [`.skintwin/manifest.json`](./.skintwin/manifest.json); the
> ecosystem-wide source of truth is `registry/ecosystem.json` in the hub repo.

**Layer:** dev-tooling · **Role:** orchestration-ide

bolt.ceo is **JAX CEO (Cognitive Execution Orchestration)**, a fork of bolt.diy: an AI
coding-agent web IDE (Remix + Vite, deployable to Cloudflare Pages, Docker, or Electron)
that runs projects in an in-browser WebContainer runtime and ships the Marduk and
Deep Tree Echo agent persona prompts. In the ecosystem it sits in the dev-tooling layer
as the orchestration/dev IDE used to build and operate the other repos — it serves
developers rather than participating in the runtime service mesh.

## Provides

Nothing — as developer/orchestration tooling, this repo exposes no runtime API,
dataset, or spec contract to other ecosystem services.

## Consumes

Nothing — the IDE talks to LLM providers and its own WebContainer runtime; it does not
call the ecosystem's REST/GraphQL contracts.

## CI

CI runs in `ci.yaml` (typecheck + vitest); the repo keeps its own workflows rather than
the hub's reusable templates. Reusable `workflow_call` CI templates are documented in
`ci/README.md` of [skintwin-ecosystem-design](https://github.com/jax-a11y/skintwin-ecosystem-design).
