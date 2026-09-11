Platform engineer building distributed ingestion services in TypeScript.

## @christisonchrissy

I build ingestion APIs, queue-backed workers, and migration-safe storage layers for high-volume event pipelines.
I own boundary validation, schema evolution, retry behavior, and the operational path from deploy to incident review.
I prioritize bounded queues, idempotent consumers, structured traces, and recoverable failures over temporary throughput.
I accept duplicated writes and temporary lag when they make recovery explicit and deployments reversible.

### 🛠 Tech & Infrastructure

**Core** — `TypeScript`, `Node.js`, `REST`, `gRPC`

**Data** — `PostgreSQL`, `Kafka`, `Redis`

**Infra** — `Kubernetes`, `OpenTelemetry`

**Tooling** — `Docker`, `GitHub Actions`

### ⚙️ Engineering Areas

- Designing idempotent event consumers with stable keys, replay tools, and bounded retry queues.
- Versioning PostgreSQL schemas and Kafka contracts behind compatibility checks and rollback plans.
- Tracing RPCs and worker spans across APIs, queues, indexes, and cache lookups.
- Tuning backpressure between ingestion bursts, durable storage, and downstream consumers.

### 🔭 Current Focus


- Moving large Kafka batches into bounded PostgreSQL writes without losing the replay window.
- Making migration compatibility explicit for schemas consumed by multiple worker versions.
- Adding traces that separate queue delay, database latency, and application work.
- Reducing retry fan-out while keeping dead-letter handling deterministic.

### 📌 Engineering Notes

- Tests should cover boundary failures, not only the happy path through an API.
- Schema boundaries belong at the queue, worker, and database edges.
- Migrations need a rollback path before they need a larger index.
- Retries without an idempotency key turn a transient failure into a data problem.

### 🧭 How I Work


- Prefer a small, observable contract over a broad abstraction.
- Make failure recovery part of the deployment, not an on-call improvisation.

_I keep systems boring enough to operate and explicit enough to repair._

[Email](mailto:christisonchrissy@gmail.com)