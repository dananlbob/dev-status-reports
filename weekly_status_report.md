# Weekly Status Report

## GitHub Notifications Summary

- **Total notifications:** 0
- No pending tasks, mentions, or review requests.

## Asyncio Quick Reference

- **Purpose:** Library for concurrent code using `async`/`await` syntax.
- **High‑level APIs:**
  - Run coroutines concurrently (`asyncio.run`, `asyncio.create_task`).
  - Network I/O and IPC (`asyncio.open_connection`, streams API).
  - Subprocess management (`asyncio.create_subprocess_exec`).
  - Queues for task distribution (`asyncio.Queue`).
  - Synchronization primitives (`asyncio.Lock`, `Event`, `Barrier`).
- **Low‑level APIs:**
  - Event loop control (`asyncio.get_event_loop`, `loop.create_server`).
  - Transports & protocols for custom networking.
  - Bridging callbacks to `await` via `asyncio.Future`.
- **Best Practices:**
  - Prefer high‑level APIs; avoid direct loop manipulation unless building a framework.
  - Use `async with` for resources (locks, files via `aiofiles`).
  - Keep tasks short; handle cancellation properly.
  - Use `asyncio.run` as entry point; for long‑running services, manage the loop manually.
  - Leverage `asyncio.create_task` instead of `ensure_future` for clarity.
  - Batch I/O operations; avoid blocking calls inside coroutines.
  - Use `asyncio.gather` for parallel execution and error aggregation.
  - Employ timeouts (`asyncio.wait_for`) to prevent hangs.

*Extracted from the official Python asyncio documentation.*