<!--
Generated from canonical UltraShip state. Do not edit directly.
Run `ultraship views` to regenerate.
-->
# Active releases

## ultraship 0.5.0

**Execution state:** DEVELOPING
**Release fit:** probable
**Target mode:** published
**Outcome:** Declare their project's deploy or publish command for a target mode, and have /ultraship:complete run it, capture its real stdout, stderr, and exit code, and record that as verified deployment evidence. A release then reaches staging-deployed, production-deployed, or published because the command actually ran and succeeded — not because an agent typed the claim. When the command exits non-zero, completion records the failure and the release stays release-ready, so a deployed mode is never asserted without proof.



_Canonical sources: products/<id>/execution/active.yaml, products/<id>/releases/<version>.yaml_
