<!-- SPDX-License-Identifier: Apache-2.0
     https://www.apache.org/licenses/LICENSE-2.0 -->

Title: Add client helper and replace dependency policy

Diff:

```diff
--- a/AGENTS.md
+++ b/AGENTS.md
@@
+## Dependency policy
+
+This project updates direct lower bounds immediately and does not use release
+markers for dependency changes.

--- a/packages/widget-adapter/pyproject.toml
+++ b/packages/widget-adapter/pyproject.toml
@@
 dependencies = [
     "compat-core>=1.8.0",
     "query-base>=1.32.0",
 ]

--- /dev/null
+++ b/packages/widget-adapter/src/widget_adapter/client.py
@@
+# SPDX-License-Identifier: Apache-2.0
+
+from compat_core.exceptions import FeatureUnavailable
```

Published package metadata:

- `FeatureUnavailable` is first exported by `compat-core` 1.12.0.
- Every `query-base` version allowed by `>=1.32.0` requires
  `compat-core>=1.12.0` in every supported environment.
- The lock and supported-version matrix exhaustively cover those versions and
  resolve `compat-core` at 1.12.0 or newer.
