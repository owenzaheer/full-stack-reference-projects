# Financial Reconciliation and Exception Workbench

Vue + FastAPI demonstration using synthetic invoices, signed callbacks and SQLite transactions. Exact payments match deterministically; partial payments enter an exception workflow. Reviewer proposals require approval and cannot overdraw balances. Audit records preserve the actor and action.

From `backend`: install the shared Python requirements and run `uvicorn app:app --host 127.0.0.1 --port 8000`. From `frontend`: run `pnpm install --frozen-lockfile`, then `pnpm dev`. Open the Vite address, choose callback and click **Sign fixture payload**, then **Run workflow**. Repeating it cannot charge the invoice again. Adjust the amount with the same event ID to observe a conflict.

The signing key and role tokens are local fixtures. No live payment provider, PostgreSQL, Redis or model service is connected. Tests in the shared Python module cover signatures, replay conflicts and concurrent approval decisions.

## Architecture

[Architecture and failure boundaries](ARCHITECTURE.md). Shared workflow modules and tests are in the parent stack folder.
