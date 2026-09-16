# GitHub Info

## Mona's editorial angle

Mona's website focuses on practical GitHub guidance backed by official references from:

- docs.github.com
- github.blog
- github.blog/changelog

## Current homepage themes

- GitHub collaboration basics: repositories, branches, pull requests, and merges.
- GitHub Copilot as an AI coding assistant across the IDE, CLI, and GitHub.
- GitHub Actions as the automation layer behind repository workflows.
- Recent GitHub Blog and Changelog stories worth watching.

## GitHub Agentic Workflows (gh-aw)

Source: [github/gh-aw README](https://github.com/github/gh-aw)

- `gh-aw` is a GitHub CLI extension that lets developers write AI-powered repository automation in Markdown with YAML frontmatter, then compiles each workflow into a standard GitHub Actions workflow (`gh aw compile`).
- Think of it as "Actions + Agent + Safety": conventional Actions still handle deterministic builds, tests, and deploys; add an agentic workflow when a task needs reasoning, like issue triage, PR review, CI failure investigation, or documentation upkeep.
- Supports multiple AI engines (GitHub Copilot, Claude Code, OpenAI Codex, Google Gemini, Pi). Agent jobs run read-only and sandboxed by default; any GitHub writes go through validated `safe-outputs` jobs with scoped permissions — a good security-by-default pattern to point readers toward.
- Install with `gh extension install github/gh-aw`.

## Awesome Copilot workflow examples

Source: [github/awesome-copilot `workflows/`](https://github.com/github/awesome-copilot/tree/main/workflows) (backing content for awesome-copilot.github.com/workflows)

A curated set of ready-to-use `gh-aw` workflows developers can copy into their own repos:

- **OSPO Organization Health Report** — weekly report surfacing stale issues/PRs, merge-time analysis, and contributor leaderboards for a GitHub org.
- **OSPO Contributors Report** — monthly contributor activity metrics across an org's repositories.
- **OSPO Release Compliance Checker** and **OSPO Stale Repos** — automated compliance and repo-hygiene reporting for open source program offices.
- **Weekly Comment Sync** — finds stale code comments or README snippets, makes text-only fixes, and opens a draft pull request for review (a nice example of the safe-outputs pull-request pattern).
- **Daily Issues Report** and **Relevance Check/Summary** — recurring triage and relevance-scoring workflows for incoming issues.

Good starting point for readers who want to try agentic automation without writing a workflow from scratch.

## Sourcing note

This update's GitHub Agentic Workflows and Awesome Copilot content was verified directly against the `github/gh-aw` and `github/awesome-copilot` repositories via the GitHub API. Live fetches to github.blog/latest and github.blog/changelog were not reachable from this environment during this pass, so no new Blog/Changelog items are included this round — revisit those sources next update.
