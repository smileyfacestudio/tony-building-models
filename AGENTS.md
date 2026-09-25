# SFS building-model project — agent instructions

## Scope

Support Sava and SFS with existing-condition capture, a future browser-based 3D model, and preliminary electrical/low-voltage/networking takeoffs for `CV255` and `NC3007`. Read `README.md`, the user's language-specific setup guide, `docs/project-brief.md`, and `docs/data-dictionary.md` first. This is currently a documentation-and-template starter, not a working viewer.

## Language

Sava's native language is Russian. If Sava is the operator, default to Russian unless he requests English. Keep IDs, filenames, and schema keys stable in English. Maintain equivalent Russian and English setup instructions.

## Public/private boundary

- This repository is PUBLIC. Only public-safe guidance, software, public-source links, and empty or clearly synthetic templates belong in commits, issues, PR descriptions, logs, or attachments.
- Actual site evidence, detailed layouts, pricing, private URLs, personal information and secrets do not belong here. Do not copy the SFS vault or its history.
- For site-specific work, confirm an approved private storage location first. An ignored `private/` directory can hold local work only after the human approves local handling. Ignoring a file does not make it encrypted, backed up, or safe to upload to another service.
- Never force-add ignored files. Before every commit, review the exact file list and diff for public suitability. Use explicit paths, not blanket staging.
- No invitations, org membership changes, visibility changes, paid services, outbound messages, record requests, deployments, or representations of property ownership without a specific user instruction.

## Evidence and estimation

- Every real geometry, device, route, or quantity needs a stable ID, `model_id`, `source_state`, confidence, and source references (or an explicit absence of evidence).
- Use exactly `verified_plan`, `observed_field`, `inferred`, `proposed`, or `unknown`. A verified plan records what a drawing says; it does not prove today's installed condition.
- Never infer concealed wiring, spare electrical capacity, code compliance, route lengths, room dimensions, or quantities from an attractive rendering. Leave unknown values blank in CSV or `null` in JSON; zero is a real measured value, not a placeholder.
- Separate existing observations, inference, proposed work, and allowances. Inferred/unknown conditions cannot silently become firm-price quantities. Proposed work must not be described as installed.
- Preserve original measurements and units. The eventual renderer may convert units; never silently interpret feet as meters.
- Keep material, labor, equipment, contingency, exclusions, and verification items distinct. Sava reviews trade assumptions; qualified professionals determine final design, safety, permitting, and construction requirements.
- No instructions to open energized equipment or perform live tests. Capture only what can safely and lawfully be observed with authorized access.

## Collaboration

Work locally first. For approved public-safe changes, use a short-lived branch and open a PR to `main`; an SFS maintainer reviews before merge. Do not push directly to `main`. Without Write access, return a public-safe proposed patch or work locally; do not upload client data to a public fork. This repository grants no authority or access to the SFS vault. End each task with changes made, evidence used, unknowns, and the next required input. Do not claim the model is complete while evidence or scale validation is missing.
