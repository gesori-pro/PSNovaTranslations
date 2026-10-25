# Korean branch rules

- Read README_KO.md. Work on KO, keeping the Arks-Layer upstream history.
- Canonical edited text lives in rmd/*.json and csv/NpcBaseParameter.json in Git. Never replace it with a stale NAS working copy.
- Preserve IDs, OriginalText, Enabled, tags, variables and line breaks. Translate from current Japanese and surrounding context. Enabled is not review completion.
- Common terminology is NAS PSO2/Glossary with game=NOVA and context/exceptions. Do not create another glossary in this repository.
- Technical work, font/image/video edits, binary/build inputs, detailed review evidence and progress live on NAS PSNova_Shared. Edit/build locally, publish verified changes to NAS.
- Do not commit new game binaries, RMD/CPK/VPK archives, saves, dumps, personal unlock patches or credentials. Inherited upstream resources stay as historical source; do not add new technical payloads.
- Keep original/previous versions and unrelated local changes. Do not force push or reset another host's work. Structural checks and device QA must be reported separately.
