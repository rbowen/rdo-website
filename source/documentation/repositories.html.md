---
title: RDO repositories
authors: apevec, kashyap, larsks, mangelajo, pixelbeat, pmyers, srikanth1239, strider
wiki_title: Repositories
wiki_revision_count: 20
wiki_last_updated: 2015-01-13
---

# RDO repositories

See the [Packstack quickstart](/install/quickstart/) for summarized instructions on how to interact with the repositories described in this document.

This document expands on the details of the various repositories involved.

### Enabling the Optional, Extras, and RH Common channels on RHEL

If using RHEL it's assumed that `rhel-7-server-rpms` is enabled by default. RDO also needs the `Optional`, `Extras`, and `RH Common` channels to be enabled:

    $ sudo subscription-manager repos --enable=rhel-7-server-optional-rpms

    $ sudo subscription-manager repos --enable=rhel-7-server-extras-rpms

    $ sudo subscription-manager repos --enable=rhel-7-server-rh-common-rpms

The `Optional` channel is not available for CentOS or Scientific Linux. The required packages are included in the main repositories for those distributions. `Extras` is enabled by default on CentOS 7.

An additional `kvm-common` repository is provided by the CentOS Virtualization SIG that includes enhanced builds of QEMU and supporting projects for use with RDO and oVirt. To enable the `kvm-common` repository install the [centos-release-qemu-ev]( http://mirror.centos.org/centos/7/virt/x86_64/kvm-common/centos-release-qemu-ev-1.0-1.el7.noarch.rpm) package.

### Red Hat OpenStack Platform

The separate [Red Hat OpenStack Platform](https://access.redhat.com/products/red-hat-openstack-platform/) product does **not** require the `Optional`, `Extras`, and `RH Common` channels enabled.

