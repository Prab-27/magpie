<!-- SPDX-License-Identifier: Apache-2.0
     https://www.apache.org/licenses/LICENSE-2.0 -->

Base ref: origin/main (merge base def5678)
Files changed: 3 (1 added, 2 modified)
Diff size: 24 additions, 3 deletions

Classified findings:
  correctness:
    - blocking | packages/widget-adapter/pyproject.toml:12
      summary: Python 3.12 can install compat-core 1.8.0, which lacks FeatureUnavailable
      evidence: '+    "compat-core>=1.8.0",'
      dependency_evidence: "The direct >=1.8.0 path applies on Python 3.12 while the transitive >=1.12.0 marker is inactive. The effective intersection is >=1.8.0 with partial metadata coverage. compat-core==1.8.0 is a concrete supported failing resolution, so runtime compatibility is broken."
  security: no findings
  conventions:
    - advisory | packages/widget-extra/pyproject.toml:14
      summary: the dependency change needs the release marker required by trusted project policy
      evidence: '+    "helper-core>=2.0",'
      dependency_evidence: "The direct >=2.0 and mandatory transitive >=2.2 paths intersect at >=2.2. Lock metadata exhaustively covers supported environments and every resolved version provides the API, so the runtime graph is compatible; trusted policy still requires a release marker."
