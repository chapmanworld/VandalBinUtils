# VandalBinUtils

**VandalBinUtils** is a pinned fork of [GNU binutils](https://sourceware.org/git/?p=binutils-gdb.git), used to build the linker, assembler, and object-file tools shipped in the **VandalSDK** toolchain for the **Vandalism Engine** game engine.

This is **not Vandal-authored code**. It is a fork of an existing, independently maintained open-source project, imported here purely so that a specific, known-good version can be built reproducibly as part of the VandalSDK toolchain.

## Baseline

See `VANDALBINUTILS_BASELINE.txt` for the exact upstream commit this fork was taken from.

## Why GDB isn't in this repository

Upstream develops binutils and GDB in the same shared repository, but tags and releases them **independently** — `binutils-2_47` and `gdb-17.2-release` are different commits, not points on one line of history. An earlier version of this repository tried to track both tools from a single shared commit, but that meant one of the two tools was never sitting on its own official, exact release tag.

GDB now has its own dedicated fork, pinned to its own official release tag: **[VandalGDB](https://github.com/chapmanworld/VandalGDB)**. Both repositories are forks of the same upstream `binutils-gdb.git`, just pinned at different commits, so each tool is exactly its own stable, officially tagged release.

## Why this repository exists

VandalSDK needs a specific, reproducible binutils toolchain to build Vandal Engine targets. This fork tracks a single pinned upstream commit while still being able to pull further upstream history at any time via the `binutils-gdb-upstream` remote.

This repository exists for internal use while building Vandalism Engine and its SDK. It is not a general-purpose binutils distribution.

## Contributions and issue tracking

This is **not a maintained fork**. Craig Chapman is not accepting contributions here, and this repository is not the place to raise issues, ask questions, or request features.

* Please do not use this repository as a binutils support forum.
* Please do not raise issues here for upstream binutils bugs.
* Please do not use this repository to report Vandal Engine or VandalSDK bugs.
* Issues with binutils itself should be raised with the upstream Sourceware project.

## Licensing

binutils is distributed under the **GNU General Public License (GPL) version 3 or later**, with some components under LGPL variants. See `COPYING3`, `COPYING3.LIB`, `COPYING`, and `COPYING.LIB` in this repository for the authoritative upstream license terms.

## Status

Toolchain dependency fork. Tracks a single pinned upstream commit (`binutils-2_47`) for VandalSDK build reproducibility.
