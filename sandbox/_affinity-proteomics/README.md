# Affinity proteomics PRIDE autoresearch drafts

Generated with the sdrf:autoresearch workflow for target `all PRIDE affinity proteomics datasets`, using PRIDE Archive project/file APIs, Europe PMC accession/publication searches, and the `affinity-proteomics`, `olink`, `somascan`, and human SDRF templates where applicable.

Summary:

- Confirmed PRIDE affinity submissions: 22
- New sandbox draft SDRFs: 22
- Platform families: 14 Olink, 8 SomaScan
- Organism template applied: human for 22 drafts
- Primary matrices read: 32 deposited NPX, ADAT, or Olink parquet files.
- Draft row model: one row per extracted sample-level matrix entry from the primary NPX/ADAT/parquet files.
- Total draft rows: 10,102 sample-level rows.
- Pruning: removed 159 columns where the field was not required by the active templates and every value was `not available`.
- Validation: 22 of 22 drafts pass `parse_sdrf validate-sdrf --template affinity-proteomics --skip-ontology` and the human template where applied.
- Platform-specific checks: the installed `parse_sdrf` registry does not expose `olink` or `somascan` schemas yet, so `comment[olink panel]`, `comment[olink platform]`, `comment[somascan menu]`, and `comment[somascan platform]` were checked against the local template-required columns.

Secondary wide abundance or raw Ct matrices were not used as sample inventories when a primary NPX or ADAT file was present; skipped files are recorded in `manifest.tsv`.

These are evidence-backed sandbox scaffolds, not final curator-reviewed submissions. Per-sample demographic values beyond direct matrix identifiers should be refined from deposited metadata spreadsheets or publication supplements before promotion to `datasets/`.

See `manifest.tsv` for PRIDE URLs, Europe PMC hits, platform calls, primary matrix counts, skipped secondary files, sample row counts, and draft paths. See `column-pruning.tsv` for the per-accession fields removed by the all-`not available` cleanup. See `autoresearch-round1.tsv` for per-accession draft status and validation status. See `validation-round2.tsv` for per-template validation results.
