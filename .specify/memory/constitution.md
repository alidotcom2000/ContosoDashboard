<!-- Sync Impact Report: Version change: n/a -> 1.0.0 | Modified principles: n/a -> I. Learning-First Security, II. Offline-First Architecture, III. Test-First Change Discipline, IV. Access-Control and Data Isolation, V. Simplicity and Maintainability | Added sections: Training and Delivery Standards; Review and Quality Gates | Removed sections: none | Deferred: none -->

# ContosoDashboard Constitution

## Core Principles

### I. Learning-First Security
This project MUST treat security as a teaching tool and as a required product constraint. Every protected page, service method, and data access path MUST enforce authentication and authorization checks before exposing data or actions. The application MUST avoid claims that exceed its training scope, and all mock security behavior MUST be clearly labeled as educational rather than production-ready.

Rationale: The repository is explicitly a training application. Security boundaries protect the learning experience and ensure the code demonstrates defensible patterns without implying production readiness.

### II. Offline-First Architecture
The project MUST remain functional without external cloud dependencies for day-to-day learning and local execution. New features MUST favor local, deterministic implementations and interfaces that permit future migration to Azure services without rewriting business logic. Any cloud-ready abstraction MUST preserve the current offline-first default for teaching, demo, and local development.

Rationale: The project is designed for training in constrained environments. Offline-first development keeps the app reproducible while still demonstrating a path to Azure-hosted production patterns.

### III. Test-First Change Discipline
Any change to behavior, security, routing, or data access MUST begin with a failing test or equivalent validation step that captures the intended requirement before implementation. Production code MUST NOT be changed solely to satisfy a passing test without a documented behavior change. Regressions MUST be fixed before new work proceeds.

Rationale: A training project benefits from visible discipline that connects requirements to proof. Test-first work prevents unverified changes and reinforces the learning objective of disciplined engineering.

### IV. Access-Control and Data Isolation
Each user, team, project, and task view MUST respect the least-privilege boundary defined by role membership and data ownership. Services MUST validate both authorization and object ownership before returning or mutating records. The application MUST reject direct object references, cross-user access, and unauthorized role escalation paths.

Rationale: User isolation is a central learning objective for this project. The app demonstrates secure data boundaries and protects the integrity of the training scenario from unsafe assumptions.

### V. Simplicity and Maintainability
The project MUST prefer clear names, small responsibilities, and explicit boundaries between UI, business logic, data access, and security rules. New code MUST avoid unnecessary abstraction, duplicate logic, or hidden dependencies. Feature work MUST remain understandable to learners and maintainable by future contributors without introducing broad, fragile refactors.

Rationale: This codebase is educational and intentionally simplified. Simplicity is a quality attribute that increases clarity, reduces accidental complexity, and supports teaching by example.

## Training and Delivery Standards

The project MUST continue to align with the educational goals described in the repository documentation:

- The application MUST remain a training sandbox, not a production specification.
- Features MUST document whether they are mock, local-only, or Azure-ready.
- Security features MUST be accurate about scope and limitations instead of implying enterprise readiness.
- Data models and services MUST separate business rules from infrastructure details where practical.
- The codebase MUST remain approachable for developers learning Spec-Driven Development, Blazor, and secure application patterns.

## Review and Quality Gates

All changes MUST be reviewed against the principles in this constitution before merge or completion. Reviewers MUST verify that:

- Security checks are explicit and enforced.
- Data access respects user and role boundaries.
- New or changed behavior has evidence through tests or validation steps.
- The implementation remains simple, understandable, and consistent with the training objective.
- Documentation reflects any operational limits, migration paths, or true production gaps.

## Governance

This constitution supersedes inconsistent local practices for this repository. Amendment requires a clear reason, explicit documentation of the change, and a version bump in accordance with the versioning policy below. Any governance change affecting security, access control, or learning expectations MUST be reviewed before being accepted.

All changes MUST be documented in the project history and must preserve a clear record of why the governing rule changed. If a future rule conflicts with this constitution, this constitution governs until amended.

**Version**: 1.0.0 | **Ratified**: 2026-09-11 | **Last Amended**: 2026-09-11
