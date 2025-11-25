# OctoAcme — Release & Deployment Guide

## Purpose
Standardize how OctoAcme releases features to production to reduce risk and improve observability.

## Release Types
- Patch: hotfixes addressing critical production issues
- Minor: incremental features and improvements
- Major: significant functionality or breaking changes

## Pre-release requirements
- All acceptance criteria met and PRs merged
- Passing CI and security scans
- Release notes drafted and reviewed
- User documentation updated (guides, API docs, help articles)
- Rollback / mitigation plan documented
- Smoke tests prepared and reviewed by QA Lead
- Performance impact assessed
- Database migrations tested (if applicable)
- Feature flags configured (if using gradual rollout)
- Monitoring and alerts configured for new features
- Support team briefed on changes and potential issues

## Deployment Checklist
- [ ] Deployment window scheduled (if needed) and stakeholders notified
- [ ] Backup or snapshot created (if applicable)
- [ ] Deploy to staging and run smoke tests
- [ ] QA sign-off on staging validation
- [ ] Deploy to production (automated pipeline preferred)
- [ ] Run post-deploy verifications (health checks, smoke tests)
- [ ] Monitor error rates, latency, and key metrics
- [ ] Verify feature flags and gradual rollout status
- [ ] Announce release to stakeholders and support team
- [ ] Update documentation with production URLs and access info
- [ ] Archive release artifacts and logs

## Rollback & Incident Playbook
- If a deployment fails or causes a critical issue:
  - Trigger incident response and notify on-call (DevOps Engineer, Tech Lead)
  - Assess severity and customer impact
  - Rollback to last known-good release if necessary
  - Communicate status to stakeholders and affected users
  - Triage root cause and capture action items
  - Schedule blameless post-mortem within 48 hours

## Rollback Decision Criteria
Rollback immediately if:
- Critical functionality is broken for majority of users
- Data integrity or security issues are detected
- Error rates exceed defined thresholds (e.g., >5% of requests)
- System performance degrades significantly (e.g., >2x latency)

Consider rollback if:
- Non-critical feature has major issues
- Workaround is complex or impacts user experience
- Fix will take >2 hours to develop and test

## Release Notes Template
**Release**: [Name / Number / Version]  
**Date**: [Date]  
**Type**: [Patch / Minor / Major]

**Summary**: [Brief overview of this release]

**New Features**:
- [Feature 1]: [Description and value to users]
- [Feature 2]: [Description and value to users]

**Improvements**:
- [Enhancement 1]: [What improved and why it matters]
- [Enhancement 2]: [What improved and why it matters]

**Bug Fixes**:
- [Fix 1]: [What was broken and how it's resolved]
- [Fix 2]: [What was broken and how it's resolved]

**Breaking Changes** (if any):
- [Change 1]: [Description, migration steps, and impact]

**Migration Steps** (if applicable):
1. [Step-by-step instructions for upgrading]
2. [Any configuration changes needed]

**Known Issues**:
- [Issue 1]: [Description and workaround if available]

**Documentation**: [Links to updated user guides, API docs, tutorials]  
**Rollback**: [Link to rollback procedure if needed]
