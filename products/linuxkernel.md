---
title: Linux Kernel
permalink: /linux
category: os
iconSlug: linux
releasePolicyLink: https://www.kernel.org/
releaseImage: https://upload.wikimedia.org/wikipedia/en/timeline/ebiqfbdzyuxdbre7104smcbs2skj37k.png
changelogTemplate: |
  https://kernelnewbies.org/Linux___RELEASE_CYCLE__
activeSupportColumn: false
releaseDateColumn: true
releaseColumn: true
sortReleasesBy: 'cycleShortHand'
versionCommand: uname -r
auto:
# Note that we're tracking the linux kernel stable tree, not torvalds' tree
# which doesn't contain all tags
-   git: https://github.com/gregkh/linux.git
    regex: ^v(?<major>0|[1-9]\d*)\.(?<minor>0|[1-9]\d*)(\.(?<patch>0|[1-9]\d*))?$

releases:
-   releaseCycle: "5.18"
    cycleShortHand: 518
    eol: false
    latest: "5.18.12"
    latestReleaseDate: 2022-07-15

    releaseDate: 2022-05-22
-   releaseCycle: "5.17"
    cycleShortHand: 517
    eol: true
    latest: "5.17.15"
    latestReleaseDate: 2022-06-14

    releaseDate: 2022-03-20
-   releaseCycle: "5.16"
    cycleShortHand: 516
    eol: 2022-04-13
    latest: "5.16.20"
    latestReleaseDate: 2022-04-13

    releaseDate: 2022-01-09
-   releaseCycle: "5.15"
    cycleShortHand: 515
    eol: 2023-10-31
    lts: true
    latest: "5.15.55"
    latestReleaseDate: 2022-07-15

    releaseDate: 2021-10-31
-   releaseCycle: "5.10"
    cycleShortHand: 510
    eol: 2026-12-01
    lts: true
    latest: "5.10.131"
    latestReleaseDate: 2022-07-15

    releaseDate: 2020-12-13
-   releaseCycle: "5.4"
    cycleShortHand: 504
    eol: 2025-12-01
    lts: true
    latest: "5.4.206"
    latestReleaseDate: 2022-07-15

    releaseDate: 2019-11-24
-   releaseCycle: "4.19"
    cycleShortHand: 419
    eol: 2024-12-01
    lts: true
    latest: "4.19.252"
    latestReleaseDate: 2022-07-12

    releaseDate: 2018-10-22
-   releaseCycle: "4.14"
    cycleShortHand: 414
    eol: 2024-01-01
    lts: true
    latest: "4.14.288"
    latestReleaseDate: 2022-07-12

    releaseDate: 2017-11-12
-   releaseCycle: "4.9"
    cycleShortHand: 409
    eol: 2023-01-01
    lts: true
    latest: "4.9.323"
    latestReleaseDate: 2022-07-12
    releaseDate: 2016-12-11

---

> The Linux kernel is a free and open-source, monolithic, modular, multitasking, Unix-like operating system kernel.
Linux is deployed on a wide variety of computing systems, such as embedded devices, mobile devices (including Android), personal computers, servers, mainframes, and supercomputers.

There are several main categories into which kernel releases may fall:

- **Prepatch or "RC"** kernels are mainline kernel pre-releases that are mostly aimed at other kernel developers and Linux enthusiasts. They must be compiled from source and usually contain new features that must be tested before they can be put into a stable release.

- **Mainline tree**  It's the tree where all new features are introduced and where all the exciting new development happens. New mainline kernels are released every 2-3 months.    

- **Stable** is labeled after each mainline kernel is released. Any bug fixes for a stable kernel are backported from the mainline tree. There are usually only a few bugfix kernel releases until next mainline kernel becomes available -- unless it is designated a "longterm maintenance kernel". Stable kernel updates are released on as-needed basis, usually once a week.
        
- **Longterm (LTS)** are usually several longterm maintenance kernel releases provided for the purposes of backporting bugfixes for older kernel trees. By default these are only supported for two years (as opposed to the 4 months of a non-LTS release) [but are usually extended depending on how long companies pledge to back it.](https://lore.kernel.org/lkml/YA%2FE1bHRmZb50MlS@kroah.com/) Only important bugfixes are applied to such kernels and they don't usually see very frequent releases, especially for older trees.
