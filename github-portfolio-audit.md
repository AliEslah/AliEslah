# GitHub Portfolio Audit - AliEslah

Audit date: July 1, 2026
GitHub profile reviewed: https://github.com/AliEslah
Primary positioning: AI Backend Engineer

## Execution Notes

- Reviewed all public owner repositories visible through the GitHub public API.
- Cloned shallow public copies locally to inspect README files, project structure, tests, Docker, licenses, environment examples, and obvious risk signals.
- No repositories were deleted, archived, renamed, made private, force-pushed, or transferred.
- No real secrets were printed or moved.
- `gh` is installed locally but not authenticated, so issues, pushes, and pull requests were not created from this environment.

## 1. Executive Summary

Your GitHub portfolio has one strong flagship repository today: `recruitment-agent`. It already communicates the right direction for AI Backend Engineering because it includes FastAPI, PostgreSQL, LangGraph, local LLM workflows, Docker, tests, documentation, security notes, and a product-like domain.

The main branding problem is that the rest of the public account still looks like an older mixed learning/CV archive. `Cv`, `exchange`, and `courses` dilute the AI backend signal and introduce privacy or quality concerns. `subtitle-translator` is safe enough as a small utility but needs modernization before it should be shown as a support project.

The fastest improvement is to make the profile README sharper, pin only relevant repositories, add strong metadata to `recruitment-agent`, and move old personal/tutorial repositories out of the recruiter path after explicit approval.

## 2. Current GitHub Branding Problems

- The profile currently has only one clear AI/backend portfolio project.
- `recruitment-agent` has no public repository description or topics, even though it is the best repository.
- The profile README referenced a deleted or unavailable `data-profile` style project, which weakens trust.
- Old repositories (`Cv`, `exchange`, `courses`) dominate the public repo list and do not match the AI Backend Engineer positioning.
- Some repositories have minimal READMEs, no setup instructions, no CI, no `.env.example`, and no architecture notes.
- Public artifacts include old SQLite databases, backup files, certificates/CV material, and stale Django settings.
- Several repo names are not recruiter-friendly: `Cv` should not be public portfolio material, and `exchange` is vague for a stale crypto wallet fork.

## 3. Strongest Repositories

### 1. `recruitment-agent`

Classification: A. Portfolio flagship
URL: https://github.com/AliEslah/recruitment-agent

Why it is strong:

- Real product-shaped AI backend system.
- Uses FastAPI, PostgreSQL, SQLAlchemy, Alembic, LangGraph, LM Studio, Next.js, Docker, and tests.
- README explains purpose, limits, architecture, quick start, evaluation, security expectations, and validation commands.
- Includes `.env.example`, `.env.test.example`, Dockerfile, Docker Compose, docs, evals, test suites, issue templates, PR template, contributing file, security file, and license.

Main gaps:

- Missing repository description and topics.
- No GitHub Actions CI workflow visible.
- GitHub license detection returned `NOASSERTION` even though the repository contains AGPL-3.0 text. This may be due to wording/metadata and should be checked.
- Could benefit from a compact architecture diagram in README or docs.

### 2. `AliEslah`

Classification: Portfolio infrastructure
URL: https://github.com/AliEslah/AliEslah

Why it matters:

- This repo controls the first impression on the GitHub profile.
- It should clearly position you as an AI Backend Engineer within the first 10 seconds.

Main gaps before this update:

- Slightly cluttered visual style.
- Included a featured project section for a missing/deleted project.
- Could be more direct about production-minded backend engineering.

### 3. `subtitle-translator`

Classification: B/C. Portfolio support project only after cleanup
URL: https://github.com/AliEslah/subtitle-translator

Why it may be useful:

- Small Python automation utility.
- Has an MIT license and a short README.

Main gaps:

- Outdated dependencies.
- No tests, CI, `.gitignore`, `.env.example`, or package structure.
- README contains broken setup syntax (`pip install requirements.txt` should be `pip install -r requirements.txt`).
- The script relies on hard-coded paths and side-effect files.

