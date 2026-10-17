# Product Requirements

An HR application that turns recorded interviews into structured job descriptions through transcription, synthesis, assisted drafting and human review.

## Users

| Role | Expected outcome |
|---|---|
| HR editor | Import interviews, review transcripts and syntheses, revise a profile and finalize a version. |
| Reader | Consult the job profiles available to their account. |
| Administrator | Manage local access, document settings and retention policies. |

## Functional scope

| Capability | User outcome |
|---|---|
| Audio intake | Collect interview recordings and follow their transcription. |
| Multi-interview synthesis | Consolidate information from several interviews before drafting. |
| Assisted writing | Generate a structured draft and revise it within the application. |
| Version history | Keep revisions and finalized job descriptions distinct. |
| PDF production | Produce a document from an identified content version and template. |
| Shared workspace | Bring imports, processing status, editing and administration together. |

## Main user journey

1. Create or open a job profile and import interview recordings.
2. Review transcripts and the consolidated interview synthesis.
3. Generate a draft, correct it and complete the HR review.
4. Finalize a version and retrieve its corresponding PDF.

## Acceptance priorities

- An editor can correct a transcript before using it in a synthesis.
- Concurrent edits do not silently overwrite one another.
- A generated proposal does not replace an intervening human revision.
- A finalized PDF corresponds to the intended finalized content.

## Product constraint

Interviews and job profiles contain sensitive HR material. Access control, private file delivery and human review are central to the design.
