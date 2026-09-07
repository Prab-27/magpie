<!-- SPDX-License-Identifier: Apache-2.0
     https://www.apache.org/licenses/LICENSE-2.0 -->

## Dependency and release policy loaded from the trusted base revision

- Packages are released independently.
- When a direct dependency range conflicts with a mandatory transitive path and changed code uses an API introduced at that transitive lower bound, update the direct requirement to that lower bound and remove any obsolete upper cap.
