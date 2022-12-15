[#]: subject: "CentOS Automotive SIG: First Year in Review"
[#]: via: "https://blog.centos.org/2022/08/centos-automotive-sig-first-year-in-review/"
[#]: author: "CentOS Blog https://blog.centos.org"
[#]: collector: "lkxed"
[#]: translator: "L-Cysteine"
[#]: reviewer: "Phodopussungorus"
[#]: publisher: " "
[#]: url: " "

CentOS 汽车小组：首年总结
======

在2021年8月，[ CentOS 汽车小组][1]成立并且进行了首次会议。此次会议共有 36 位成员参与。尽管没有基础设施、可靠的架构计划甚至文件，但是作为一个充满积极性的团队，我们迅速地在 Red Hat 之外的领域获得了进展，进入了自动驾驶的社区。

事情自此发生了巨大的转变！技术指导 Pierre-Yves Chibon 列举了过去一年里达成的众多成就：

- 我们试图阐明汽车小组目前的产品，在如下三个方面取得一定的成果：

  - **AutoSD** 基于 CentOS-Steam 的 linux 发行版。此版本（与 RHEL 的 CentOS Steam类似）是 Red Hat 车载操作系统的公开的开发中版本。
  - **Automotive SIG RPM 存储库** 社区通过该库可以扩充 AutoSD 的内容或者测试其中的某些部分。
  - **示例映像** 借助 OSbuild 构建的示例映像提供如何整合基于 AutoSD 、针对某些硬件自定义的生产过程映像的范例，包括基于 CoreOS/OSTree 技术的容器映像。

- 我们在 gitlab 上创建了一个基础架构允许基本发行版装配 CI/CD 的[存储库][2]。
- 我们与[ CentOS 基础架构团队][3]合作，使得各小组在 gitlab.com 主 “CentOS” 命名空间下能使用 gitlab 命名空间。[可用文档][4]
- 我们与[ CentOS 基础架构团队][3]合作，完成平面 dist-git 布局，从而让在 Fedora 上完成的工作能够轻松地被向后移植，也确保借助 Fedora、CentOS-Stream、Automotive SIG 工作的人员能够获得统一的开发人员体验。
-同样的，我们已经与[ CentOS 基础架构团队][3]合作，以便各小组使用的后备缓存与 Fedora 和 CentOS Stream 所采用的保持统一，支持相同的结构。所有的成果现在可供所有 CentOS 小组使用（以选择加入的形式），并且已有[详实记录][5]。
- 关于第一个支持的演示硬件，我们选择了当前未作改动的 [Raspberry Pi 4][6]（好吧，曾经的……）。我们已经在 Automotive SIG RPM 存储库和 AutoSD 中可用的[内核汽车][7]包中加入了对该硬件的支持。
- 我们正在为不同的用例构建相应的一组[夜间映像][8]。
- 对于为存有我们[示例映像]的存储库而开的每个合并请求，我们会运行 CI 来确保我们的更改不会破坏映像的构建。
- 最后，我们致力于记录大量的用例，比如：

  - [更新 OSTree 映像][10]
  - [推出无人监管的更新][11]
  - [如何自定义映像][12]
  - [在映像中嵌入容器][13]
  - [加密映像][14]
  - [使用 Raspberry Pi 4 作为 USB 部件][15]

我们为目前的工作成果感到自豪，但这仅仅是开始，因为我们正在与 [SOAFEE][16]、[Eclipse SDV][17] 等其他的社区建立关系，并且进一步完善 AutoSD 。我们希望在[未来的会议][18]或者[邮件列表][19]与[ Matrix 聊天][20]中见到你。

--------------------------------------------------------------------------------

via: https://blog.centos.org/2022/08/centos-automotive-sig-first-year-in-review/

作者：[CentOS Blog][a]
选题：[lkxed][b]
译者：[L-Cysteine](https://github.com/L-Cysteine)
校对：[Phodopussungorus](https://github.com/Phodopussungorus)

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
