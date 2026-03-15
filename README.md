# amplifier-writing-readme

Your AI agent writes a README for your project. It starts with "A tool that..." and lists features. No one reads past the second sentence.

This bundle provides a skill that teaches AI agents how to write READMEs people actually read — and that other AI agents can parse for capability signals and routing decisions.

## What the skill teaches

- **Problem before solution** — open with pain, not features
- **Two audiences** — humans scanning GitHub + AI agents parsing capabilities
- **Show, don't describe** — before/after examples over prose
- **Timing is respect** — tell people how long things take
- **Six-section structure** — opening, output example, components, quick start, how it works, built by
- **Quality checklist** — eight dimensions, self-rated, target 8+ on all

## Install

Add to any Amplifier bundle:

```yaml
# In your bundle.md includes:
includes:
  - bundle: git+https://github.com/cpark4x/amplifier-writing-readme@main
```

Or add directly:

```bash
amplifier bundle add git+https://github.com/cpark4x/amplifier-writing-readme@main
```

The skill becomes available as `writing-readmes` via `load_skill`.

## Built by

[Chris Park](https://www.linkedin.com/in/chrispark) — Microsoft Office of the CTO, AI Incubation.
