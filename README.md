# Clear Quotes

A reusable AI skill for drafting and revising business quotes and service proposals. It helps customers and AI reviewers understand scope, commercial terms, supported strengths, and next steps.

## Use in a chat

Attach `SKILL.md`, or paste its contents, together with an existing quotation or customer brief. For example:

> Use this skill to improve my quotation. Preserve my business's tone and commercial terms, and ask me about missing details.

The template asks for your business profile in short groups. Customize a separate copy with approved company information; keep this starter generic. Review the finished quotation before sending it.

## Install as a Codex skill

From this repository's root, copy the skill and its UI metadata into a new `clear-quotes` directory under your Codex skills directory:

```sh
mkdir -p "${CODEX_HOME:-$HOME/.codex}/skills/clear-quotes/agents"
cp SKILL.md "${CODEX_HOME:-$HOME/.codex}/skills/clear-quotes/SKILL.md"
cp agents/openai.yaml "${CODEX_HOME:-$HOME/.codex}/skills/clear-quotes/agents/openai.yaml"
```

Check for an existing customized installation before copying. Invoke it with a request such as:

> Use $clear-quotes to revise this proposal using the attached customer brief.

## Requirements and contents

No scripts, packages, API keys, or external services are required by the skill. Supply an AI assistant and the business materials it needs. `SKILL.md` contains the complete instructions; `agents/openai.yaml` supplies optional Codex display metadata.

Keep customized company profiles and customer documents outside this repository. Unknown prices, dates, evidence, and guarantees must be confirmed. Drafting a quote does not authorize sending it or making commitments.

## License

No license has been selected for this export. This repository does not grant additional reuse or redistribution permissions.
