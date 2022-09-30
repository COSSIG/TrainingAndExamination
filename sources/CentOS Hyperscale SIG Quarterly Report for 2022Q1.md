[#]: subject: "CentOS Hyperscale SIG Quarterly Report for 2022Q1"
[#]: via: "https://blog.centos.org/2022/04/centos-hyperscale-sig-quarterly-report-for-2022q1/"
[#]: author: "CentOS Blog https://blog.centos.org"
[#]: collector: "lkxed"
[#]: translator: " "
[#]: reviewer: " "
[#]: publisher: " "
[#]: url: " "

CentOS Hyperscale SIG Quarterly Report for 2022Q1
======

This report covers work that happened between January 1st and April 4th. For previous work, see the [2021Q4 report][1].

## Purpose

The [Hyperscale SIG][2] focuses on enabling CentOS Stream deployment on large-scale infrastructures and facilitating collaboration on packages and tooling.

## Membership update

Since the last update, the SIG gained six new members (Manu Bretelle, Daan De Meyer, Oscar Dominguez, Kevin Wells, Ali Koroglu and Brandon Johnson).

We welcome anybody that’s interested and willing to do work within the scope of the SIG to join and contribute. See the [membership][3] section on the wiki for the current members list and how to join.

## Releases and Packages

Unless otherwise specified, packages are available in our main repository, which can be enabled with `dnf install centos-hyperscale-release`. Please report any issues with these packages on our [package-bugs][4] tracker.

### Documentation

We have continued fleshing out our [user documentation][5] website. Among other things, we have added extensive documentation of the [kernel build and contribution][6] process, greatly expanded the existing [systemd][7] documentation and improved our [SIG onboarding][8] process.

As previously mentioned, we would very much welcome any feedback and [contributions][9] you might have for this documentation.

### systemd

The latest released version in the Hyperscale SIG is systemd 250.3, for both CentOS Stream 8 and CentOS Stream 9.

The systemd RPM sources for the Hyperscale SIG have been migrated to use a flat dist-git layout, making it easier to rebase our changes directly on top of Fedora Rawhide. Our specfile will also now build directly with tarballs from the Hyperscale SIG’s systemd Git fork. This change means our backports no longer have to be managed though patch files; they will be included directly from our Git fork.

### Kernel

#### CentOS Stream 9

Updated kernel builds tracking the upstream CentOS Stream 9 kernel have continued to flow into the Hyperscale experimental repository. Of note, we are testing a backport of [SimpleDRM with fbdev emulation][10] to ensure Wayland environments work regardless of graphics hardware.

Neal Gompa has written [basic automation for updating the kernel][11]. As part of that, the kernel RPM sources for the Hyperscale SIG have been migrated to use a flat dist-git layout. We eventually aim to introduce CI/CD to continually track and test our changes on top of Red Hat’s changes in the baseline CentOS Stream 9 kernel.

#### CentOS Stream 8

The CentOS 8 kernel is now building with the same sources as our CentOS 9 kernel and work has begun to automate rebases and builds using scripts written for our CentOS 9 kernel.

### Container images

We have reworked our [container build scripts][12] to properly support CentOS Stream 9, and have pushed updated containers to our [registry namespace][13] on [Quay.io][14].

### Package updates

#### CentOS Stream 9

We have contributed updates to SDL2 (to backport fixes for running SDL2 applications as native Wayland applications) and upgraded Flatpak to the 1.12 version series to improve compatibility with the wider ecosystem of Flatpaks.

We also contributed changes to `centos-stream-release` to make it easier for spins to selectively replace branding packages to producing spins or remixes.

#### CentOS Stream 8

We have published updates for ethtool (to 5.16) and zstd (to 1.5.1) for CentOS Stream 8.

### Spin updates

All necessary image build tools are now shipped in EPEL 9 to support building live media for CentOS Stream 9. This includes the following packages: `kiwi`, `livecd-tools`, `appliance-tools`.

We have started working on the Hyperscale spin based on CentOS Stream 9. In the coming weeks, the Cloud variant of the Hyperscale spin will become available on the Amazon Web Services Marketplace. Other cloud platforms and spin variants will follow shortly thereafter.

### DNF/RPM stack with CoW support

The [Copy-on-Write][15] stack got rebased on top of RPM’s head as of late January and the change has been ported and distributed under the CentOS Stream 8 and CentOS Stream 9 Hyperscale’s experimental repos.

RPM CoW now verify RPM signatures at transcode time and can re-use this within `rpmkeys` logic. Likewise, `rpm -i` does not require the use of `--nodigest` anymore.

A test suite has been added, testing different scenarios and ensuring that future changes do not break functionalities.

Finally, by removing the need for executable stack, the `reflink` plugin is now compatible with SELinux-enabled environments.

### Sticky Vendor

Hyperscale packages built after February 8, 2022 have their [vendor field set to “CentOS Hyperscale SIG”][16], e.g. `systemd-249.4-2.13.hs.el8`. This allows users to stick to Hyperscale packages without worrying about a higher NEVRA in other repositories, by setting [`allow_vendor_change=False`][17].

## Health and Activity

The SIG continues to maintain a healthy development pace.

### Meetings

The SIG holds regular [bi-weekly meetings][18] on Wednesdays at 16:00 UTC. Meetings are logged and the minutes for past meetings are [available][19].

The SIG uses the [`#centos-hyperscale`][20] IRC channel for ad-hoc communication and work coordination; this channel is also bridged on Matrix in the [`#centos-hyperscale:fedoraproject.org`][21] room. For async discussions and announcements we generally use the [centos-devel][22] mailing list. The SIG also holds open [monthly video conference sessions][23] to promote collaboration and social interaction.

### Conference talks

Last quarter, Davide Cavalca presented an update on SIG activities at [CentOS Dojo, FOSDEM 2022][24] ([slides][25], [video][26]). At the same event, Neal Gompa talked about the experience of contributing to CentOS Stream ([slides][27], [video][28]).

A SIG-adjacent talk around [CentOS Stream][29] has also been accepted for [SCALE 19x][30].

### Live streams

The SIG periodically does work live on Twitch from [its official Twitch channel][31]. Interested parties who want to watch and interact with us as we do work should follow us on Twitch to get notified for when we stream.

### Planned work

The SIG tracks pending work as issues on our [Pagure repository][32]. Notable projects currently in flight include:

- using CBS to build our spin images
- shipping an updated QEMU package in EPEL
- integrate btrfs transactional updates as an optional feature
- setup a continuous build pipeline for the container image on the CentOS CI infrastructure

## Issues for the Board

We have no issues to bring to the board’s attention at this time.

--------------------------------------------------------------------------------

via: https://blog.centos.org/2022/04/centos-hyperscale-sig-quarterly-report-for-2022q1/

作者：[CentOS Blog][a]
选题：[lkxed][b]
译者：[译者ID](https://github.com/译者ID)
校对：[校对者ID](https://github.com/校对者ID)

[a]: https://blog.centos.org
[b]: https://github.com/lkxed
[1]: https://blog.centos.org/2022/01/centos-hyperscale-sig-quarterly-report-for-2021q4/
[2]: https://wiki.centos.org/SpecialInterestGroup/Hyperscale
[3]: https://wiki.centos.org/SpecialInterestGroup/Hyperscale#Membership
[4]: https://pagure.io/centos-sig-hyperscale/package-bugs
[5]: https://sigs.centos.org/hyperscale/
[6]: https://sigs.centos.org/hyperscale/internal/kernel/
[7]: https://sigs.centos.org/hyperscale/internal/systemd/
[8]: https://sigs.centos.org/hyperscale/internal/onboarding/
[9]: https://sigs.centos.org/hyperscale/internal/documentation/
[10]: https://fedoraproject.org/wiki/Changes/ReplaceFbdevDrivers
[11]: https://pagure.io/centos-sig-hyperscale/linux-releng/blob/main/f/kernel-rebase/c9s
[12]: https://pagure.io/centos-sig-hyperscale/containers-releng
[13]: https://quay.io/repository/centoshyperscale/centos
[14]: http://Quay.io
[15]: https://fedoraproject.org/wiki/Changes/RPMCoW
[16]: https://pagure.io/centos-infra/issue/621
[17]: https://dnf.readthedocs.io/en/latest/conf_ref.html#allow-vendor-change-label
[18]: https://www.centos.org/community/calendar/#hyperscale-sig
[19]: https://sigs.centos.org/hyperscale/internal/meetings/
[20]: https://wiki.centos.org/irc#A.23centos-hyperscale
[21]: https://matrix.to/#/#centos-hyperscale:fedoraproject.org
[22]: https://lists.centos.org/mailman/listinfo/centos-devel
[23]: https://www.centos.org/community/calendar/#hyperscale-sig-monthly-hangout
[24]: https://wiki.centos.org/Events/Dojo/FOSDEM2022
[25]: https://wiki.centos.org/Events/Dojo/FOSDEM2022?action=AttachFile&do=view&target=Hyperscale+SIG+update%2C+February+2022.pdf
[26]: https://youtu.be/2Wb8g1irrw8
[27]: https://wiki.centos.org/Events/Dojo/FOSDEM2022?action=AttachFile&do=view&target=datto-exp-contrib-centos-stream-centdojo-fosdem22.pdf
[28]: https://youtu.be/t6FQpCj5jgg
[29]: https://www.socallinuxexpo.org/scale/19x/presentations/building-future-centos-stream
[30]: https://www.socallinuxexpo.org/scale/19x
[31]: https://www.twitch.tv/centoshyperscale
[32]: https://pagure.io/centos-sig-hyperscale/sig/issues
