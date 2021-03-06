---
title: MySQL for PCF v1.2.0.0 Release Notes
owner: MySQL
---

## Changes since v1.1.0.0:

* Service renamed to 'MySQL for Pivotal CF'
* Plan attributes are configurable
    * Max Storage per database
    * Max Concurrent Connections per user
    * Max databases
* Plan name is determined dynamically based on configured storage quota
* Plan features include disclaimer that the service is not for production use
* API changes:
    * Dashboard url returned on instance creation.
* New UI for Service Instance Dashboard:
    * Styled dashboard shows instance storage usage.
    * Includes warning when quota has been surpassed.
    * Uses new SSO feature in Cloud Controller API. User must approve `openid` and `cloud_controller.read` scopes for UI to work. (Scope approvals can be updated at any time.)
* Security Upgrades:
    * Updated Rails.
    * Prevention of SQL injection.
* Broker is available via URL (rather than by IP). Typically has the format `https://p-mysql.<cf-domain>`.
* Supports clustered NATS.
* Displayed plan name is configurable at deploy time.
* Bosh errands can be used to register and deregister the broker, and to run tests that verify the deployment.
* Improved logging in service broker

## The following components will be re-deployed:

* cf-mysql-broker
* mysql

## The release includes new components (all used to run Bosh errands):

* broker-registrar
* broker-deregistrar
* acceptance-tests
