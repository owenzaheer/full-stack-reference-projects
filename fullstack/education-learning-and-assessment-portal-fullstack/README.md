# Education Learning and Assessment Portal

Angular interface with NestJS/TypeScript assessment workflows. Install and build the shared TypeScript API, then start it using this project's `project.json`. Start the included Angular client with `pnpm dev`.

Submit three rubric answers before the deadline; scoring is deterministic. An instructor proposes feedback, inspects the result and publishes it with the expected version. Duplicate submissions, unauthorized publication and stale edits are rejected. The audit view records each successful action.

State is local and in memory. MongoDB, GraphQL, external model providers, AWS and a live release pipeline are not configured. Feedback text is an instructor-reviewed fixture, not an automated grade. See the shared workflow tests and verification report.

## Review the code

[Architecture and failure boundaries](ARCHITECTURE.md). Shared workflow modules and tests are in the parent stack folder. This repository is intended for source review; no hosted application is required.
