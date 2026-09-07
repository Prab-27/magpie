<!-- SPDX-License-Identifier: Apache-2.0
     https://www.apache.org/licenses/LICENSE-2.0 -->

Base ref: origin/main (merge base abc1234)
Files changed: 2 (1 added, 1 modified)
Diff size: 18 additions, 1 deletion

Classified findings:
  correctness:
    - blocking | packages/widget-adapter/pyproject.toml:12
      summary: Python 3.12 can install compat-core 1.8.0, which lacks FeatureUnavailable
      evidence: '+    "compat-core>=1.8.0",'
      dependency_evidence: "The direct compat-core>=1.8.0 path applies on Python 3.12 while the transitive >=1.12.0 marker is inactive there. The effective intersection is >=1.8.0 with partial metadata coverage. compat-core==1.8.0 is a concrete supported failing resolution, so runtime compatibility is broken."
  security: no findings
  conventions: no findings
