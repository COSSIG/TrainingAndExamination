[#]: subject: "CentOS Hyperscale SIG Quarterly Report for 2021Q4"
[#]: via: "https://blog.centos.org/2022/01/centos-hyperscale-sig-quarterly-report-for-2021q4/"
[#]: author: "CentOS Blog https://blog.centos.org"
[#]: collector: "lkxed"
[#]: translator: " "
[#]: reviewer: " "
[#]: publisher: " "
[#]: url: " "

CentOS Hyperscale SIG Quarterly Report for 2021Q4
======

This report covers work that happened between October 2nd and December 31st. For previous work, see the [2021Q3 report][1].

### Purpose

The [Hyperscale SIG][2] focuses on enabling CentOS Stream deployment on large-scale infrastructures and facilitating collaboration on packages and tooling.

### Membership update

Since the last update, the SIG gained two new members (Jack Aboutboul and David Duncan).

We welcome anybody that’s interested and willing to do work within the scope of the SIG to join and contribute. See the [membership][3] section on the wiki for the current members list and how to join.

### Releases and Packages

Unless otherwise specified, packages are available in our main repository, which can be enabled with `dnf install centos-hyperscale-release`. Please report any issues with these packages on our [package-bugs][4] tracker.

#### CentOS Stream 9

CentOS Stream 9 is [now available][5] and Hyperscale tags have been setup in CBS to build and release packages for it. As of now, we have released systemd and kpatch in our main repository, plus btrfs-progs and a kernel in our experimental repository. We have more packages and features targeting CentOS Stream 9 specifically [planned][6] for the near future. Going forward, we expect to continue building packages for both CentOS Stream 8 and CentOS Stream 9 in parallel.

The SIG also emphasizes contributing to CentOS Stream 9 itself whenever possible. As a result, SIG members have made several improvements to CentOS Stream 9.

The Hyperscale SIG is responsible for the following features in CentOS Stream 9, most of which have been contributed in the last quarter:

- Addition of the `systemd-oomd` package with useful default configuration
- Packaging macros for third-party NGINX modules as RPMs
- PipeWire with WirePlumber and JACK compatibility for the audio subsystem
- Wayland support for the GNOME Classic session
- `sdl12-compat` package replaced the `SDL` package
- `SDL2` upgraded with proper support for GNOME Wayland

These features have been partially or fully developed by SIG members in Fedora Linux and backported to CentOS Stream 9 for the benefit of the Enterprise Linux community.

#### Documentation

We have continued fleshing out our [user documentation][7] website. Among other things, we have added an explicit [versioning policy][8] for our packages, documented our [systemd release process][9] and compiled a reference list of Hyperscale-related [conference talks][10].

As previously mentioned, we would very much welcome any feedback and [contributions][11] you might have for this documentation.

#### systemd

The latest version in the Hyperscale SIG continues to be systemd 249. Since the last update we have [re-enabled `systemd-repart`][12] and backported a fix for [BPF cgroup controller realization][13]. We now also compile systemd without support for iptables, thus defaulting to nftables, in line with the [Fedora packaging][14]. This has allowed us to create builds of systemd 249 for CentOS Stream 9.

In order to support systemd builds, our meson backport has also been updated to 0.58.2.

#### Compression libraries

We have branched and updated lz4 to 1.9.3 and zstd to 1.5.0. Because these libraries are ABI and API compatible, we were able to push these updates without requiring additonal rebuilds of downward dependencies.

#### Kernel

#### CentOS Stream 9

Neal Gompa has started building an experimental kernel for CentOS Stream Hyperscale 9 based on the CentOS Stream/RHEL 9 kernel sources. Initial kernel builds have been released to the experimental repository. As part of this effort, he has been working with the RHEL kernel developers on developing the workflow for external (that is, non-Red Hat) contributors and [has begun contributing to the RHEL kernel][15].

We are also collaborating with the CentOS Kmods SIG to assist in enablement of the necessary support modules in the RHEL kernel to offer Btrfs as a kernel module package for RHEL 9, for those using RHEL 9 or derivatives and need the official RHEL kernel. As part of this, we intend to contribute community maintenance of Btrfs in the RHEL kernel tree for our kernel and the Kmods SIG to carve out and build as a kernel module package.

#### CentOS Stream 8

The CentOS 8 kernel has remained at 5.12 while Justin Vreeland looks into issues showing up in the bpf selftest during aarch64 builds. Justin plans to have it sync’d with the CentOS Stream 9 kernel Neal has been working on by the end of Q1 2022.

#### Live media

We started work on getting the necessary image build tools shipped in EPEL 9 to start offering live media based on CentOS Stream 9. The `livecd-tools` package is currently blocked on `dumpet`, which has [a stalled package branch request for EPEL][16]. The `appliance-tools` package is blocked on `livecd-tools` in EPEL. The `kiwi` package is currently blocked on [Red Hat shipping `mtools` on all architectures][17]. This should be resolved once the next CentOS Stream 9 compose is released and imported into Fedora Koji for EPEL 9.

#### DNF/RPM stack with CoW support

We have rebased the [Copy-on-Write][18] packaging stack in the experimental repository to match the latest updates that landed in CentOS Steam 8 proper.

### Health and Activity

The SIG continues to maintain a healthy development pace.

#### Meetings

The SIG holds regular [bi-weekly meetings][19] on Wednesdays at 16:00 UTC. Meetings are logged and the minutes for past meetings are [available][20].

The SIG uses the [`#centos-hyperscale`][21] IRC channel for ad-hoc communication and work coordination, and the [centos-devel][22] mailing list for async discussions and announcements. The SIG also holds open [monthly video conference sessions][23] to promote collaboration and social interaction.

#### Conference talks

Last quarter, Davide Cavalca and Neal Gompa presented an update on SIG activities at [CentOS Dojo, October 2021][24] ([slides][25], [video][26]). Hyperscale SIG work was also covered in [Building the future with CentOS Stream][27] at the [Red Hat mini-theater][28] during [Supercomputing 2021][29].

This year, we’ll be presenting another update on SIG activites at [CentOS Dojo, FOSDEM 2022][30]. SIG-adjacent talk proposals have also been submitted to [DevConf.cz 2022][31] and [SCALE 19x][32].

#### Planned work

The SIG tracks pending work as issues on our [Pagure repository][33]. Notable projects currently in flight include:

- using CBS to build our spin images
- shipping an updated QEMU package in EPEL
- integrate btrfs transactional updates as an optional feature
- setup a continuous build pipeline for the container image on the CentOS CI infrastructure
- build a set of Hyperscale-enabled Cloud images

### Issues for the Board

We have no issues to bring to the board’s attention at this time.

--------------------------------------------------------------------------------

via: https://blog.centos.org/2022/01/centos-hyperscale-sig-quarterly-report-for-2021q4/

作者：[CentOS Blog][a]
选题：[lkxed][b]
译者：[译者ID](https://github.com/译者ID)
校对：[校对者ID](https://github.com/校对者ID)

[a]: https://blog.centos.org
[b]: https://github.com/lkxed
[1]: https://blog.centos.org/2021/10/centos-hyperscale-sig-quarterly-report-for-2021q3/
[2]: https://wiki.centos.org/SpecialInterestGroup/Hyperscale
[3]: https://wiki.centos.org/SpecialInterestGroup/Hyperscale#Membership
[4]: https://pagure.io/centos-sig-hyperscale/package-bugs
[5]: https://blog.centos.org/2021/12/introducing-centos-stream-9/
[6]: https://pagure.io/centos-sig-hyperscale/sig/issue/83
[7]: https://sigs.centos.org/hyperscale/
[8]: https://sigs.centos.org/hyperscale/internal/versioning_policy/
[9]: https://sigs.centos.org/hyperscale/internal/systemd/
[10]: https://sigs.centos.org/hyperscale/internal/talks/
[11]: https://sigs.centos.org/hyperscale/internal/documentation/
[12]: https://pagure.io/centos-sig-hyperscale/systemd/c/7456943fdfb262262db34b8173f20c962baf8b58?branch=fb-v249.4
[13]: https://pagure.io/centos-sig-hyperscale/systemd/c/a79f75109e6e5a916cd70d35ef192ae85e4f0266?branch=fb-v249.4
[14]: https://src.fedoraproject.org/rpms/systemd/pull-request/68
[15]: https://gitlab.com/redhat/centos-stream/src/kernel/centos-stream-9/-/merge_requests?scope=all&state=all&author_username=Conan_Kudo
[16]: https://pagure.io/releng/issue/10526
[17]: https://bugzilla.redhat.com/2036365
[18]: https://fedoraproject.org/wiki/Changes/RPMCoW
[19]: https://www.centos.org/community/calendar/#Hyperscale_SIG
[20]: https://wiki.centos.org/SpecialInterestGroup/Hyperscale/Meetings
[21]: https://wiki.centos.org/irc#A.23centos-hyperscale
[22]: https://lists.centos.org/mailman/listinfo/centos-devel
[23]: https://www.centos.org/community/calendar/#hyperscale-sig-monthly-hangout
[24]: https://wiki.centos.org/Events/Dojo/October2021
[25]: https://wiki.centos.org/Events/Dojo/October2021?action=AttachFile&do=view&target=Hyperscale+SIG+update.pdf
[26]: https://www.youtube.com/watch?v=s6unjYyjbXk&list=PLuRtbOXpVDjCSvlyrEtctWVeXTNWilmOH&index=7
[27]: https://t.co/GNlDBKPQNk
[28]: https://www.redhat.com/en/events/red-hat-SC21#mini-theater-schedule
[29]: https://sc21.supercomputing.org/
[30]: https://wiki.centos.org/Events/Dojo/FOSDEM2022
[31]: https://www.devconf.info/cz/
[32]: https://www.socallinuxexpo.org/scale/19x
[33]: https://pagure.io/centos-sig-hyperscale/sig/issues