## 4. Weak, Risky, or Low-Signal Repositories

| Repository | Why It Is Weak Or Risky | Recommendation |
| --- | --- | --- |
| `Cv` | Public personal/CV/certificate material, no README, committed SQLite database, old Django app, case-colliding PDF filenames. | Make private after approval or replace with a sanitized portfolio/CV project. |
| `exchange` | Forked stale Django crypto wallet, committed SQLite database, backup files, Django settings risk, wallet code prints generated mnemonic/key material at runtime. | Archive or make private after approval. Do not pin. |
| `courses` | Forked course material with notebooks/slides, not aligned with AI backend portfolio, no setup/test story. | Archive or keep unpinned as learning/course material. |
| `subtitle-translator` | Small and old, minimal docs, no tests, outdated dependencies. | Keep public only if modernized into a clean Python CLI support project. |

## 5. Security And Privacy Risks

High priority:

- `Cv` contains personal artifacts such as certificates/images/PDFs plus a committed SQLite database. This should not remain prominent in a professional AI backend portfolio.
- `exchange` contains a committed SQLite database and stale Django settings files. If any secret in that repo was ever used outside local experimentation, rotate it.
- `exchange` includes editor backup files (`~` and `#...#`) that should never be in a polished public repository.
- `exchange` wallet sample code prints generated mnemonic/key-related output at runtime. Even if not a real secret today, it is a bad public security signal for a backend portfolio.

Medium priority:

- `recruitment-agent` has local placeholder credentials in `.env.example`, which is acceptable when clearly marked as local-only. Keep real `.env` files ignored and never commit them.
- Public repos should add or tighten `.gitignore` rules for `.env`, SQLite files, generated outputs, local notebooks, editor backups, and OS files.

## 6. Recommended Pinned Repositories

Current public account:

1. `recruitment-agent` - pin now.

Do not pin today:

- `Cv`
- `exchange`
- `courses`
- `subtitle-translator` until it is cleaned up

Recommended future pinned set:

1. `recruitment-agent`
2. `rag-knowledge-api`
3. `fastapi-production-template`
4. `langgraph-agent-workflows`
5. `subtitle-translator` only after modernization, or a better Python automation utility
6. `n8n-llm-agent-nodes` only if it contains no private/company code

## 7. Recommended Archive Or Private Candidates

Do not perform these actions without explicit approval.

| Repository | Recommended Visibility Action | Reason | Priority |
| --- | --- | --- | --- |
| `Cv` | Make private | Personal documents/certificates and old DB-backed Django material are not useful public hiring signals. | High |
| `exchange` | Archive or make private | Stale fork, crypto wallet context, DB/settings artifacts, and weak code quality signal. | High |
| `courses` | Archive or keep public but unpinned | Course/tutorial material is not aligned with AI backend positioning. | Medium |

## 8. Recommended New Portfolio Repositories

### 1. `rag-knowledge-api`

One-line description: Production-style FastAPI RAG API with ingestion, chunking, vector search, citations, evaluation, and observability.

Why it helps your career:

- Directly targets AI Backend Engineer, RAG Engineer, and LLM Workflow Engineer roles.
- Shows backend depth beyond a notebook demo.
- Makes retrieval, storage, evaluation, and API design visible.

MVP feature list:

- FastAPI REST API for document upload, ingestion, search, and question answering.
- PostgreSQL plus pgvector or Qdrant vector store.
- Object storage through local MinIO/S3-compatible API.
- Async ingestion pipeline with status tracking.
- Chunking, metadata extraction, embedding, retrieval, reranking placeholder, and citation output.
- Structured response schemas with source attribution.
- Evaluation dataset and repeatable quality checks.
- Docker Compose local stack.
- API tests and ingestion tests.
- Clear security boundaries around uploaded files.

Ideal README structure:

- Problem statement
- Architecture diagram
- Quick start
- API examples
- Ingestion workflow
- Retrieval and answer flow
- Evaluation
- Environment variables
- Tests and CI
- Limitations and roadmap

