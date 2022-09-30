[#]: subject: "CentOS Community Newsletter, May 2022"
[#]: via: "https://blog.centos.org/2022/05/centos-community-newsletter-may-2022/"
[#]: author: "CentOS Blog https://blog.centos.org"
[#]: collector: "lkxed"
[#]: translator: " "
[#]: reviewer: " "
[#]: publisher: " "
[#]: url: " "

CentOS Community Newsletter, May 2022
======

## Project News

### Online Summer Dojo

CentOS will be holding a free online [Dojo on June 17][1]. CentOS Dojos are mini conferences highlighting the work within the project and across the entire ecosystem. Registration is free but required. We invite everybody to join us.

The call for presentations is open. We welcome presentations about CentOS Stream, CentOS SIGs, RHEL, and projects built on top of CentOS.

## SIG Reports

CentOS Special Interest Groups focus on work around CentOS Stream. Each SIG reports quarterly in this newsletter.

### Storage SIG

Package updates since the last report:

- Glusterfs updated to glusterfs-9.5 and glusterfs-10.1; packages are available for Stream 9 and Stream 8.
- Ceph Quincy (17) was released; packages are available for Stream 9, Stream 8, and RHEL8.
- Ceph Pacific (16) updated to ceph-16.2.7, with 16.2.8 expected any day now; packages are available for Stream 9, Stream 8, and RHEL8.
- Ceph Octopus (15) was updated to 15.2.16; packages are available for Stream 8 and RHEL8.
- NFS-ganesha-4 and libntirpc-4 were released; packages are available for Stream 9, Stream 8, RHEL8, and CentOS 7. NFS-Ganesha-3 is now EOL upstream.

New packages in the Storage SIG:

- Apache Arrow (libarrow-7.0.0) and Apache ORC (liborc-1.7.4) and their dependencies are now in the Storage SIG. Ostensibly they are provided as dependencies for Ceph Quincy. Packages are available for Stream 9, Stream 8, and RHEL8.

### Cloud SIG

#### Purpose

Packaging and maintaining different FOSS based Private cloud infrastructure applications that one can install and run natively on CentOS.

[https://wiki.centos.org/SpecialInterestGroup/Cloud][2]

#### Membership update

New Chair elected - Joel Capitao.

Thank you Alfredo for all your hard work this past year.

#### Releases in the most recent quarter (or most recent release, if none in that quarter)

#### RDO

April 27 2022 - Yoga release [https://blogs.rdoproject.org/2022/04/rdo-yoga-released/][3]

In the last few months, the SIG worked hard on bootstrapping Yoga OpenStack release onto CentOS Stream 9. The initial plan was to release Xena onto CS9 but because of bad timing due to uncertainty about CS GA plans, we coudln’t make it. The positive point is that we had more time to add CS9 as the supported Operating System to the OpenStack project.

Adding CS9 to OpenStack CI provided valuable feedback as it allowed us to catch issues early in the CI, it was challenging but proved valuable. Note that RDO will use Yoga as a transitive Openstack release with Cloud Stream 8 and Cloud Stream 9 support, in order to be able to migrate the OS from one to another. The next OpenStack release, Zed, will be supported only on CentOS Stream 9.

#### Continuous Integration

Cloud SIG had migrated all their jobs from older jenkins instance ([ci.centos.org][4]) to a new private instance running in the CentOS CI OpenShift environment ([https://jenkins-cloudsig-ci.apps.ocp.ci.centos.org/][5])

Last but not least, RDO related CI pipelines which required only x86_64 nodes have been migrated to RDO Zuul CI/CD environment in order to reduce node requests.

#### Health and activity

The Cloud SIG remains fairly healthy. However, it is still, for the most part, a monoculture containing only OpenStack.

--------------------------------------------------------------------------------

via: https://blog.centos.org/2022/05/centos-community-newsletter-may-2022/

作者：[CentOS Blog][a]
选题：[lkxed][b]
译者：[译者ID](https://github.com/译者ID)
校对：[校对者ID](https://github.com/校对者ID)

[a]: https://blog.centos.org
[b]: https://github.com/lkxed
[1]: https://wiki.centos.org/Events/Dojo/Summer2022
[2]: https://wiki.centos.org/SpecialInterestGroup/Cloud
[3]: https://blogs.rdoproject.org/2022/04/rdo-yoga-released/
[4]: https://ci.centos.org
[5]: https://jenkins-cloudsig-ci.apps.ocp.ci.centos.org/
