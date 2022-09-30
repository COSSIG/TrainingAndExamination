[#]: subject: "CentOS Community Newsletter, July 2022"
[#]: via: "https://blog.centos.org/2022/07/centos-community-newsletter-july-2022/"
[#]: author: "CentOS Blog https://blog.centos.org"
[#]: collector: "lkxed"
[#]: translator: " "
[#]: reviewer: " "
[#]: publisher: " "
[#]: url: " "

CentOS Community Newsletter, July 2022
======

## Project News

### Summer Dojo Videos

We held an [online Dojo][1] on June 17. [Videos of the talks][2] are now available.

### DevConf Dojo

CentOS is hosting an in-person Dojo at [DevConf.US][3]. Dojos are free mini-conferences with sessions on a range of topics in the Enterprise Linux ecosystem. This Dojo takes place on August 17 at Boston University. Registration is free but strongly recommended. We also have a room block at the nearby Residence Inn. See [the event page][4] for details.

The call for presentations is open thru July 22. We’d love to hear what you’re doing with CentOS.

### Hyperscale SIG Meetup

The CentOS Hyperscale SIG will be holding an in-person meetup on August 16th, 2022 at Boston University. This is the same venue hosting CentOS Dojo on August 17th and DevConf.us on August 18th-20th. The meetup is open to everybody interested – you don’t have to be a member of the SIG to attend, and we’d welcome participation from anyone interested in this space.

The event will be held from 9am to 5pm in the GSU conference room 310 at Boston University. While this is an in-person event, we will do our best to setup a conference bridge so that remote participants can attend and interact as well.

Please register at [https://www.eventbrite.com/e/centos-hyperscale-sig-meetup-dojodevconfus-2022-tickets-384259589777][5] to help with the event planning.

### CentOS CI

CentOS CI is going hardwareless. The CentOS CI team will be retiring hardware as it reaches end of life. They will take this opportunity to modernize infrastructure and move to a hybrid cloud environment.

[Read the announcment][6] and watch the video of the [Dojo session on CentOS CI][7].

### Alternate Images SIG Proposal

Troy Dawson has proposed an [Alternate Images Special Interest Group][8]. This SIG would produce ISO images that aren’t produced by the core CentOS Stream, including live images and alternate install images. Discussion is ongoing.

## SIG Reports

Each month, we publish a rotating selection of quarterly reports from our [Special Interest Groups][9]. This month includes reports from the Software Collections, Hyperscale, Kmods, and Automotive SIGs.

### Software Collections SIG

#### Purpose

Provide an upstream development area for various software collections and related tools. Provide RedHat authored and released collection packages for CentOS.

#### Membership

No membership changes. New members are always welcome, and they would help to alleviate the issues outlined below.

#### Releases and packages

No major releases in the last quarter. The RedHat packages are being rebuilt and released semi-regularly.

#### Health and activity

The group is mostly passive, focusing on the rebuild and maintenance of existing packages. It has a single active member (jstanek), and this shows in various places:

- The https://softwarecollections.org website is being kept online, but the content is out of date; technical issues with current hosting prevents log-in and updating the content.
- Changes in the CentOS infrastructure resulted in broken CI; rebuilt packages are no longer being tested automatically. Fixing this is planned, but no ETA.

In short, the amount of work needed grows faster than jstanek is able to keep up. Additional members would be very welcome.

### Hyperscale SIG

The Hyperscale SIG has posted their quarterly report [on the CentOS blog][9].

### Kmods SIG

This report covers work that happened since last report. The previous report can be found [here][10].

#### Purpose

Packaging and maintaining kernel modules for CentOS Stream and Enterprise Linux.

#### Membership Update

No SIG members have been added since last report. We welcome anybody that’s interested and willing to do work within the scope of the SIG to join and contribute.

#### Support for CentOS Stream 9 / EL9

The Kmods SIG provides packages for CentOS Stream 9 and will for EL9 once available in CBS.

#### Support for CentOS Stream 8 / EL8

The Kmods SIG continues to provide packages for CentOS Stream 8 and EL8.

#### New Packages

See [Kmods SIG’s documentation][11] for lists of available packages. This documentation also provides further information, e.g. how to enable the Kmods SIG’s repositories.

Note that the kernel modules provided by the Kmods SIG are currently not signed with a private key. Hence it is required to disable Secure Boot to be able to use any of these kernel modules.

Please report any issues with these packages in the corresponding project on [gitlab.com/CentOS/kmods][12] or [here][13] in case the issue is not related to a particular package.

#### Recent Activities

The Kmods SIG is currently moving all of its resources to [gitlab.com/CentOS/kmods][12]. Moving to gitlab.com allows us to use the GitLab CI for the automated detection of required kernel module rebuilds due to kABI changes, i.e., it is now all public and everybody can see what’s going on. We also changed the structure of some of the kernel module repositories. Where appropriate we have dedicated source-git and dist-git repositories where the dist-git is auto-generated from the source-git and manual changes are only meant to be applied to the source-git repository. These changes were implemented to make it as easy as possible for everyone to contribute improvements or bug fixes.

#### Health and Activity

The Kmods SIG maintains a healthy development pace.

#### Communication

Regular meetings are scheduled monthly, in the first week, on Monday at 1600 UTC in #centos-meeting. Everyone is welcome to join! You can also get in touch with SIG members at any time in #centos-kmods.

#### Open Issues

- **Signing kernel modules:** This requires collaboration and further discussion with Infra SIG. Especially about how to securely store a SIG specific key that can be used in CBS, but is not accessible by any unauthorized person.
- **Driver Disks:** The SIG would like to provide Driver Disks required to install CentOS Stream on unsupported hardware. The current state can be tracked [here][14].

#### Issues for the Board

The Kmods SIG asks for clarification concerning the possibility of SIGs creating content for RHEL 8 and 9. Open questions include support for release packages, see extras-common tag, and for how long SIGs can expect to be able to build for RHEL, e.g., up till end of “Full Support” or “Maintenance Support” of the RHEL life cycle.

### Automotive SIG

#### Membership update

This SIG does not have a formal membership process. The mailing list currently has 94 subscribers representing at least 30 organizations, though not all subscribers use corporate emails and some are participating as individuals.

#### Releases in the most recent quarter (or most recent release, if none in that quarter)

The SIG provides a new distribution: Automotive Stream Distribution (AutoSD), a CentOS Stream derivative designed specifically around the needs of an automotive OS, and transparently the upstream project for Red Hat’s eventual in-vehicle OS product. AutoSD has been downloaded and used by several organizations who have commented or asked for help, so we know it is getting some traction though of course we don’t have exact metrics on usage.

#### Health report and general activity narrative.

The SIG has had two public meetings per month, one formal and one informal “office hours”, each with 25-40 attendees, with visible participation from 7-10 separate organizations. This SIG is intended to be a community effort with contributions and shared benefits from all participants. All formal meetings are recorded and posted on this page:[https://wiki.centos.org/SpecialInterestGroup/Automotive/Meetings][15]

Several Red Hat employees made the initial contributions to the project as well as the infrastructure required to build and test it. We now occupy a gitlab repository building software regularly using CI, with build instructions provided on the documentation page at [https://sigs.centos.org/automotive/][16]. Sample images are present and downloadable along with customization and build instructions.

This is a high-level summary of current activity:

- All work has migrating to a CentOS namespace within GitLab in order to cement our intention as a community project: [https://gitlab.com/centos/automotive][17]
- CI/CD infrastructure is in place
- Firmware size has been reduced
- Encryption is available via LUKS
- a Linux chroot is being worked on for Android devices
- manifests now enable EFI runtime services
- Lookaside cache structure
- Downloadable images are available: [https://autosd.sig.centos.org/][18]
- Documentation has been greatly expanded with both community and corporate contributions: [https://sigs.centos.org/automotive/][16]
- Documentation now includes detailed contribution guidelines: [https://sigs.centos.org/automotive/contributing/contributing-to-auto-sig-repo/][19]
- Ongoing discussions within the meetings have centered around supported hardware and expectations for documentation
- A new meetings page contains recordings of all meetings: [https://wiki.centos.org/SpecialInterestGroup/Automotive/Meetings][15]
- Synchronous communications have moved from IRC to Matrix thanks to some help from Fedora: [https://app.element.io/#/room/#centos-automotive-sig:fedoraproject.org][20]

#### Issues for the board to address, if any

None, keep up the excellent work 🙂

--------------------------------------------------------------------------------

via: https://blog.centos.org/2022/07/centos-community-newsletter-july-2022/

作者：[CentOS Blog][a]
选题：[lkxed][b]
译者：[译者ID](https://github.com/译者ID)
校对：[校对者ID](https://github.com/校对者ID)

[a]: https://blog.centos.org
[b]: https://github.com/lkxed
[1]: https://wiki.centos.org/Events/Dojo/Summer2022
[2]: https://www.youtube.com/playlist?list=PLuRtbOXpVDjBHX0AkqhpR2IS4Db2wZZt0
[3]: https://www.devconf.info/us/
[4]: https://wiki.centos.org/Events/Dojo/DevConfUS2022
[5]: https://www.eventbrite.com/e/centos-hyperscale-sig-meetup-dojodevconfus-2022-tickets-384259589777
[6]: https://lists.centos.org/pipermail/centos-devel/2022-June/120418.html
[7]: https://youtu.be/aqgs-3NnRmA
[8]: https://lists.centos.org/pipermail/centos-devel/2022-July/120445.html
[9]: https://blog.centos.org/2022/07/centos-hyperscale-sig-quarterly-report-for-2022q2/
[10]: https://blog.centos.org/2022/04/centos-community-newsletter-april-2022/
[11]: https://sigs.centos.org/kmods/
[12]: https://gitlab.com/CentOS/kmods
[13]: https://gitlab.com/CentOS/kmods/sig
[14]: https://pagure.io/centos-infra/issue/418
[15]: https://wiki.centos.org/SpecialInterestGroup/Automotive/Meetings
[16]: https://sigs.centos.org/automotive/
[17]: https://gitlab.com/centos/automotive
[18]: https://autosd.sig.centos.org/
[19]: https://sigs.centos.org/automotive/contributing/contributing-to-auto-sig-repo/
[20]: https://app.element.io/#/room/#centos-automotive-sig:fedoraproject.org
