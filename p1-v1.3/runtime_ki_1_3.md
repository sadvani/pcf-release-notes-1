---
title: Pivotal Elastic Runtime v1.3 Known Issues
owner: RelEng
---

* PCF Services (e.g.: MySQL for PCF, MongoDB for PCF or Pivotal HD for PCF) may lose connectivity during the upgrade of Pivotal Cloud Foundry Elastic Runtime due to an existing known issue with the Ruby BOSH Agent. Pivotal recommends that these services are upgraded to their 1.3 release versions along with the Elastic Runtime upgrade, as they include a new Go BOSH Agent that resolves the known issue. If you choose not to upgrade a service at this time and find that the installation has lost connectivity, run ``bosh cck`` against the affected VMs.
