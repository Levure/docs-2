---
title: 'Migrating a failover IP'
excerpt: 'Find out how to migrate a failover IP address to another instance'
slug: migrating_a_failover_ip
legacy_guide_number: g1890
section: Networking
order: 10
---

**Last updated 3rd September 2021**

## Objective

Being able to migrate IP addresses generally limits or removes the possibility that your service becomes unavailable. For example, you can effectively update a whole website to a new version or you can keep a replicated server active while running maintenance or installing updates on your production server.

**This guide explains how to migrate a failover IP from one OVHcloud Public Cloud instance to another.**

## Prerequisites

- at least two [Public Cloud instances](https://www.ovhcloud.com/en-gb/public-cloud/) in your OVHcloud account
- a failover IP address
- access to the [OVHcloud Control Panel](https://www.ovh.com/auth/?action=gotomanager&from=https://www.ovh.co.uk/&ovhSubsidiary=GB)

## Instructions

> [!warning]
>
> A failover IP cannot be moved from one zone to another. For example, an IP located in the SBG(X) data center can be moved to GRA(X) or RBX(X), but cannot be moved to BHS(X).
>

First, log in to the [OVHcloud Control Panel](https://www.ovh.com/auth/?action=gotomanager&from=https://www.ovh.co.uk/&ovhSubsidiary=GB), go to the `Public Cloud`{.action} section and select the Public Cloud service concerned. Then, select Failover IP in the “Network” section.
In our example, a failover IP is routed to "Instance_A" and we want to redirect it towards "Instance_B".

![migrating failover IP](images/failover.png){.thumbnail}

Click on `...`{.action} next to the failover IP and select `Modify associated instance`{.action}.

![migrating failover IP](images/modify.png){.thumbnail}

Choose the destination server from the list by clicking the checkbox.

![migrating failover IP](images/modify1.png){.thumbnail}

Confirm with `Attach`{.action}.

After a few seconds the Control Panel will be updated and a confirmation message will be displayed if the migration was done sucessfully.

![migrating failover IP](images/modify2.png){.thumbnail}

> [!primary]
>
The failover IP can be configured on the destination server before or after carrying out the migration. If it was preconfigured, it will begin to respond as soon as the routing operation is completed.
>

## Go further

[Configure a failover IP](../configure_a_failover_ip)

[Importing a failover IP](../import_a_failover_ip)

Join our community of users on <https://community.ovh.com/en/>.
