<!-- SPDX-License-Identifier: Apache-2.0
     https://www.apache.org/licenses/LICENSE-2.0 -->

Title: Add client helper to the widget adapter

Diff:

```diff
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
+
+def get_client():
+    raise FeatureUnavailable("client support is not installed")
```

Published package metadata:

- `FeatureUnavailable` is first exported by `compat-core` 1.12.0.
- The supplied metadata covers `query-base` 1.32.0 only; that version
  declares the mandatory dependency `compat-core>=1.12.0`.
- Metadata for later `query-base` versions permitted by the direct
  requirement was not supplied, so their transitive constraints are unknown.
- No concrete supported resolution lacking `FeatureUnavailable` has been
  demonstrated.
