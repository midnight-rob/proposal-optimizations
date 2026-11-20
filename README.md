# Optimization Skills

A collection of reusable AI skills. Each skill lives in its own folder under `skills/`, with its instructions and any supporting resources kept together.

## Skill catalog

| Skill | Purpose |
| --- | --- |
| [Quote and Proposal Optimization](skills/quote-proposal-optimization/SKILL.md) | Draft and revise business quotes and service proposals so customers and AI reviewers can understand the offer, compare its terms, and identify supported strengths. |

## Use in a chat

Open the skill from the catalog and attach its `SKILL.md`, or paste its contents, together with your quotation or customer brief. Ask the assistant to apply the skill, preserve your business's tone and commercial terms, and ask about missing details.

The quote and proposal skill helps you customize a business profile in short groups. Save approved company information in a separate copy and review the finished quotation before sending it.

## Install a skill in Codex

From this repository's root, copy the chosen skill folder into your Codex skills directory. For the current skill:

```sh
mkdir -p "${CODEX_HOME:-$HOME/.codex}/skills"
cp -R skills/quote-proposal-optimization "${CODEX_HOME:-$HOME/.codex}/skills/"
```

Check for an existing customized installation before copying. Invoke the installed skill by mentioning `$quote-proposal-optimization` alongside your quotation and customer brief.

## Add another skill

Create `skills/<skill-name>/SKILL.md` with YAML frontmatter containing `name` and `description`. Match the folder name to the skill name using lowercase letters, digits, and hyphens. Keep any optional `agents/`, `scripts/`, `references/`, or `assets/` resources inside that skill's folder and add a row to the catalog above.

Each skill should be usable on its own. Document any dependencies with the skill that needs them.

## Requirements

The current skill requires an AI assistant and user-supplied business materials. It needs no scripts, packages, API keys, or external services. Its `agents/openai.yaml` supplies optional Codex display metadata.

Keep customized company profiles and customer documents outside this repository. Unknown prices, dates, evidence, and guarantees must be confirmed. Drafting a quote does not authorize sending it or making commitments.

## License

No license has been selected for this export. This repository does not grant additional reuse or redistribution permissions.
