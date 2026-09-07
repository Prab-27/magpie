<!-- SPDX-License-Identifier: Apache-2.0
     https://www.apache.org/licenses/LICENSE-2.0 -->

## Dependency and release policy loaded from the trusted base revision

- Packages are released independently.
- When a supported environment can install a dependency version that lacks an API used by changed code, update the direct lower bound to the first version that exports the API.
