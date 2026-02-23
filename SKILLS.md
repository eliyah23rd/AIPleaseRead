# Skills

## upgrade_idea

Purpose:
- Upgrade an existing clean idea document without replacing it.

Required behavior:
- Preserve all substantive content from the original clean idea.
- Keep the original thesis, core claims, and major sections intact.
- Add new material as an extension, clarification, defense, or deeper treatment.
- Do not delete original arguments unless they are factually contradictory or explicitly rejected by the user.

Default output strategy:
- Read source from `AIPleaseRead/clean_ideas_md/<name>.md`.
- Write upgraded version to `AIPleaseRead/upgraded_clean/<name>.md`.
- Maintain the same title unless user asks to retitle.
- Integrate upgrade content naturally into existing sections (`Core Idea`, `Novel Contributions`, `Why It Matters`, `Open Questions`, `Next Steps`, etc.) by default.
- Do not use meta framing like "the original framing" unless explicitly requested.
- Use a separate addendum section only when the user explicitly asks for an addendum style.
- Do not reference document versions (e.g., "in this version", "upgraded version", "original post"). The output must read as a single unified presentation.

Content rules for upgrades:
- The upgrade is additive, not a rewrite-from-scratch replacement.
- Explicitly include the new user-specified emphasis.
- Ensure new material appears in core sections, not only in a trailing section.
- Ensure prose is self-contained and topic-focused, not process-focused.
- If user provides objections, answer them directly in the upgraded text.
- Keep tone consistent with the existing clean document style.
- Keep markdown clear and publication-ready.

Quality checklist before finalizing:
1. Confirm all original sections are still represented.
2. Confirm user-requested additions are present and prominent.
3. Confirm file is written under `AIPleaseRead/upgraded_clean/`.
4. Confirm no accidental loss of original core claims.

Suggested commit style when asked to commit:
- `Upgrade <idea name> with additive extension`

Sync requirement:
- Whenever this file changes, copy the updated file to `AIPleaseRead/SKILLS.md` so it can be committed in the top repo.
