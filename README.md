# Issue #11245: actual browser screenshots

Captured from the production DBX Web UI against disposable local MySQL 8.4.11.

- baseline-84-production.png: unchanged main 504ef7e1c6f5156b792a5a63348ce95d5db58df0, original qrtz.sql self-comparison, five tables / ten false FK differences.
- review-fix-84-self.png: source corresponding to fix commit 5dc1a5fb35212896d5b5cfe79fc6526eafcf90ce, self-comparison has zero differences.
- review-fix-84-real-diff.png: change ON DELETE only in the disposable target, one real FK difference remains detectable.
- review-fix-84-converged.png: execute the exact generated SQL in the disposable target, read native metadata and compare again, zero differences.

Images are original captures, without compositing or edits. Only dedicated test connections are visible. This evidence branch is separate from the implementation PR.
