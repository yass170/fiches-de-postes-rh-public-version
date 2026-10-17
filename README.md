# HR Job Profiles — Interview-to-Document Workflow

An HR application that turns recorded interviews into structured job descriptions through transcription, synthesis, assisted drafting and human review.

HR teams can consolidate several interviews into one job profile while keeping source material, editable drafts, finalized versions and PDF output in the same workflow. Drafting assistance supports the reviewer; it does not replace the HR approval step.

## Users

| Role | Use |
|---|---|
| HR editor | Import interviews, review transcripts and syntheses, revise a profile and finalize a version. |
| Reader | Consult the job profiles available to their account. |
| Administrator | Manage local access, document settings and retention policies. |

## Main features

- **Audio intake.** Collect interview recordings and follow their transcription.
- **Multi-interview synthesis.** Consolidate information from several interviews before drafting.
- **Assisted writing.** Generate a structured draft and revise it within the application.
- **Version history.** Keep revisions and finalized job descriptions distinct.
- **PDF production.** Produce a document from an identified content version and template.
- **Shared workspace.** Bring imports, processing status, editing and administration together.

## Typical workflow

1. Create or open a job profile and import interview recordings.
2. Review transcripts and the consolidated interview synthesis.
3. Generate a draft, correct it and complete the HR review.
4. Finalize a version and retrieve its corresponding PDF.

## Project structure

```text
fiches-de-postes-rh-public-version/
├── backend/
│   ├── migrations/
│   │   └── versions/
│   ├── src/
│   │   └── job_profiles/
│   │       ├── api/
│   │       ├── auth/
│   │       ├── jobs/
│   │       ├── module-003/
│   │       ├── module-015/
│   │       ├── persistence/
│   │       └── app.py
│   ├── tests/
│   ├── tools/
│   ├── pyproject.toml
│   └── README.md
├── deploy/
│   ├── docker/
│   ├── scripts/
│   ├── tests/
│   └── README.md
├── docs/
│   ├── contracts/
│   ├── decisions/
│   ├── design/
│   │   ├── decisions.md
│   │   ├── requirements.md
│   │   └── verification.md
│   ├── issue/
│   │   └── README.md
│   ├── module-013/
│   ├── specifications/
│   └── README.md
├── frontend/
│   ├── src/
│   │   ├── api/
│   │   ├── components/
│   │   ├── pages/
│   │   └── validation/
│   ├── tests/
│   ├── package.json
│   └── README.md
├── issues/
│   ├── epics/
│   ├── features/
│   ├── tasks/
│   └── README.md
├── ARCHITECTURE.md
└── README.md
```

[Complete directory structure](docs/design/structure.md)

| Area | Responsibility |
|---|---|
| Web interface | React editing, interview intake, progress, history and preview screens. |
| Application API | FastAPI permissions, business operations, document versions and controlled downloads. |
| Durable worker | Transcription, synthesis and drafting outside interactive requests. |
| Persistence | PostgreSQL metadata and private storage for recordings and generated files. |
| Document rendering | PDF generation separated from the AI drafting stage. |

## Technology

React, TypeScript, Vite, Python, FastAPI, PostgreSQL, server-side AI adapters, ReportLab and Docker.

## Engineering

- [Architecture](ARCHITECTURE.md)
- [Product requirements](docs/design/requirements.md)
- [Design decisions](docs/design/decisions.md)
- [Verification strategy](docs/design/verification.md)

Interviews and job profiles contain sensitive HR material. Access control, private file delivery and human review are central to the design.

---

Source code, operational configuration and project-specific data are withheld for confidentiality.
