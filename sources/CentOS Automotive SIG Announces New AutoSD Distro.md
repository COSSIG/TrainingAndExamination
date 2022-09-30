[#]: subject: "CentOS Automotive SIG Announces New AutoSD Distro"
[#]: via: "https://blog.centos.org/2022/03/centos-automotive-sig-announces-new-autosd-distro/"
[#]: author: "CentOS Blog https://blog.centos.org"
[#]: collector: "lkxed"
[#]: translator: " "
[#]: reviewer: " "
[#]: publisher: " "
[#]: url: " "

CentOS Automotive SIG Announces New AutoSD Distro
======

## Introducing the Automotive Stream Distribution

The CentOS Automotive SIG is excited to announce the Automotive Stream Distribution. This is a binary distribution developed within the SIG that serves as a public, in-development preview of the upcoming Red Hat in-vehicle OS.

In August 2021, the CentOS project announced the launch of the CentOS Automotive SIG. The purpose of this SIG is two-fold. First, it is meant to be a neutral public space for collaboration between third parties interested in open development of software targeted at in-vehicle automotive use cases. Second, it is meant to provide such projects with build and test infrastructure.

The goal of the SIG is to provide an open-source home for RHEL-oriented automotive work, and to attract and encourage open development of automotive software between commercial and non-commercial partners.

As this RHEL-oriented automotive work is being defined, it has become clear that having multiple development stages would be most beneficial. We have identified three of these stages:

- The CentOS Automotive SIG open to anyone and everyone to build, test, experiment, and contribute with software for the automotive industry.
- The Red Hat automotive product,—the product itself that Red Hat sells and supports. The SIG is where this product is being developed.
- A third place which would sit between the CentOS Automotive SIG and the product. This is a public, in development, version of the product.

This third point is what we would like to present to you today: the Automotive Stream Distribution (AutoSD).

The Automotive Stream Distribution is an upstream to the Red Hat automotive product, just as CentOS Stream is to RHEL. The Automotive Stream Distribution will be based on CentOS Stream with a few divergences where it makes sense/is required. The first of these divergences will be the Linux kernel. AutoSD will rely on the kernel-automotive package rather than CentOS Stream's kernel package.

[![][1]][2]

So the Automotive SIG will be the place where anyone and everyone can join, contribute, and experiment (e.g., the SIG supports enabling new hardware on the kernel) and benefit from the infrastructure developed around this SIG, but without engaging Red Hat (new hardware enabled in the SIG does not mean it would automatically become part of Red Hat's automotive product.)

As a binary distribution, AutoSD will thus be the place where the community, customers and/or partners will be able to see what will land in the automotive product down the line. Like CentOS Stream, Automotive Stream Distribution will be opened to contributions, using similar mechanisms.

The next Automotive SIG meeting will be held on Wednesday March 2nd at 15:00 UTC. We will discuss the Automotive Stream Distribution in that meeting, so join us!

--------------------------------------------------------------------------------

via: https://blog.centos.org/2022/03/centos-automotive-sig-announces-new-autosd-distro/

作者：[CentOS Blog][a]
选题：[lkxed][b]
译者：[译者ID](https://github.com/译者ID)
校对：[校对者ID](https://github.com/校对者ID)

[a]: https://blog.centos.org
[b]: https://github.com/lkxed
[1]: https://blog.centos.org/wp-content/uploads/2022/03/autosd.png
