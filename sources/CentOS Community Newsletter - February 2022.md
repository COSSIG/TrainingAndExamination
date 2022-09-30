[#]: subject: "CentOS Community Newsletter, February 2022"
[#]: via: "https://blog.centos.org/2022/02/centos-community-newsletter-february-2022/"
[#]: author: "CentOS Blog https://blog.centos.org"
[#]: collector: "lkxed"
[#]: translator: " "
[#]: reviewer: " "
[#]: publisher: " "
[#]: url: " "

CentOS Community Newsletter, February 2022
======

## Project News

### FOSDEM Dojo

CentOS hosted its annual [FOSDEM Dojo][1]. This Dojo was once again virtual. If you missed the Dojo, or you just want to watch it again, all of the videos (and some of the slides) are available on the [Dojo wiki page][2].

Also, Aleksandra Fedorova gave a talk at FOSDEM called [CentOS Stream: stable and continuous][3]. This excellent talk went into details of how CentOS is actually built.

### CentOS Linux 8

Following on the EOL of CentOS Linux 8 last year, the packages for CentOS Linux 8 were removed from the mirror network and placed in the vault at the end of January. If you still need to migrate from CentOS Linux 8 to CentOS Stream 8, see the [updated instructions on centos.org][4].

## SIG Reports

[Special Interest Groups][5] (SIGs) are the most interesting part of the CentOS project - this is where people build value on top of the CentOS platform. SIGs report quarterly on what they’ve been up to. Here are this month’s reports.

### Cloud

#### Purpose

The [Cloud SIG][6] is responsible for packaging and maintaining different FOSS based Private cloud infrastructure applications that one can install and run natively on CentOS.

#### Releases and Packages

**Retirement of CentOS 8**

The Cloud SIG has been working on the removal of all jobs and repositories that were utilizing CentOS 8 and moving any remaining jobs to CentOS Stream 8.

**Preparation for CentOS Stream 9** The Cloud SIG has been working with the OpenStack Technical Committee and community to coordinate the Yoga release, planned for March 2022, to be on CentOS Stream 9. To achieve this goal, some preparations tasks are being carried out in the RDO Project:

- OpenStack dependencies have been built for CentOS Stream 9 and preparation to build OpenStack Yoga versions is in progress.
- Those packages are being validated to find potential issues early, report them, and propose fixes when possible.
- Coordination with upstream projects that require relevant changes to support the new CentOS Stream.

#### Meetings and communication

The periodic meeting has been rescheduled from the first Thursday of the month to the second Thursday of the month at 1500 UTC in #centos-meeting. This move was made to alleviate a scheduling overlap with the Fedora Cloud SiG and encourage cross project collaboration.

### NFV

#### Purpose

The CentOS [NFV (Network Function Virtualization) SIG][7] provides a CentOS-based stack that will serve as a platform for the deployment and testing of virtual network functions (VNFs) and NFV component packages on compliant CentOS platform.

#### Membership Update

No changes.

#### Overall update

NFV SIG keeps updating openvswitch 2.13, 2.15 and 2.16 and OVN for CentOS Stream 8 and CentOS Stream 9.

Packages openvswitch2.15, openvswitch2.16 and ovn-2021 have been pushed to official CentOS Stream 9 mirrors and are available for users.

#### Issues for the Board

No issues to report to the Board.

### Storage

#### Purpose

The [Storage SIG][8] is a collection of like-minded individuals coming together to ensure that CentOS is a suitable platform for many different storage solutions. This group will ensure that all Open Source storage options seeking to utilize CentOS as a delivery platform have a voice in packaging, orchestration, deployment, and related work.

#### Package Updates

**CentOS 7:**

- NFS-Ganesha-4.0 and (lib)ntirpc-4.0 have been released.

**CentOS 8:**

- NFS-Ganesha-4.0 and (lib)ntirpc-4.0 have been released.
- Have asked for build+release of centos-release-ceph-quincy for the upcoming release.
- Have asked for build+release of centos-release-nfs-ganesha4.

**CentOS Stream 8:**

- Ceph Pacific and the related cephadm package v16.2.7 has been released
- NFS-Ganesha-4.0 and (lib)ntirpc-4.0 have been released.
- Have asked for build+release of centos-release-ceph-quincy for the upcoming release.
- Have asked for build+release of centos-release-nfs-ganesha4.

**CentOS Stream 9:**

- Ceph Pacific and the related cephadm package v16.2.7 has been released
- NFS-Ganesha-4.0 and (lib)ntirpc-4.0 have been released.
- Centos-release-storage-common, centos-release-ceph-pacific, and centos-release-ceph-quincy have been released.
- Centos-release-nfs-ganesha4 has been released.

**Misc:**

- cephadm subpackage was unbundled from ceph on stream-9 to support ceph’s upstream CI facility. Francesco Pantano (fmount) builds the cephadm package.
- The OpenStack upstream CI promoted Ceph pacific v16.2.7 on both stream-8 and stream-9 with the related cephadm version.

### Messaging

#### Purpose

The [Messaging SIG][9] is responsible for packaging and maintaining messaging related projects to be consumed e.g by the OpsTools SIG or the Cloud SIG.

#### Membership Update

No change. As always, more hands would be helpful.

#### Overall update

We have rebuilt and refreshed packages for CentOS Stream 8.

#### Issues for the Board

None to bring forward at the moment.

--------------------------------------------------------------------------------

via: https://blog.centos.org/2022/02/centos-community-newsletter-february-2022/

作者：[CentOS Blog][a]
选题：[lkxed][b]
译者：[译者ID](https://github.com/译者ID)
校对：[校对者ID](https://github.com/校对者ID)

[a]: https://blog.centos.org
[b]: https://github.com/lkxed
[1]: https://wiki.centos.org/Events/Dojo/FOSDEM2022
[2]: https://fosdem.org/2022/schedule/event/centos_stream_stable_and_continuous/
[3]: https://www.centos.org/centos-stream/
[4]: https://wiki.centos.org/SpecialInterestGroup
[5]: https://wiki.centos.org/SpecialInterestGroup/Cloud
[6]: https://wiki.centos.org/SpecialInterestGroup/NFV
[7]: https://wiki.centos.org/SpecialInterestGroup/Storage
[8]: https://wiki.centos.org/SpecialInterestGroup/Messaging
