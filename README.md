# VandalBinUtils

**VandalBinUtils** is a pinned fork of [GNU binutils and GDB](https://sourceware.org/git/?p=binutils-gdb.git) — upstream develops both in one shared repository, and this fork follows that structure — used to build the linker, assembler, object-file tools, and debugger shipped in the **VandalSDK** toolchain for the **Vandalism Engine** game engine.

This is **not Vandal-authored code**. It is a fork of an existing, independently maintained open-source project, imported here purely so that a specific, known-good version can be built reproducibly as part of the VandalSDK toolchain.

## Baseline

See `VANDALBINUTILS_BASELINE.txt` for the exact upstream commit this fork was taken from, and **importantly**, for an explanation of how the single shared commit relates to the separately-tagged `binutils-2_47` and `gdb-17.2-release` upstream releases — they are not the same commit, and the tradeoff involved in picking one baseline for both tools is spelled out there.

## Why this repository exists

VandalSDK needs a specific, reproducible binutils and GDB toolchain to build and debug Vandal Engine targets. Because upstream develops both tools in one repository, this fork tracks both from a single pinned commit rather than maintaining two separate forks, while still being able to pull further upstream history at any time via the `binutils-gdb-upstream` remote.

GDB in this toolchain is built against GMP, MPFR, MPC, and ISL — see `VandalGMP`, `VandalMPFR`, `VandalMPC`, and `VandalISL` for those forks.

This repository exists for internal use while building Vandalism Engine and its SDK. It is not a general-purpose binutils/GDB distribution.

## Contributions and issue tracking

This is **not a maintained fork**. Craig Chapman is not accepting contributions here, and this repository is not the place to raise issues, ask questions, or request features.

* Please do not use this repository as a binutils or GDB support forum.
* Please do not raise issues here for upstream binutils or GDB bugs.
* Please do not use this repository to report Vandal Engine or VandalSDK bugs.
* Issues with binutils or GDB themselves should be raised with the upstream Sourceware project.

## Licensing

binutils and GDB are distributed under the **GNU General Public License (GPL) version 3 or later**, with some components under LGPL variants. See `COPYING3`, `COPYING3.LIB`, `COPYING`, and `COPYING.LIB` in this repository for the authoritative upstream license terms.

## Status

Toolchain dependency fork. Tracks a single pinned upstream commit for VandalSDK build reproducibility.
