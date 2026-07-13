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
- Repetitive-column cleanup: removed 110 repeated/overlapping optional columns, including duplicate `comment[sdrf template]` and redundant `comment[fraction identifier]`.
- Sample-type cleanup: ordinary assay samples no longer use `characteristics[sample type]`; when special roles are present, values are restricted to guideline terms such as `negative control`, `plate control`, `quality control sample`, and `calibrator`.
- Template refresh: restored the generic `comment[panel name]` recommended by `affinity-proteomics`, added `characteristics[ancestry category]`, added missing `characteristics[individual]`, and added missing SomaScan `comment[dilution]` fields.
- Current template check: 44 of 44 PAD SDRF copies (22 promoted `datasets/` files and 22 matching `sandbox/` files) pass local YAML checks for `affinity-proteomics`, `human`, and either `olink` or `somascan`.
- Validator note: `parse_sdrf` was not available in the current restricted session, so the latest pass checks the current local `sdrf-templates` YAML rules directly. Earlier `parse_sdrf --skip-ontology` results are retained in `validation-round2.tsv`.

Secondary wide abundance or raw Ct matrices were not used as sample inventories when a primary NPX or ADAT file was present; skipped files are recorded in `manifest.tsv`.

These are evidence-backed sandbox scaffolds, not final curator-reviewed submissions. Per-sample demographic values beyond direct matrix identifiers should be refined from deposited metadata spreadsheets or publication supplements before promotion to `datasets/`.

See `manifest.tsv` for PRIDE URLs, Europe PMC hits, platform calls, primary matrix counts, skipped secondary files, sample row counts, and draft paths. See `column-pruning.tsv` for the per-accession fields removed by the all-`not available` cleanup, `repetitive-column-removal.tsv` for the duplicate/overlapping optional fields removed, `sample-type-correction.tsv` for the sample-type guideline correction, and `template-refresh-round1.tsv` for the current template refresh. See `autoresearch-round1.tsv` for per-accession draft status and validation status. See `validation-round3.tsv` for current local YAML template results and `validation-round2.tsv` for earlier `parse_sdrf` results.
