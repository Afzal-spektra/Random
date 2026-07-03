# Cisco ASA Firewall — VPN & Monitoring (Lab 02)

Welcome to your Cisco ASA firewall hands-on skills assessment. This environment gives you a live Cisco ASAv firewall, a remote IPsec peer, and a Linux jump host to work from. Read this page, then move to **Exercise 1** to begin.

### Overall Estimated timing: 90 Minutes

## Overview

In this assessment you act as the **network security engineer** responsible for a Cisco ASA firewall that must connect your site to a remote site over an encrypted **Site-to-Site IPsec VPN**, and must give the operations team **session, connection, and VPN visibility**. You will build the VPN from the ground up — crypto map, IKE/IPsec policy, and the object groups that define interesting traffic — then turn on monitoring, enable active-connection tracking, and finish by binding the crypto map to the outside interface so the tunnel can be verified and troubleshot. You are graded on the **running configuration of the live Cisco ASAv**.

## Objectives

By the end of this assessment you will have:

1. **Configured a Site-to-Site IPsec VPN** — a crypto map and an L2L tunnel-group pointing at the remote peer.
2. **Defined the IKE and IPsec parameters** — a Phase 1 IKE policy and a Phase 2 transform-set.
3. **Created object groups** for the VPN's local and remote networks and referenced them in the crypto ACL.
4. **Enabled session and connection monitoring** through logging.
5. **Enabled active-connection tracking** with threat-detection and/or connection settings.
6. **Completed the VPN** by binding the crypto map to the outside interface so it can be troubleshot.

## Pre-requisites

Working knowledge of Cisco ASA administration: the ASA CLI (`enable`, `configure terminal`, `write memory`), Site-to-Site IPsec VPN concepts (crypto maps, tunnel-groups, IKE/ISAKMP policies, transform-sets), object groups and access-lists, ASA logging, threat-detection, and the `show crypto` family of troubleshooting commands.

## Getting Started with the lab

Your virtual machine and this **Guide** are available within your web browser. Use the **Split Window** button at the top-right to open the guide beside your terminal.

## Accessing Your Lab Environment

1. Connect to the Lab (jump) VM over SSH using the details on the **Environment** tab.

    - **SSH command:** see the **LABVM SSH Command** output on the **Environment** tab
    - **Username:** see the **LABVM Admin Username** output on the **Environment** tab
    - **Password:** see the **LABVM Admin Password** output on the **Environment** tab

1. From the jump host, connect to the **Cisco ASAv** firewall to configure it:

    - **SSH command:** `ssh cisco@10.0.0.5`
    - **Username:** `cisco`
    - **Password:** `Cisco@1234`
    - Then enter privileged mode with `enable` and `configure terminal` to apply configuration.

1. Your environment id for this run is **<inject key="DeploymentID" enableCopy="false"/>** — quote it if you contact support.

## Track Your Progress

Use the **Validate** button on each task to check your work. The **Progress** tab shows your validation score; it reaches 100% when all six task validations pass.

## Support Contact

The CloudLabs support team is available 24/7 via email and live chat.

- Email Support: labs-support@spektrasystems.com
- Live Chat Support: https://cloudlabs.ai/labs-support

Click **Next** to begin Exercise 1.

## Happy Assessing !!
