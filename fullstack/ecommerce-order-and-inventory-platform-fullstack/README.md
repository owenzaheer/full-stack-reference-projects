# Ecommerce Order and Inventory Platform

Next.js/React interface and Node/TypeScript route handlers with local in-memory workflow state. Install with `pnpm install --frozen-lockfile`, run `pnpm dev`, or build with `pnpm build` and run `pnpm start`.

Reserve stock using an idempotency key and expected inventory version. Operator actions cancel, ship and refund; cancellations release stock once. The outbox retains events during a simulated relay failure. Version conflicts reject stale updates. Shared TypeScript tests verify these business rules.

Storage resets when the Node service restarts. The in-memory fixture is designed for one local process and must not be deployed as a distributed transactional backend. PostgreSQL, Prisma, Redis, Kafka and Kubernetes are not connected in this reference implementation.

## Architecture

[Architecture and failure boundaries](ARCHITECTURE.md). Shared workflow modules and tests are in the parent stack folder.
