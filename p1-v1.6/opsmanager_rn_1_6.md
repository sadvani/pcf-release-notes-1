---
title: Pivotal Cloud Foundry&reg; Ops Manager v1.6 Release Notes
owner: Ops Manager
---
## v1.6.13 patch release:
Patches USN-2959-1, USN-2957-1, USN-2949-1, USN-2943-1, and USN-2935-2. Additional info can be found at https://pivotal.io/security.

## v1.6.12 patch release:
Ops Manager 1.6.12 includes a fix for Ubuntu Security Notice USN-2932-1. (Embedded stemcell 3146.10, Ops Manager build 2981f)

## v1.6.11 patch release:
Ops Manager 1.6.11 includes a fix for Ubuntu Security Notice USN-2910-1. (Embedded stemcell 3146.9, Ops Manager build 567cac)

## v1.6.10 patch release:
Ops Manager 1.6.10 includes a fix for Ubuntu Security Notice USN-2900-1 for CVE-2015-7547. (Embedded stemcell 3146.8, Ops Manager build 8d3baac)

## v1.6.9 patch release:
Ops Manager 1.6.9 includes a fix for Pivotal CVE-2016-0883, Ubuntu Security Notice USN-2882-1, USN-2879-1, USN-2875-1, and USN-2874-1. (Embedded stemcell 3146.6, Ops Manager build 1468ac3)

## v1.6.8 patch release:
Ops Manager 1.6.8 includes patches for Ubuntu Security Notice USN-2870-2. (Embedded stemcell 3146.5, Ops Manager build b69cad)

## v1.6.7 patch release:
Ops Manager 1.6.7 includes patches for Ubuntu Security Notice USN-2869-1. (Embedded stemcell 3146.3, Ops Manager build 234cf4d)

## v1.6.6 patch release:
Ops Manager 1.6.6 includes patches for Ubuntu Security Notice USN-2857-1. (Embedded stemcell 3146.2, Ops Manager build 236fca1)

## v1.6.5 patch release:
Ops Manager 1.6.5 includes patches for a bug that can render important information in log files as a series of asterisks. (Embedded stemcell 3146 - same as 1.6.4, Ops Manager build c79b317)

## v1.6.4 patch release:
Ops Manager 1.6.4 includes patches for Ubuntu Security Notices USN-2821 and USN-2820-1. (Embedded stemcell 3146, Ops Manager build 511c28f)

## v1.6.3 patch release:
Ops Manager 1.6.3 includes patches for Ubuntu Security Notices USN-2815-1, USN-2812-1 and USN-2810-1.  (Embedded stemcell 3144, Ops Manager build c47f94)

## v1.6.2 patch release:
Ops Manager 1.6.2 includes patches for Ubuntu Security Notices USN-2806-1 and USN-2798-1.  (Embedded stemcell 3130, Ops Manager build 6042e5)

## v1.6.1 patch release:
Ops Manager 1.6.1 is the security patch rollup for November 2015.  (Embedded stemcell 3112)

## Version 1.6.0 (changes since v1.5.5)

### Major Features

* EBS encryption is now available for AWS deployments. This enables AWS customers to have encrypted data at rest on persistent disks.

### API Changes
* Previously, Ops Manager provided an API endpoint called `/api/users` that allowed for the creation of multiple user accounts, though only the first one was functional. To correct this, `/api/users` has been replaced by `/api/setup` that provides the same functionality for creating the first user, but does not attempt to create secondary, tertiary, etc., users, since these user accounts would not be functional. Please see API documentation at `http://your-ops-man-ip/docs` for more information. **Please note that the API is not officially supported and may change without warning in the future.**

### Security Features

* Multiple CVE fixes per [pivotal.io/security](http://pivotal.io/security).
* VM passwords are now scrubbed from the output logs and replaced with asterisks.

### Minor Features

* On vSphere, the operator is now able to split availability zones by resource pool in the same cluster.

### Bug Fixes

* Credentials no longer shows incorrect credentials when "Use default BOSH password" is selected.
* Upgrades no longer fail if product version contains a dash.
* A migration that exists but is null no longer results in a 500 error.

### Product Author Features

* New product author documentation has been made available here: http://docs.pivotal.io/pivotalcf/packaging/index.html

### Notes
Embedded stemcell in 1.6.0 is 3100
