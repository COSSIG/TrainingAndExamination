[#]: subject: "CentOS Automotive SIG: First Year in Review"
[#]: via: "https://blog.centos.org/2022/08/centos-automotive-sig-first-year-in-review/"
[#]: author: "CentOS Blog https://blog.centos.org"
[#]: collector: "lkxed"
[#]: translator: "L-Cysteine"
[#]: reviewer: " "
[#]: publisher: " "
[#]: url: " "

CentOS Automotive SIG: First Year in Review
======

In August 2021, the [CentOS Automotive SIG][1] launched and held its first meeting with 36 participants. We had no infrastructure, no solid architectural plans, and no documentation - just a very motivated group that very quickly grew beyond Red Hat and into the automotive community.

Things have certainly changed since then! Technical lead Pierre-Yves Chibon has provided a list of the many accomplishments over the past year:

- **AutoSD**, a CentOS-Stream based linux distribution which is the public, in-development version of the Red Hat In-Vehicle Operating System (similar to CentOS Stream for RHEL).
- An **Automotive SIG RPM repository** that allows the community to expand the content of AutoSD or experiment with some of its parts.
- **Sample images**, built using OSBuild, which provide examples of how to assemble production images based on AutoSD, customized for some hardware, including container images, based on CoreOS/ostree technologies.

- [Updating OStree images][10]
- [Unattended updates roll out][11]
- [How to customize your image][12]
- [Embedding containers in your image][13]
- [Encrypting your image][14]
- [Using your Raspberry Pi 4 as a USB gadget][15]

- We worked to define what the Automotive SIG is producing and we landed on three artifacts:
- We created a [repository][2] on gitlab, with the infrastructure to enable CI/CD for a basic distribution.
- We worked with the [CentOS Infrastructure team][3] to enable the use of gitlab namespaces for SIGs under the main “CentOS” namespace on gitlab.com. [Documentation available][4]
- We worked with the [CentOS Infrastructure team][3] to enable flat dist-git layout, allowing easy backporting of work done in Fedora but also a consistent developer experience for people working on Fedora, CentOS-stream and in the Automotive SIG.
- Similarly, we've worked with the [CentOS Infrastructure team][3] to allow the lookaside cache used by SIGs to support the same structure as the lookaside cache used in Fedora and in CentOS Stream. All of this work is now available to all CentOS SIGs (as opt-in) and is [fully documented][5].
- We picked the [Raspberry Pi 4][6] as our first demo hardware to support as it is (well, as it was…). We have included support for this hardware in the [kernel-automotive][7] package available both in the Automotive SIG RPM repository as well as in AutoSD itself.
- We are building a set of [nightly images][8] for different use-cases.
- For every merge-request opened against the repository hosting the definition of our [sample images][9], we have CI running,validating that the changes we make do not break the building of our images
- Finally, we worked on documenting a large number of use cases, such as:

While we are proud of this work so far, it is just the beginning as we develop our relationships with other communities, including [SOAFEE][16] and [Eclipse SDV][17], and further refine AutoSD. We hope to see you at a [future meeting][18], or on our [mailing list][19] and [Matrix chat][20].

--------------------------------------------------------------------------------

via: https://blog.centos.org/2022/08/centos-automotive-sig-first-year-in-review/

作者：[CentOS Blog][a]
选题：[lkxed][b]
译者：[译者ID](https://github.com/译者ID)
校对：[校对者ID](https://github.com/校对者ID)

[a]: https://blog.centos.org
[b]: https://github.com/lkxed
[1]: https://wiki.centos.org/SpecialInterestGroup/Automotive
[2]: https://gitlab.com/CentOS/automotive
[3]: https://docs.infra.centos.org/infra/team/
[4]: https://sigs.centos.org/guide/gitlab/
[5]: https://sigs.centos.org/guide/git/
[6]: https://www.raspberrypi.com/products/raspberry-pi-4-model-b/
[7]: https://gitlab.com/CentOS/automotive/src/kernel
[8]: https://sigs.centos.org/automotive/download_images/
[9]: https://gitlab.com/CentOS/automotive/sample-images
[10]: https://sigs.centos.org/automotive/building/updating_ostree
[11]: https://sigs.centos.org/automotive/building/unattended_updates
[12]: https://sigs.centos.org/automotive/building/customize_template/
[13]: https://sigs.centos.org/automotive/building/containers/
[14]: https://sigs.centos.org/automotive/building/encryption/
[15]: https://sigs.centos.org/automotive/building/gadget/
[16]: https://soafee.io
[17]: https://sdv.eclipse.org
[18]: https://wiki.centos.org/SpecialInterestGroup/Automotive/Meetings
[19]: https://lists.centos.org/mailman/listinfo/centos-automotive-sig/
[20]: https://app.element.io/#/room/#centos-automotive-sig:fedoraproject.org
