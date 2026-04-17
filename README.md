# Claude Skills

A collection of custom skills for [Anthropic's Claude](https://claude.ai), built primarily for fiction writing and editing.

Each skill is a self-contained folder with its own `SKILL.md` and supporting reference files. Skills teach Claude to follow a specific workflow or produce structured output for a particular kind of task.

## Skills in this repo

### 📖 [novel-editor](./novel-editor/)
A structured editorial review system for fiction manuscripts. Catches grammar and style issues, tracks character voice consistency, flags plot contradictions and timeline problems, monitors foreshadowing (planted → reinforced → paid off), analyzes pacing, and enforces world-building continuity.

Ships with six reference templates for a complete story bible:
- `characters.md` — character profiles and voice fingerprints
- `plot-tracker.md` — scene list, established facts, timeline
- `foreshadowing-ledger.md` — setups and payoffs
- `knowledge-matrix.md` — who knows what, and when
- `style-guide.md` — target prose voice and genre conventions
- `world-bible.md` — world rules, geography, systems

*(More skills coming — this section will grow.)*

## How to install a skill

Each skill folder can be installed as a `.skill` file in Claude:

1. Download the skill's folder (e.g., `novel-editor/`) — either clone the whole repo or download the folder as a zip from GitHub
2. Zip the **folder itself** (not its contents — the zip should contain `novel-editor/SKILL.md`, not `SKILL.md` at the root)
3. Rename the resulting `.zip` file to `.skill`
4. Upload it through Claude's skill interface

## How to work with the markdown files directly

If you don't want to install the skill, you can use the reference templates as plain working documents. Clone the repo:

```bash
git clone https://github.com/YOURUSERNAME/claude-skills.git
```

Then open the markdown files in any editor ([Obsidian](https://obsidian.md) is a great fit for this kind of working bible). When you want Claude to review a chapter, paste the relevant reference files into chat along with your draft.

## Using this as a starting point

The reference templates in `novel-editor/references/` are populated with generic placeholder content. Copy the folder, delete the examples, and fill in your own story. The templates are meant to be edited — they're scaffolding, not scripture.

## License

MIT — see [LICENSE](./LICENSE). Use, modify, and share freely. If these are useful to you, I'd love to hear about it.

## Contributing / feedback

If you have ideas, improvements, or just want to share what you built on top of these, open an issue or a pull request.
