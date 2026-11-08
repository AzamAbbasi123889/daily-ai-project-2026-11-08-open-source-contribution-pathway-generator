# Implementation Checklist

Build the application yourself using `PROJECT_BRIEF.md`.

## Initial setup

- [ ] Read the project specification.
- [ ] Review the architecture and data model.
- [ ] Create a Python virtual environment.
- [ ] Install and pin the required dependencies.
- [ ] Configure credentials through environment variables.
- [ ] Review the data privacy and security requirements.

## Project acceptance criteria

- [ ] User can upload a .txt/.pdf or fill a form
- [ ] Extracted skills appear as distinct nodes in the graph
- [ ] Each skill node has an embedding stored in pgvector
- [ ] Top‑5 projects returned within 5 seconds
- [ ] Each project includes repo name, stars, primary language, and relevance score
- [ ] Generated markdown includes: selected issue link, step‑by‑step actions, code snippet placeholders, and checklist
- [ ] Roadmap is persisted and retrievable via a unique ID
- [ ] User can close the browser and retrieve the same roadmap after 24 h
- [ ] State updates (e.g., after completing a step) reflect in the graph
- [ ] Initialize repo, Docker, CI
- [ ] Design Postgres schema + pgvector
- [ ] Implement JWT auth
- [ ] Create LangChain prompt chain
- [ ] Integrate OpenAI embedding model
- [ ] Store skill nodes
- [ ] Build GitHub search agent
- [ ] Define relevance scoring logic
- [ ] Implement Roadmap agent (markdown generation)
- [ ] Wire CrewAI orchestrator
- [ ] Persist roadmaps in LangGraph
- [ ] Add Redis caching
- [ ] Create minimal React page to view roadmap
- [ ] Write unit & integration tests
- [ ] Run OWASP‑ASVS checklist for token handling
- [ ] Docker‑Compose production stack, GitHub Actions CI/CD
- [ ] Pytest unit tests for each FastAPI route (status codes, schema validation)
- [ ] Mocked GitHub responses to verify Repo‑Search scoring logic
- [ ] LangGraph state rollback tests (add/remove skill nodes)
- [ ] CrewAI orchestration integration test with deterministic LLM responses (using OpenAI’s test mode)
- [ ] Security test: ensure JWT token is not logged and GitHub PAT is stored only in env
- [ ] Load test with locust for /recommendations endpoint
- [ ] Dockerfile builds slim python:3.11‑slim image; multi‑stage for dependencies
- [ ] docker‑compose.yml defines services: api, postgres, redis, supabase‑studio (optional)
- [ ] GitHub Actions workflow: lint → unit tests → build image → push to Docker Hub → Deploy to Railway (free tier) on push to main
- [ ] Environment variables: OPENAI_API_KEY, GITHUB_PAT, JWT_SECRET, DATABASE_URL
- [ ] Enable HTTPS via Railway/Render automatic TLS

## Before completion

- [ ] Implement the planned MVP features.
- [ ] Add unit and integration tests.
- [ ] Run the test suite.
- [ ] Measure the evaluation metrics in the brief.
- [ ] Record actual results and known limitations.
- [ ] Document setup and deployment.
- [ ] Update the README to reflect the implemented features.
- [ ] Add only verified outcomes to your resume.
