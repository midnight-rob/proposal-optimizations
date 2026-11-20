# Optimization Skills

A collection of reusable AI skills. Each skill lives in its own folder under `skills/`, with its instructions and any supporting resources kept together.

## Skill catalog

| Skill | Purpose |
| --- | --- |
| [Quote and Proposal Optimization](skills/quote-proposal-optimization/SKILL.md) | Draft and revise business quotes and service proposals so customers and AI reviewers can understand the offer, compare its terms, and identify supported strengths. |

## Choose how to use a skill

These skills use the open [Agent Skills format](https://agentskills.io/home): a folder containing `SKILL.md` and any supporting resources. Use your agent's native skill installer when it supports this format, or provide the instructions directly in a chat.

### Any chat assistant: ChatGPT, Claude, Gemini, Perplexity, Grok, and others

Open the skill from the catalog, copy the contents of its `SKILL.md`, and paste them into your conversation together with your quotation or customer brief. You can attach the file instead when your app supports Markdown attachments.

Ask the assistant to apply the supplied instructions, preserve your business's tone and commercial terms, and ask about missing details. For example:

> Use the attached skill to improve my quotation. Keep the commercial terms unchanged, preserve my business's voice, and ask me about any missing information.

This uses the skill as conversation context. Automatic discovery, persistent installation, and file support depend on the app. Provide the instructions again in a new chat unless you have saved them using a supported feature in that app.

The quote and proposal skill helps you customize a business profile in short groups. Save approved company information in a separate copy and review the finished quotation before sending it.

### Agents with native Agent Skills support

Download or clone this repository, then install the individual folder under `skills/` using your agent's documented skill directory or import workflow. Keep `SKILL.md` and its supporting resources together. Install the chosen skill folder rather than the entire collection as one skill.

The commands below run from this repository's root on macOS or Linux. Check for an existing customized installation before copying.

#### Claude Code

Copy the skill into your personal Claude Code skills directory:

```sh
mkdir -p "$HOME/.claude/skills"
cp -R skills/quote-proposal-optimization "$HOME/.claude/skills/"
```

Invoke it with `/quote-proposal-optimization` alongside your quotation and customer brief. For a project-only installation, use `.claude/skills/` in that project instead. See the [Claude Code skills documentation](https://code.claude.com/docs/en/skills).

#### Claude web or desktop

Package the `skills/quote-proposal-optimization` folder as a ZIP containing that folder and its files. In Claude, go to **Customize > Skills**, choose **+ > Create skill > Upload a skill**, upload the ZIP, and enable the skill. Availability depends on your account settings; Claude's skills feature requires code execution and file creation to be enabled. See [Use skills in Claude](https://support.claude.com/en/articles/12512180-use-skills-in-claude).

#### Gemini CLI

Copy the skill into your personal Gemini CLI skills directory:

```sh
mkdir -p "$HOME/.gemini/skills"
cp -R skills/quote-proposal-optimization "$HOME/.gemini/skills/"
```

In Gemini CLI, run `/skills reload`, then `/skills list` to confirm discovery. Ask Gemini to apply Quote and Proposal Optimization to your supplied quotation. See the [Gemini CLI skills documentation](https://geminicli.com/docs/cli/skills/). For the Gemini chat app, use the chat instructions above.

#### Codex

Copy the skill into your Codex skills directory:

```sh
mkdir -p "${CODEX_HOME:-$HOME/.codex}/skills"
cp -R skills/quote-proposal-optimization "${CODEX_HOME:-$HOME/.codex}/skills/"
```

Invoke it by mentioning `$quote-proposal-optimization` alongside your quotation and customer brief.

#### Other compatible agents

Follow your agent's instructions for importing an Agent Skills folder or placing it in a supported skills directory. Directory names and invocation syntax vary by product. If your app does not offer native skill loading, use the chat instructions above.

## Add another skill

Create `skills/<skill-name>/SKILL.md` with YAML frontmatter containing `name` and `description`. Match the folder name to the skill name using lowercase letters, digits, and hyphens. Keep any optional `agents/`, `scripts/`, `references/`, or `assets/` resources inside that skill's folder and add a row to the catalog above.

Each skill should be usable on its own. Document any dependencies with the skill that needs them.

## Requirements

The current skill requires an AI assistant and user-supplied business materials. It needs no scripts, packages, API keys, or external services. Its `agents/openai.yaml` supplies optional Codex display metadata.

Keep customized company profiles and customer documents outside this repository. Unknown prices, dates, evidence, and guarantees must be confirmed. Drafting a quote does not authorize sending it or making commitments.

## License

No license has been selected for this export. This repository does not grant additional reuse or redistribution permissions.
