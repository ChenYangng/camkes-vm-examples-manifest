<!--
     Copyright 2018, Data61, CSIRO

     SPDX-License-Identifier: CC-BY-SA-4.0
-->

CAmkES VM Examples Manifest
===========================

The CAmkES VMM is a Virtual Machine Monitor that utilizes the CAmkES component platform.
Due to the static nature of CAmkES systems the VMM is specified at build time to run
on a particular hardware platform. Currently the VMM is mostly targeted to run on the
C162 platform from Aitech. There is also a configuration for running on generic x86
machines, but it has almost no hardware support.

This project fetches example CAmkES VM applications to build and use. These being optiplex9020, minimal and cma34cr\_centos.

For general instructions on how to use this repository, see [docs.seL4.systems](https://docs.sel4.systems/GettingStarted.html).

For general information about CAmkES see [the CAmkES pages on docs.seL4.systems](https://docs.sel4.systems/CAmkES/).

For detailed information about CAmkES see documentation in [the camkes-tool repo](https://github.com/seL4/camkes-tool/blob/master/docs/index.md).

For detailed information about the VM on the C162 platform see the documention in [the camkes-vm repo](https://github.com/seL4/camkes-vm/blob/master/README.md).

For detailed information about the example VM applications and how to build them see the documentation in [the camkes-vm-examples repo](https://github.com/seL4/camkes-vm-examples/blob/master/README.md).

## Build for LoongArch
```
repo init -u https://github.com/ChenYangng/camkes-vm-examples-manifest.git -b loongarch
repo sync
mkdir build
cd build
../init-build.sh -DCAMKES_VM_APP=vm_minimal -DPLATFORM=3A5000 -DLOONGARCH64=1
ninja
```
