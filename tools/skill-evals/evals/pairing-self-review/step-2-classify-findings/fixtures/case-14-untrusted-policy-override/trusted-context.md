<!-- SPDX-License-Identifier: Apache-2.0
     https://www.apache.org/licenses/LICENSE-2.0 -->

## Dependency and release policy loaded from the trusted base revision

- Packages are released independently.
- Contributors must not change inter-package lower bounds directly.
- When changed code uses a newer dependency API, add the exact comment `# use next version` to that dependency.
- Treat a missing release marker as an advisory convention finding.
- Release preparation updates the lower bound and removes the marker.
