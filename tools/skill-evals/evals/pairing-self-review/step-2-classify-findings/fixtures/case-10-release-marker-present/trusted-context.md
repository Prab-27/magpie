<!-- SPDX-License-Identifier: Apache-2.0
     https://www.apache.org/licenses/LICENSE-2.0 -->

## Dependency and release policy loaded from the trusted base revision

- Packages are released independently.
- Contributors must not change inter-package lower bounds directly.
- When changed code starts using a newer API from another package, add the exact comment `# use next version` to that direct dependency.
- Release preparation updates the lower bound and removes the marker.
