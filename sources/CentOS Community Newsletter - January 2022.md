[#]: subject: "CentOS Community Newsletter, January 2022"
[#]: via: "https://blog.centos.org/2022/01/centos-community-newsletter-january-2022/"
[#]: author: "CentOS Blog https://blog.centos.org"
[#]: collector: "lkxed"
[#]: translator: " "
[#]: reviewer: " "
[#]: publisher: " "
[#]: url: " "

CentOS Community Newsletter, January 2022
======

## January 2022 Newsletter

### Project News

**Update 2022-02-01:** These instructions no longer work since the packages were moved from the mirror network to the vault. See the CentOS 8 section of the [CentOS Stream page][1] for current instructions.

The big news, of course, is that CentOS Linux 8 reached End Of Life on Friday, December 31, 2021. The CentOS Project recommends that you migrate existing CentOS Linux 8 installations to CentOS Stream:

```
dnf swap centos-linux-repos centos-stream-repos
dnf distro-sync
```

### Upcoming events

The first CentOS Dojo of 2022 is scheduled for February 3rd and 4th, immediately before the first day of [FOSDEM 2022][2]. We expect to publish the schedule to the [event wiki page][3] by the time you read this newsletter. The event will be held online, and registration is free! Join us for two days of CentOS content and networking.

### SIG Reports

[Special Interest Groups][4] (SIGs) are the most interesting part of the CentOS project - this is where people build value on top of the CentOS platform. SIGs report quarterly on what they’ve been up to. Here’s this month’s reports.

#### Software Collections

#### Purpose

Provide packages and support for both Red Hat and community Software collections.

#### Releases

**RHSCL-3.8** – A new Red Hat Software Collections were released for RHEL 7 and subsequently made available for CentOS 7.

The following collections are now available:

- Developer Tollset 11 (`devtoolset-11`)
- Nginx 12.0 (`rh-nginx120`)
- Redis 6 (`rh-redis6`)

#### Health and activity

Given that there are no plans for supporting Software Collections in newer RHEL and/or CentOS Stream, this SIG is now effectively in a “sunset” phase.

Regular rebuilds and updates of both existing and new collections are still planned, but no other activity is expected.

We also expect that the SIG will cease its activity around the EOL date of CentOS 7 (June 2024).

#### Kmods SIG

This report covers work that happened since last report. The previous report can be found [here][5].

#### Purpose

Packaging and maintaining kernel modules for CentOS Stream and Enterprise Linux.

#### Membership Update

No SIG members have been added since last report.

We welcome anybody that’s interested and willing to do work within the scope of the SIG to join and contribute.

#### Support for CentOS Stream 9

The Kmods SIG recently started building kernel modules for CentOS Stream 9. In case you are missing a particular kernel module in CentOS Stream 9, you can let us know [here][6].

#### Support for EL8

The Kmods SIG continues to provide packages for EL8, i.e. RHEL 8 and any of its derivatives, even though CentOS Linux 8 went EOL. This can be achieved thanks to RHEL 8 buildroots being available in CBS. We plan to do the same for RHEL 9 once released and available in CBS.

#### New Packages

See [Kmods SIG’s documentation][7] for lists of available packages. This docuementation also provides further information, e.g. how to enable the Kmods SIG’s repositories.

New packages released since last report:

- NTFS3

Note that the kernel modules provided by the Kmods SIG are currently not signed with a private key. Hence it is required to disable Secure Boot to be able to use any of these kernel modules.

Please report any issues with these packages in the corresponding project on [pagure.io][8] or [here][9] in case the issue is not related to a particular package.

#### Health and Activity

The Kmods SIG maintains a healthy development pace.

#### Communication

Regular meetings are scheduled every two weeks (on even weeks) on Monday 1600 UTC in #centos-meeting. Everyone is welcome to join!

You can also get in touch with SIG members at any time in #centos-kmods.

#### Open Issues

Signing kernel modules: This requires collaboration and further discussion with Infra SIG. Especially about how to securely store a SIG specific key that can be used in CBS, but is not accessible by any unauthorized person.

Driver Disks: The SIG would like to provide Driver Disks required to install CentOS Stream on unsupported hardware. The current state can be tracked [here][10].

#### Issues for the Board

We have no issues to bring to the board’s attention at this time.

#### Hyperscale

The Hyperscale SIG has posted their quarterly report [on the CentOS blog][11].

#### Automotive

#### Membership update

This SIG does not have a formal membership process. The mailing list currently has 77 subscribers representing at least yy companies. I have been asked to act as chair for the first few months in order to stabilize the SIG.

#### Releases

The SIG is not yet creating builds or publishing releases, but we are very close to doing so at this point; see the report below.

#### Health report and general activity

The SIG has had two public meetings per month, one formal and one informal “office hours”, each with 25-40 attendees representing 7-10 separate organizations. We feel this is a good start at corporate community diversity but will continue to work toward a community-driven project. This SIG is intended to be a community effort with contributions and shared benefits from all participants.

Several RH employees made the first contribution to the project as well as the infrastructure required to build and test it. We now occupy a gitlab repository building software regularly, with build instructions provided, and we are on track for a downloadable release in Q1 2022.

This is a high-level summary of current activity from our technical lead:

- qemu and raspberry pi
- x86_64 and aarch64,
- ostree-based (default) and non-ostree-based
- booting via uefi of by-passing it and booting directly the kernel

- minimal
- osbuilder (containing the tools allowing to build images with osbuild)
- neptune (demo image with a graphical interface running the demo app:neptune)

- The work keeps on going at: [https://gitlab.com/redhat/automotive/automotive-sig][12]
- We have created manifests in that repository that can be used with OSBuild tocreate a number of images.
- We currently support:
- We then have 3 images
- The OSBuild manifests have been streamed-line and simplified a lot. If you havenot look at them in a while have a look !
- We have also added a mechanism to easily build images from within a virtualmachine, which makes it easier to build images without root privileges.
- The VM created for the step just above (^) can also be migrated to a differentsystem, thus allowing to build more easily in a different architecture.
- Instructions on how to build images have also been greatly simplifiedThe doc at: [https://sigs.centos.org/automotive/building/][13] is up to date
- We have a kernel-auto package based on the CentOS-Stream package and with theReal-Time patches included
- We have a few koji tags set-up for the SIG, the kernel-auto is the mainbeneficiary of them (with a couple of other RT related packages)
- We are working on automatically building some of our sample images and makingthem available.A few of them can be found at: [https://pingou.fedorapeople.org/images/][14] butthis is a temporary location and they are now over a month old.
- We have been sending weekly updates to the SIG mailing list on a regularcadence and will try to continue doing it.

### Board Election

We are delighted to announce that in the January Board of Directors meeting, we [selected two new directors][15]: Amy Marrich and Celeste Lyn Paul. Please join us in welcoming them.

As you are aware, Jim Perrin and Karanbir Singh have stepped down at the expiration of their board term, and we thank them for their many years of service.

You will no doubt hear more from them in the coming days. Welcome, Amy and Celeste, and thank you for being willing to take on this important role in our community.

### Community Manager

It’s with some amount of sadness that I, personally, announce that I (Rich Bowen) will be stepping out of the community manager role in the coming weeks. I will be replaced in that role by Shaun McCance, who has a great deal of experience in open source communities. Please welcome Shaun, and do what you can to help him succeed in his new role.

### Until next time …

While this newsletter is very late this month, that’s not unusual for January. I hope that you all have a wonderful new year, and that we see each of you stepping up in new ways in the CentOS community this coming year.

--------------------------------------------------------------------------------

via: https://blog.centos.org/2022/01/centos-community-newsletter-january-2022/

作者：[CentOS Blog][a]
选题：[lkxed][b]
译者：[译者ID](https://github.com/译者ID)
校对：[校对者ID](https://github.com/校对者ID)

[a]: https://blog.centos.org
[b]: https://github.com/lkxed
[1]: https://www.centos.org/centos-stream/
[2]: https://fosdem.org/2022/
[3]: https://wiki.centos.org/Events/Dojo/FOSDEM2022
[4]: https://wiki.centos.org/SpecialInterestGroup
[5]: https://blog.centos.org/2021/10/kmods-sig-quarterly-report-2/
[6]: https://pagure.io/centos-sig-kmods/sig/issue/12
[7]: https://sigs.centos.org/kmods/
[8]: https://pagure.io/projects/centos-sig-kmods/%2A
[9]: https://pagure.io/centos-sig-kmods/sig/issues
[10]: https://pagure.io/centos-infra/issue/418
[11]: https://blog.centos.org/2022/01/centos-hyperscale-sig-quarterly-report-for-2021q4/
[12]: https://gitlab.com/redhat/automotive/automotive-sig
[13]: https://sigs.centos.org/automotive/building/
[14]: https://pingou.fedorapeople.org/images/
[15]: https://lists.centos.org/pipermail/centos-devel/2022-January/120134.html
