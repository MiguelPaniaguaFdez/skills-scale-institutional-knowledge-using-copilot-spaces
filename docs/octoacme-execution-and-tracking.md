# OctoAcme — Execution & Tracking

## Purpose
Guidance for managing day-to-day execution and tracking progress toward project milestones.

## Team Rhythm
- Daily standups (15 min) — focus on progress, blockers, dependencies
- Weekly delivery sync — show progress, updates, and flagged risks
- Demo/Review at the end of each sprint or milestone

## Workflows
- Use the project board (e.g., GitHub Projects) with columns: Backlog, Ready, In Progress, In Review, QA, Done
- Pull Request workflow:
  - Small PRs (<= 400 lines when possible)
  - Include issue link and acceptance criteria in PR description
  - Run automated tests and linting in CI before requesting review
  - Require at least one approval before merging (or team-defined policy)

## Quality & Testing
- Unit tests for new logic
- Integration tests where applicable
- End-to-end smoke tests for critical flows before release
- Security scanning in CI
- Manual QA for feature acceptance when needed

## Reporting & Metrics
- Track velocity and burndown
- Monitor success metrics identified in the Project One-pager
- Use dashboards for key signals (errors, latency, usage)

## Blocker Escalation
- Level 1: Team-level triage in daily standup
- Level 2: PM escalates to Product Lead and dependent teams
- Level 3: Sponsor-level escalation for business-impacting issues

## Daily Standup Template
Each team member shares:
- **Yesterday**: What did I complete?
- **Today**: What am I working on?
- **Blockers**: What's preventing progress?
- **Dependencies**: Do I need anything from teammates?

Keep updates brief (2 minutes max per person). Document blockers in project board for tracking.

## Sprint Review/Demo Template
**Sprint Goal**: [What was the sprint objective?]

**Completed Work**:
- [Story/Feature 1]: Brief demo and acceptance criteria met
- [Story/Feature 2]: Brief demo and acceptance criteria met

**Incomplete Work**:
- [Story/Feature X]: Current status and reason (to be carried over or re-prioritized)

**Metrics**:
- Velocity: [X story points completed]
- Burndown: [On track / Behind]
- Quality: [Test coverage, defects found/fixed]

**Feedback**: [Stakeholder input and questions]  
**Next Sprint Preview**: [What's coming up next]

## Execution Checklist
- [ ] Branching and PR conventions documented in repo
- [ ] CI configured for tests and lint
- [ ] Regular demos scheduled (sprint reviews, milestone showcases)
- [ ] Risk register updated weekly
- [ ] Deployment pipeline and environments ready
- [ ] Monitoring and alerting configured for key metrics
- [ ] Documentation updated alongside feature development
- [ ] Design assets and specs accessible to developers
- [ ] Test automation integrated into CI/CD pipeline
- [ ] Team velocity and burndown tracked in project board
