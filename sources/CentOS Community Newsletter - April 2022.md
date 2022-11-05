[#]: subject: "CentOS Community Newsletter, April 2022"
[#]: via: "https://blog.centos.org/2022/04/centos-community-newsletter-april-2022/"
[#]: author: "CentOS Blog https://blog.centos.org"
[#]: collector: "lkxed"
[#]: translator: "L-N1988"
[#]: reviewer: " "
[#]: publisher: " "
[#]: url: " "

CentOS Community Newsletter, April 2022
======

## Project News

### Transition to issues.redhat.com

As CentOS Stream 9 stabilizes and we approach a release of RHEL 9, [Red Hat is planning to transition][1] to using [issues.redhat.com][2] exclusively for reporting issues and requesting features for RHEL and CentOS, deprecating the use of [bugzilla.redhat.com][3]. This will be a gradual process as we all figure out the workflows that work best for the CentOS community.

### KDE in EPEL 9

Good news for KDE fans. [KDE is ready for testing][4] in EPEL 9 for CentOS Stream 9 and related operating systems. [EPEL][5] is a project under the Fedora umbrella that builds packages for Enterprise Linux that aren’t available as supported packages in RHEL. CentOS Stream allows EPEL to get ahead of the game and build packages earlier than ever before.

### Bringing RHEL docs to CentOS

The RHEL documentation team has been working on moving their content and processes to CentOS. They have made a [preview build][6] of their work so far. This is an ongoing effort, and it will take time to upstream everything to CentOS.

## SIG Reports

### Automotive SIG

#### Membership update

This SIG does not have a formal membership process. The mailing list currently has 89 subscribers representing at least 12 companies, though not all subscribers use corporate emails and some are participating as individuals.

#### Releases in the most recent quarter (or most recent release, if none in that quarter)

The SIG now provides a new distribution: Automotive Stream Distribution (AutoSD), a CentOS Stream derivative designed specifically around the needs of an automotive OS, and transparently the upstream project for Red Hat’s eventual in-vehicle OS product. AutoSD has been downloaded and used by several organizations who have commented or asked for help, so we know it is getting some traction though of course we don’t have exact metrics on usage.

#### Health report and general activity narrative.

The SIG has had two public meetings per month, one formal and one informal “office hours”, each with 25-40 attendees, with visible participation from 7-10 separate organizations. This SIG is intended to be a community effort with contributions and shared benefits from all participants.

Several Red Hat employees made the first contributions to the project as well as the infrastructure required to build and test it. We now occupy a gitlab repository building software regularly using CI, with build instructions provided. Sample images are present and downloadable along with customization and build instructions.

This is a high-level summary of current activity:

- The work is migrating to a CentOS namespace within GitLab in order to cement our intention as a community project: [https://gitlab.com/centos/automotive][7]
- CI/CD infrastructure is in place
- Downloadable images are available: [https://autosd.sig.centos.org/][8]
- Documentation has been greatly expanded with both community and corporate contributions: [https://sigs.centos.org/automotive/][9]
- Documentation now includes detailed contribution guidelines: [https://sigs.centos.org/automotive/contributing/contributing-to-auto-sig-repo/][10]
- Ongoing discussions within the meetings have centered around supported hardware and expectations for documentation
- A new meetings page contains recordings of all meetings: [https://wiki.centos.org/SpecialInterestGroup/Automotive/Meetings][11]
- Synchronous communications have moved from IRC to Matrix thanks to some help from Fedora: [https://app.element.io/#/room/#centos-automotive-sig:fedoraproject.org][12]

#### Issues for the board to address, if any

None, keep up the excellent work 🙂

### Hyperscale SIG

The Hyperscale SIG has posted their quarterly report [on the CentOS blog][13].

### Kmods SIG

This report covers work that happened since last report. The previous report can be found [here][14].

#### Purpose

Packaging and maintaining kernel modules for CentOS Stream and Enterprise Linux.

#### Membership Update

Unfortunately, **Jonathan Billings** left the Kmods SIG due to lack of time. We thank him for all the work he contributed to the Kmods SIG: Thank you!

No SIG members have been added since last report. We welcome anybody that’s interested and willing to do work within the scope of the SIG to join and contribute.

#### Support for CentOS Stream 9 / EL9

The Kmods SIG provides packages for CentOS Stream 9 and will for EL9 once released and available in CBS.

#### Support for CentOS Stream 8 / EL8

The Kmods SIG continues to provide packages for CentOS Stream 8 and EL8.

#### New Packages

See [Kmods SIG’s documentation][15] for lists of available packages. This documentation also provides further information, e.g. how to enable the Kmods SIG’s repositories.

Notable packages released since last report:

- btrfs-progs (9 only)
- kmod-btrfs (9 only)
- virtual-guest-additions (9 only)
- kmod-vbox-guest-additions (9 only)
- ecryptfs-utils
- kmod-ecryptfs

Note that the kernel modules provided by the Kmods SIG are currently not signed with a private key. Hence it is required to disable Secure Boot to be able to use any of these kernel modules.

Please report any issues with these packages in the corresponding project on [pagure.io][16] or [here][17] in case the issue is not related to a particular package.

#### Recent Activities

The Kmods SIG started working on a dnf plugin to improve handling of kABI tracking kernel module packages. See the [dnf-plugin-kmods][18] project on pagure.io for further details.

#### Health and Activity

The Kmods SIG maintains a healthy development pace.

#### Communication

Regular meetings are scheduled monthly, in the first week, on Monday at 1600 UTC in #centos-meeting. Everyone is welcome to join!

You can also get in touch with SIG members at any time in #centos-kmods.

#### Open Issues

- **Signing kernel modules:** This requires collaboration and further discussion with Infra SIG. Especially about how to securely store a SIG specific key that can be used in CBS, but is not accessible by any unauthorized person.
- **Driver Disks:** The SIG would like to provide Driver Disks required to install CentOS Stream on unsupported hardware. The current state can be tracked [here][19].

#### Issues for the Board

We have no issues to bring to the board’s attention at this time.

--------------------------------------------------------------------------------

via: https://blog.centos.org/2022/04/centos-community-newsletter-april-2022/

作者：[CentOS Blog][a]
选题：[lkxed][b]
译者：[译者ID](https://github.com/译者ID)
校对：[校对者ID](https://github.com/校对者ID)

[a]: https://blog.centos.org
[b]: https://github.com/lkxed
[1]: https://lists.centos.org/pipermail/centos-devel/2022-March/120269.html
[2]: https://issues.redhat.com/
[3]: https://bugzilla.redhat.com/
[4]: https://lists.centos.org/pipermail/centos-devel/2022-March/120283.html
[5]: https://docs.fedoraproject.org/en-US/epel/
[6]: https://lists.centos.org/pipermail/centos-docs/2022-March/026867.html
[7]: https://gitlab.com/centos/automotive
[8]: https://autosd.sig.centos.org/
[9]: https://sigs.centos.org/automotive/
[10]: https://sigs.centos.org/automotive/contributing/contributing-to-auto-sig-repo/
[11]: https://wiki.centos.org/SpecialInterestGroup/Automotive/Meetings
[12]: https://app.element.io/#/room/#centos-automotive-sig:fedoraproject.org
[13]: https://blog.centos.org/2022/04/centos-hyperscale-sig-quarterly-report-for-2022q1/
[14]: https://blog.centos.org/2022/01/centos-community-newsletter-january-2022/
[15]: https://sigs.centos.org/kmods/
[16]: https://pagure.io/projects/centos-sig-kmods/%2A
[17]: https://pagure.io/centos-sig-kmods/sig/issues
[18]: https://pagure.io/centos-sig-kmods/dnf-plugin-kmods
[19]: https://pagure.io/centos-infra/issue/418
