# Affinity proteomics PRIDE autoresearch drafts

Generated with the sdrf:autoresearch workflow for target `all PRIDE affinity proteomics datasets`, using PRIDE Archive project/file APIs, Europe PMC accession/publication searches, and the `affinity-proteomics`, `olink`, `somascan`, and human SDRF templates where applicable.

Summary:

- Confirmed PRIDE affinity submissions: 22
- New sandbox draft SDRFs: 22
- Platform families: 14 Olink, 8 SomaScan
- Organism template applied: human for 22 drafts
- Draft row model: one row per deposited affinity data matrix file selected from PRIDE RAW/RESULT or data-like files.
- Validation: 22 of 22 drafts pass `parse_sdrf validate-sdrf --template affinity-proteomics --skip-ontology` and the human template where applied.
- Platform-specific checks: the installed `parse_sdrf` registry does not expose `olink` or `somascan` schemas yet, so `comment[olink panel]`, `comment[olink platform]`, `comment[somascan menu]`, and `comment[somascan platform]` were checked against the local template-required columns.

These are evidence-backed sandbox scaffolds, not final curator-reviewed submissions. Per-sample demographic values, exact plate/sample maps, and panel version details should be refined from deposited metadata spreadsheets or publication supplements before promotion to `datasets/`.

See `manifest.tsv` for PRIDE URLs, Europe PMC hits, platform calls, file counts, and draft paths. See `autoresearch-round1.tsv` for per-accession draft status and validation status. See `validation-round1.tsv` for per-template validation results.