Suggested stack:

- Python, FastAPI, Pydantic, SQLAlchemy, PostgreSQL, pgvector or Qdrant, MinIO, Docker Compose, pytest, ruff, optional LangChain/LangGraph.

First 10 issues/tasks:

1. Scaffold FastAPI app, settings, logging, and health endpoints.
2. Add Docker Compose for API, PostgreSQL, pgvector or Qdrant, and MinIO.
3. Create document upload and object storage service.
4. Add ingestion job model and status endpoints.
5. Implement text extraction and chunking pipeline.
6. Add embeddings adapter with local/dev provider abstraction.
7. Implement retrieval endpoint with metadata filters.
8. Implement answer endpoint with citations and structured output.
9. Add evaluation fixtures and quality report command.
10. Add GitHub Actions CI for lint and tests.

### 2. `fastapi-production-template`

One-line description: Reusable production-minded FastAPI template with auth, migrations, settings, Docker, CI, tests, and observability basics.

Why it helps your career:

- Shows backend engineering fundamentals independent of AI hype.
- Useful for recruiters evaluating maintainability, structure, and delivery readiness.

MVP feature list:

- FastAPI app layout with routers, services, repositories, schemas, and dependencies.
- PostgreSQL, SQLAlchemy, Alembic, Pydantic settings.
- JWT auth and role-based access control.
- Dockerfile and Docker Compose.
- Structured logging and request IDs.
- Health/readiness endpoints.
- Pytest test setup with DB fixtures.
- Ruff formatting/linting.
- GitHub Actions CI.
- Example CRUD module.

Ideal README structure:

- What this template gives you
- Architecture and folder structure
- Quick start
- Configuration
- Auth model
- Database and migrations
- Testing
- CI
- Production checklist
- Extension guide

Suggested stack:

- Python, FastAPI, Pydantic, SQLAlchemy, Alembic, PostgreSQL, Docker Compose, pytest, ruff, GitHub Actions.

First 10 issues/tasks:

1. Create base FastAPI project structure.
2. Add settings model and environment examples.
3. Add PostgreSQL and Alembic setup.
4. Add auth module with JWT and password hashing.
5. Add role-based dependency helpers.
6. Add example resource module.
7. Add Dockerfile and Docker Compose.
8. Add pytest database fixtures.
9. Add ruff and formatting configuration.
10. Add CI workflow and README production checklist.

### 3. `langgraph-agent-workflows`

One-line description: Practical LangGraph workflow examples for tool use, approval gates, retries, state persistence, and evaluation.

Why it helps your career:

- Directly supports Agentic AI, LLM Workflow Engineer, and AI Backend roles.
- Demonstrates that you understand control flow, state, and reliability instead of only prompt demos.

MVP feature list:

- Multiple minimal workflows with separate folders.
- Tool-calling workflow with typed tool input/output.
- Human approval workflow.
- Retry and fallback workflow.
- RAG-assisted workflow.
- Persistent state/checkpointing example.
- Evaluation fixtures.
- FastAPI wrapper for at least one workflow.
- Dockerized local run path.
- Architecture notes for each pattern.

Ideal README structure:

- Why LangGraph
- Workflow catalog
- Quick start
- Diagrams
- API wrapper
- Testing and evaluation
- Pattern notes
- Limitations
- Roadmap

Suggested stack:

- Python, LangGraph, LangChain Core, FastAPI, Pydantic, SQLite/PostgreSQL checkpointing, pytest, Docker.

First 10 issues/tasks:

1. Scaffold repo and dependency management.
2. Add typed state schemas and shared tool abstractions.
3. Build simple tool-calling workflow.
4. Build human approval workflow.
5. Build retry/fallback workflow.
6. Add checkpointing example.
7. Add FastAPI endpoint for one workflow.
8. Add Mermaid diagrams in docs.
9. Add tests for state transitions.
10. Add evaluation fixtures and CI.

### 4. `n8n-llm-agent-nodes`

