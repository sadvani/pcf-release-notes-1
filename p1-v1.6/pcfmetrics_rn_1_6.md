---
title: Pivotal Cloud Foundry&reg; Metrics Release Notes
owner: Metrix
---

## Version 1.0.4

### Known issues
For Known Issues, please see [PCF Metrics Known Issues](../p1-v1.6/pcfmetrics_ki_1_6.html).

### Notes
* Update to use Stemcell 3146.11
* Change list of apps available to a user and prevent overload of Cloud Controller API
* The route for the PCF Metrics application is registered as `metrics.<system-domain>` in this v1.0.4 release.   The application can be accessed at `https://metrics.<system-domain>`
* The install will create a small deployment suitable for hundreds of apps. This is not configured for thousands of apps.

## Version 1.0.3

### Known issues
For Known Issues, please see [PCF Metrics Known Issues](../p1-v1.6/pcfmetrics_ki_1_6.html).

### Notes
* Updated to use stemcell 3146.5
* This beta requires Elastic Runtime v1.6.16 or greater. 
* The route for the PCF Metrics application is registered as `metrics.<system-domain>` in this v1.0.3 release.   The application can be accessed at `https://metrics.<system-domain>`
* The install will create a small deployment suitable for hundreds of apps. This is not configured for thousands of apps.
