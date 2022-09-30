[#]: subject: "CentOS Community Newsletter, June 2022"
[#]: via: "https://blog.centos.org/2022/06/centos-community-newsletter-june-2022/"
[#]: author: "CentOS Blog https://blog.centos.org"
[#]: collector: "lkxed"
[#]: translator: " "
[#]: reviewer: " "
[#]: publisher: " "
[#]: url: " "

CentOS Community Newsletter, June 2022
======

## Project News

### Online Summer Dojo

CentOS is hosting an [online Dojo][1] this Friday, June 17, from 14:00 to 20:00 UTC. CentOS Dojos are free miniconferences with talks on a variety of topics from CentOS and the wider Enterprise Linux ecosystem. This Dojo features seven talks, along with an informal chat with the CentOS Board of Directors.

Registration is free but required. [Register today.][2]

### DevConf Dojo

In addition to our online Summer Dojo, we are hosting an in-person [Dojo at DevConf.US][3] on August 17, the day before the main DevConf talks. The call for presentations is now open.

## SIG Reports

### Artwork SIG

#### Purpose

The CentOS Artwork SIG exists to produce the CentOS Project visual identity. See https://wiki.centos.org/SpecialInterestGroup/Artwork

#### Membership Update

There is not membership changes. We are always looking for new members.

#### Releases

None.

#### Healthy and Activity

#### Health

We are here; doing what we can, when we can.

#### Recent activities related to CentOS Symbol redesign

The [contrast issues][4] related to [CentOS Symbol redesign][5] has been addressed with the following composition:

![][6]

This design uses only two colors, the CentOS Purple (`#a14F8C`) and the CentOS White (`#ffffff`). The outer square is being considered an integral part of the symbol itself and must not be removed from it, to provide acceptable recognition on top of both dark and light backgrounds. From all the four CentOS colors available, the purple one seems to provide the best background neutrality.

Soureces related to this design are available at https://gitlab.com/areguera/centos-brand/-/tree/v2-centos-artwork-sig-issue-5 and you are welcome to contribute.

Tests related to size:

![][7]

![][8]

![][9]

![][10]

![][11]

![][12]

![][13]

![][14]

Tests related to contrast and overall presentation in default theme:

![][15]

![][16]

![][17]

![][18]

![][19]

![][20]

![][21]

Tests related to contrast and overall presentation in dark mode theme:

![][22]

![][23]

#### Recent actitivities related to CentOS word transition from Denmark to Montserrat typography

[Issue 71][24]: The images necessary to implement the transition from Denmark to Montserrat typography are already in the centos-logos repository, the upstream location used to build the centos-logo package. Please, see the content provided in release [90.7][25]. Presently, the centos-package is built based on source release [90.4][26].

The Artwork SIG cannot make changes in the centos-logo spec. We only can update the upstream repository with the images you need, and tag the changes with a new version, so for a Red Hat developer to do the source version swift.

#### Recent actitivities related to website visual corrections

It has been reported an issues related lists.centos.org visual presentation. See https://github.com/CentOS/ansible-role-mailman/issues/15.

A redesign simplification is being considered to “flatten” the web site presentation using CentOS colors only.

#### Issues for the Board

None.

### Virtualization SIG

For oVirt:

- Membership update: new members from oVirt project joined the SIG: Sharon Gratch, Eitan Raviv, Harel Braha, Lev Veyde, Yedidyah Bar David, Ori Liel (please add yourself if I missed you as joined in the last quarter)
- Releases and Packages: oVirt 4.5.0 has been released upstream using CentOS Virtualization SIG for shipping binaries except for a few packages which couldn’t build within the CentOS Community Build Service.
- Health and Activity: oVirt is pretty active.
- Issues for the Board: CentOS Stream is lacking important and critical security updates compared to already released RHEL content. An effort on making CentOS Stream more secure would be welcome (example: as of June 1st the latest kernel in CentOS Stream 8 is kernel-4.18.0-383.el8 which was built on 2022-04-20, it’s laking CVE fixes delivered over the last 40 days in RHEL 8.6)

--------------------------------------------------------------------------------

via: https://blog.centos.org/2022/06/centos-community-newsletter-june-2022/

作者：[CentOS Blog][a]
选题：[lkxed][b]
译者：[译者ID](https://github.com/译者ID)
校对：[校对者ID](https://github.com/校对者ID)

[a]: https://blog.centos.org
[b]: https://github.com/lkxed
[1]: https://wiki.centos.org/Events/Dojo/Summer2022
[2]: https://hopin.com/events/centos-dojo-summer-2022
[3]: https://wiki.centos.org/Events/Dojo/DevConfUS2022
[4]: https://git.centos.org/centos/Artwork/issue/5
[5]: https://git.centos.org/centos/Artwork/issue/1
[6]: https://i.imgur.com/Ug5ok9m.png
[7]: https://i.imgur.com/Su9doRU.png
[8]: https://i.imgur.com/ilrxist.png
[9]: https://i.imgur.com/445cl3p.png
[10]: https://i.imgur.com/yTnkgH8.png
[11]: https://i.imgur.com/h19TJya.png
[12]: https://i.imgur.com/NescFUO.png
[13]: https://i.imgur.com/MqDv5uD.png
[14]: https://i.imgur.com/nBzFCjz.png
[15]: https://i.imgur.com/oS1YskB.png
[16]: https://i.imgur.com/sN2Edpd.png
[17]: https://i.imgur.com/gjTzuDQ.jpg
[18]: https://i.imgur.com/gO8OvrR.png
[19]: https://i.imgur.com/kb5NYxx.png
[20]: https://i.imgur.com/1HC0aat.png
[21]: https://i.imgur.com/envtjj4.jpg
[22]: https://i.imgur.com/fSwrFER.jpg
[23]: https://i.imgur.com/ctFDq0Q.png
[24]: https://git.centos.org/centos/board/issue/71
[25]: https://github.com/CentOS/centos-logos/releases/tag/90.7
[26]: https://gitlab.com/redhat/centos-stream/rpms/centos-logos