One-line description: Safe n8n workflow examples for LLM-backed automation, tool calls, and human approval.

Why it helps your career:

- Shows workflow automation experience.
- Bridges backend systems, agents, and real operational processes.

Important safety condition:

- Publish only if no company/private workflows, credentials, customer data, endpoints, prompts, or internal business logic are exposed.

MVP feature list:

- Sanitized example workflows.
- Local-only credential placeholders.
- FastAPI webhook receiver example.
- LLM classification workflow.
- Human approval workflow.
- Error handling and retry path.
- Docker Compose local n8n setup.
- Example payloads.
- Security checklist.
- Import/export instructions.

Ideal README structure:

- What workflows are included
- Local setup
- Workflow diagrams
- Example payloads
- Credential safety
- Backend integration
- Testing workflows
- Limitations
- Roadmap

Suggested stack:

- n8n, FastAPI, Docker Compose, PostgreSQL, local LLM or OpenAI-compatible placeholder, webhook endpoints.

First 10 issues/tasks:

1. Create sanitized local n8n Docker Compose setup.
2. Add README safety policy.
3. Build FastAPI webhook receiver.
4. Add example classification workflow.
5. Add human approval workflow.
6. Add retry/error path workflow.
7. Add local payload examples.
8. Add workflow screenshots or diagrams.
9. Add import/export instructions.
10. Add security review checklist.

## 9. Quick Wins

1. Update the profile README to remove missing projects and sharpen AI backend positioning. Done locally in this branch.
2. Add a repository description to `recruitment-agent`.
3. Add relevant topics to `recruitment-agent`.
4. Pin `recruitment-agent` and unpin or avoid pinning older repos.
5. Make `Cv` private after approval.
6. Archive or make `exchange` private after approval.
7. Add GitHub Actions CI to `recruitment-agent` for backend lint/tests and frontend lint/typecheck/tests.
8. Add an architecture diagram to `recruitment-agent`.
9. Modernize `subtitle-translator` or leave it unpinned.
10. Create one new focused RAG/backend repository before adding more small projects.

## 10. 30-Day Improvement Roadmap

### Days 1-3: Profile And Visibility Cleanup

- Merge the updated profile README.
- Add `github-portfolio-audit.md` to the profile repository.
- Update `recruitment-agent` description and topics.
- Pin `recruitment-agent`.
- Decide whether `Cv`, `exchange`, and `courses` should be private or archived.

### Days 4-7: Flagship Repository Polish

- Add GitHub Actions CI to `recruitment-agent`.
- Add an architecture diagram.
- Add screenshots or a short screen recording/GIF if possible.
- Add a concise "Why this exists" section near the top of the README.
- Confirm AGPL license detection.

### Days 8-14: Build RAG Portfolio Repo

- Create `rag-knowledge-api`.
- Implement ingestion, vector search, answer endpoint, citations, and tests.
- Add Docker Compose.
- Publish a polished README with architecture and API examples.

### Days 15-21: Backend Template Repo

- Create `fastapi-production-template`.
- Add auth, migrations, settings, Docker, tests, and CI.
- Make it reusable enough that a hiring team can clone and run it quickly.

### Days 22-30: Agent Workflow Repo

- Create `langgraph-agent-workflows`.
- Implement 3-5 small but serious workflow patterns.
- Add diagrams, tests, and a FastAPI wrapper.
- Pin the best new repositories and revisit profile copy.

## Repository Classification Matrix

