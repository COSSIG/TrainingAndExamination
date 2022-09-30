[#]: subject: "CentOS Hyperscale SIG Quarterly Report for 2022Q2"
[#]: via: "https://blog.centos.org/2022/07/centos-hyperscale-sig-quarterly-report-for-2022q2/"
[#]: author: "CentOS Blog https://blog.centos.org"
[#]: collector: "lkxed"
[#]: translator: " "
[#]: reviewer: " "
[#]: publisher: " "
[#]: url: " "

CentOS Hyperscale SIG Quarterly Report for 2022Q2
======

This report covers work that happened between April 5th and July 4th. For previous work, see the [2022Q1 report][1].

## Purpose

The [Hyperscale SIG][2] focuses on enabling CentOS Stream deployment on large-scale infrastructures and facilitating collaboration on packages and tooling.

## Membership update

Since the last update, the SIG members have remained the same.

Justin Vreeland has decided to step down as co-chair of the SIG, and Neal Gompa has been elected to fill the vacancy. We thank Justin for all of his work in establishing the SIG and getting it up to speed and welcome Neal in his new role as co-chair. Neal will be serving alongside Davide Cavalca, who remains in the other co-chair seat.

We welcome anybody that’s interested and willing to do work within the scope of the SIG to join and contribute. See the [membership][3] section on the wiki for the current members list and how to join.

## Releases and Packages

Unless otherwise specified, packages are available in our main repository, which can be enabled with `dnf install centos-hyperscale-release`. Please report any issues with these packages on our [package-bugs][4] tracker.

### Documentation

We have continued fleshing out our [user documentation][5] website. Recent additions include details about our [containers image build process][6] and our [ELN Extras workflow][7]. We’ve also expanded our documentation around the [systemd release process][8] to cover the use of the [CI/CD infrastructure][9]. Finally, we have started formally documenting the SIG [governance processes][10].

As previously mentioned, we would very much welcome any feedback and [contributions][11] you might have for this documentation.

### systemd

The latest released version in the Hyperscale SIG is systemd 250.3, for both CentOS Stream 8 and CentOS Stream 9. We are in the process of deploying systemd 251.2.

We also updated the systemd daily CI to work with the new release process that was introduced along with the update to 250.3. The script was rewritten in Python and updated to run CI against both Centos Stream 8 and Centos Stream 9. On top of that, we added documentation on how to update the corresponding containers running in Openshift with any new changes made to the scripts.

Finally, we updated the release documentation in preparation for the release of 251.2.

### Kernel

The `brtfs-progs` package was updated to 5.16.2 on both CentOS Stream 8 and CentOS Stream 9. Additionally, we have started distributing the `compsize` utility (based on its Fedora packaging) in the SIG experimental repository.

We have also updated the `kpatch` package to include some additional bugfixes backported from upstream.

### Container images

We have started working on automating the container build pipeline by leveraging the Open Shift CI/CD infrastructure. The in-progress work is currently [up for review][12].

### Package updates

We have published updated backports of the TPM stack for CentOS Stream 8, notably `tpm2-tss` and `tpm2-tools`, based on the existing Fedora packaging. Also for CentOS Stream 8, we have published a patched version of `cloud-init` with support for newer EC2 metadata versions. We have also contributed upstream fixes for this for [CentOS Stream 8][13] and [CentOS Stream 9][14].

On the development front, we have spun up a CI pipeline to [detect package updates][15] in upstream CentOS that would supersede our versions and alert us, so that we can publish updates in a timely basis. This pipeline leverages the [MQTT broker][16] where [git.centos.org][17] event notifications are published. While this was written for Hyperscale, we hope it could be useful for other SIGs as well.

### DNF/RPM stack with CoW support

The [Copy-on-Write][18] stack was rebuilt on top of the latest upstream changes.

## Health and Activity

The SIG continues to maintain a healthy development pace.

### Meetings

The SIG holds regular [bi-weekly meetings][19] on Wednesdays at 16:00 UTC. Meetings are logged and the minutes for past meetings are [available][20].

The SIG uses the [`#centos-hyperscale`][21] IRC channel for ad-hoc communication and work coordination; this channel is also bridged on Matrix in the [`#centos-hyperscale:fedoraproject.org`][22] room. For async discussions and announcements we generally use the [centos-devel][23] mailing list. The SIG also holds open [monthly video conference sessions][24] to promote collaboration and social interaction.

### Conference talks

Last quarter, Davide Cavalca presented an update on SIG activities at [CentOS Dojo, Summer 2022][25] ([slides][26], [video][27]).

A number of SIG members plan to attend [CentOS Dojo, DevConf.US 2022][28] and [DevConf.US 2022][29] in Boston next month. Davide Cavalca has submitted another update on SIG activities there, and Neal Gompa has submitted a talk to introduce image building. We also plan to hold a Hyperscale meetup alongside these events, likely on August 16th. Details will be shared as soon as the venue is finalized.

A SIG-adjacent talk around [CentOS Stream][30] will be presented at [SCALE 19x][31] later this month.

### Live streams

The SIG periodically does work live on Twitch from [its official Twitch channel][32]. Interested parties who want to watch and interact with us as we do work should follow us on Twitch to get notified for when we stream.

### Planned work

The SIG tracks pending work as issues on our [Pagure repository][33]. Notable projects currently in flight include:

- using CBS to build our spin images
- shipping an updated QEMU package in EPEL
- integrate btrfs transactional updates as an optional feature
- publish spin images for CentOS Stream 9

## Issues for the Board

We have no issues to bring to the board’s attention at this time.

--------------------------------------------------------------------------------

via: https://blog.centos.org/2022/07/centos-hyperscale-sig-quarterly-report-for-2022q2/

作者：[CentOS Blog][a]
选题：[lkxed][b]
译者：[译者ID](https://github.com/译者ID)
校对：[校对者ID](https://github.com/校对者ID)

[a]: https://blog.centos.org
[b]: https://github.com/lkxed
[1]: https://blog.centos.org/2022/04/centos-hyperscale-sig-quarterly-report-for-2022q1/
[2]: https://wiki.centos.org/SpecialInterestGroup/Hyperscale
[3]: https://wiki.centos.org/SpecialInterestGroup/Hyperscale#Membership
[4]: https://pagure.io/centos-sig-hyperscale/package-bugs
[5]: https://sigs.centos.org/hyperscale/
[6]: https://sigs.centos.org/hyperscale/internal/containers
[7]: https://sigs.centos.org/hyperscale/eln_extras
[8]: https://sigs.centos.org/hyperscale/internal/systemd
[9]: https://sigs.centos.org/hyperscale/internal/ci
[10]: https://sigs.centos.org/hyperscale/internal/governance
[11]: https://sigs.centos.org/hyperscale/internal/documentation/
[12]: https://pagure.io/centos-sig-hyperscale/containers-releng/pull-request/4
[13]: https://bugzilla.redhat.com/show_bug.cgi?id=2082686
[14]: https://bugzilla.redhat.com/show_bug.cgi?id=2091640
[15]: https://pagure.io/centos-sig-hyperscale/package-updates
[16]: https://wiki.centos.org/Sources#Message_Broker_.28MQTT.29
[17]: http://git.centos.org
[18]: https://fedoraproject.org/wiki/Changes/RPMCoW
[19]: https://www.centos.org/community/calendar/#hyperscale-sig
[20]: https://sigs.centos.org/hyperscale/internal/meetings/
[21]: https://wiki.centos.org/irc#A.23centos-hyperscale
[22]: https://matrix.to/#/#centos-hyperscale:fedoraproject.org
[23]: https://lists.centos.org/mailman/listinfo/centos-devel
[24]: https://www.centos.org/community/calendar/#hyperscale-sig-monthly-hangout
[25]: https://wiki.centos.org/Events/Dojo/Summer2022
[26]: https://wiki.centos.org/Events/Dojo/Summer2022?action=AttachFile&do=view&target=Hyperscale+SIG+update%2C+June+2022.pdf
[27]: https://youtu.be/P5vMYIjzWOY
[28]: https://wiki.centos.org/Events/Dojo/DevConfUS2022
[29]: https://www.devconf.info/us
[30]: https://www.socallinuxexpo.org/scale/19x/presentations/building-future-centos-stream
[31]: https://www.socallinuxexpo.org/scale/19x
[32]: https://www.twitch.tv/centoshyperscale
[33]: https://pagure.io/centos-sig-hyperscale/sig/issues