| Repository | Class | Current Problem | Recommended Action | Exact Changes Needed | Priority |
| --- | --- | --- | --- | --- | --- |
| `recruitment-agent` | A. Portfolio flagship | Strong code/docs, but missing metadata and CI. | Keep public, pin, polish. | Add repo description; add topics; add GitHub Actions CI; add architecture diagram; verify license detection. | High |
| `AliEslah` | Profile infrastructure | First impression needed cleanup and removal of missing project reference. | Keep public, merge README rewrite and audit. | Update `README.md`; add `github-portfolio-audit.md`; update repo description/topics. | High |
| `subtitle-translator` | B/C. Support project after polish | Small old utility with outdated dependencies and weak docs. | Keep public only if modernized; do not pin yet. | Add `.gitignore`; fix README install command; convert to CLI; remove hard-coded path; add tests; update dependencies; add CI. | Medium |
| `Cv` | D/F. Archive/private candidate and privacy risk | Personal documents/certificates, old Django app, committed SQLite DB, no README. | Make private after approval or rebuild as sanitized portfolio site. | Remove personal docs from public view; remove DB; add README only if kept public; fix case-colliding PDF names. | High |
| `exchange` | D/E/F. Archive/private candidate | Forked stale crypto wallet, committed DB, backup files, settings risk, weak crypto/security signal. | Archive or make private after approval. | Remove DB/backups; rotate any reused settings secrets; add README disclaimer if kept public; do not pin. | High |
| `courses` | E. Fork/tutorial/learning repo | Course notebooks/slides are not aligned with AI backend positioning. | Archive, or keep public but unpinned. | Add README saying it is course material; add topics only if kept public; do not pin. | Medium |

## Repository Metadata Recommendations

| Repository | Suggested Description | Suggested Topics |
| --- | --- | --- |
| `recruitment-agent` | Local-first AI recruiting decision-support platform with FastAPI, PostgreSQL, LangGraph, LM Studio, and Next.js. | `ai-backend`, `fastapi`, `python`, `langgraph`, `langchain`, `ai-agents`, `agentic-workflows`, `postgresql`, `docker`, `local-llm`, `human-in-the-loop`, `structured-output` |
| `AliEslah` | Profile README for Ali Eslah, AI Backend Engineer. | `github-profile`, `portfolio`, `ai-backend` |
| `subtitle-translator` | Python CLI experiment for batch subtitle translation to Persian. | `python`, `cli`, `automation`, `subtitles`, `translation` |
| `courses` | Course notebooks and slides for Python, pandas, NumPy, and machine learning. | `python`, `pandas`, `numpy`, `machine-learning`, `jupyter-notebook` |
| `exchange` | Do not prioritize metadata unless kept public. | If kept public: `django`, `learning-project`, `wallet`, `archive` |
| `Cv` | Do not prioritize metadata unless rebuilt as a sanitized portfolio site. | If rebuilt: `portfolio`, `django`, `resume` |

## High-Value Issue Drafts

Issues were not created because GitHub CLI is not authenticated locally. These are the recommended issue drafts to create manually or after `gh auth login`.

| Repository | Title | Labels |
| --- | --- | --- |
| `recruitment-agent` | Add GitHub Actions CI for backend and frontend checks | `portfolio`, `ci`, `backend` |
| `recruitment-agent` | Add architecture diagram and concise system overview | `portfolio`, `documentation`, `ai` |
| `recruitment-agent` | Add repository topics and public description | `portfolio`, `cleanup` |
| `AliEslah` | Publish refreshed AI Backend Engineer profile README | `portfolio`, `documentation` |
| `subtitle-translator` | Convert subtitle translator into a tested Python CLI | `portfolio`, `cleanup`, `good-first-task` |
| `subtitle-translator` | Update dependencies, README setup, and `.gitignore` | `documentation`, `cleanup`, `security` |
| `Cv` | Decide whether to make private or replace with sanitized portfolio repo | `cleanup`, `security` |
| `exchange` | Decide whether to archive or make private | `cleanup`, `security` |

## Manual Actions Still Required

- Authenticate GitHub CLI if you want this branch pushed and a PR opened.
- Approve or reject archive/private actions for `Cv`, `exchange`, and `courses`.
- Update repository descriptions and topics in GitHub settings.
- Pin `recruitment-agent` on the profile.
- Create the high-value issues above if you want GitHub-tracked follow-up work.
- Review whether old public databases or personal documents need removal from history. If any real secrets or sensitive data were committed, use a proper secret-removal process and rotate credentials.
