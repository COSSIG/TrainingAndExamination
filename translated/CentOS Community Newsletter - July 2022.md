[#]: subject: "CentOS Community Newsletter, July 2022"
[#]: via: "https://blog.centos.org/2022/07/centos-community-newsletter-july-2022/"
[#]: author: "CentOS Blog https://blog.centos.org"
[#]: collector: "lkxed"
[#]: translator: "yzuowei"
[#]: reviewer: " "
[#]: publisher: " "
[#]: url: " "

CentOS社区快报， 2022年7月
======

## 项目新闻

### 夏日道场视频

我们在6月17日举办了一个[在线道场][1] 。 [座谈视频][2]现在已经可以观看了。

### 开发大会道场

CentOS 正在 [DevConf.US][3] 举办一个面对面道场。道场是一个免费的小型会议讨论有关企业 Linux 生态系统的各种各样的议题。这次道场将在8月17日于波士顿大学举行。登记是免费的但我们强烈推荐。我们在附近的住宿旅馆也有预定的房间。详情请看[活动页面][4]。

演讲征集将持续至7月22日。我们很高兴能听到你对 CentOS 的体验和分享。

### Hyperscale SIG 聚会

CentOS Hyperscale SIG 将会在2022年8月16日波士顿大学举办一个面对面聚会。聚会会跟8月17日的 CentOS 道场和8月18-20日的 DevConf.us 在同一个地方举行。这次聚会对所有感兴趣的人开放 - 你不需要是 SIG 的一员，我们欢迎所有人的参与。

这次活动将会在波士顿大学的 GSU 310会议室举行，持续时间从上午9点到下午5点。虽然这是一次面对面活动，我们会尽我们最大努力去搭建一个会议中心，这样远程参与者的也能够参加和互动。

请在 [https://www.eventbrite.com/e/centos-hyperscale-sig-meetup-dojodevconfus-2022-tickets-384259589777][5] 登记，这样我们可以更好的规划这次活动。

### CentOS CI

CentOS CI 将会去硬件化。CentOS CI 团队将会淘汰硬件因为硬件已经到达生命末期了。他们将会借此机会来现代化基础架构并转移到混合云平台。

[阅读声明][6]并观看 [CentOS CI 的道场议程][7]的视频。

### 替代镜像 SIG 提议

Troy Dawson 提议了成立[替代镜像特别兴趣小组][8]。这个 SIG 将生产不由核心 CentOS Stream 生产的 ISO 镜像，其中包括自生镜像和替代安装镜像。讨论还在进行中。

## SIG 报告

每个月，我们都会发布来自我们[特殊兴趣小组][9]的轮流选出的季度报告。这个月包括了来自 Software Collections, Hyperscale, Kmods 以及 Automotive SIGs 的报告。

### 软件合集 SIG

#### 目的

为各样的软件合集和相关工具提供一个上流开发环境。提供 RedHat 为 CentOS 著作并发布的合集包。

#### 成员制度

成员制度不变。我们永远欢迎新的成员，而他们会帮助缓解以下提出的问题。

#### 发布和包

上个季度没有重要发布。RedHat 包半常规地重建并发布。

#### 健康与活跃度

这个组大部分是消极的，主要专注于重建和维护现有的包。组内仅有一名活跃的成员 (jstanek)，而这体现在各个地方：

- 网站 https://softwarecollections.org 依然在线，但其内容已经过时；目前服务存在技术问题妨碍了登录和内容更新。
- CentOS 基础架构的变化导致了破碎的 CI；重建的包不再被自动测试。修复此问题已在计划中，但还没有 ETA。

简单来说，工作量的增长已经超出了 jstanek 的能力。我们非常欢迎新的成员。

### Hyperscale SIG

Hyperscale SIG 已经在 [CentOS博客][9]里更新了他们的季度报告。

### Kmods SIG

这份报告覆盖了自从上次报告以来发生的工作。上次报告能在[这里][10]找到。

#### 目的

打包并维护 CentOS 流和企业 Linux 的内核模块。

#### 成员制度更新

自上次报告以来没有 SIG 成员被加入。我们欢迎任何感兴趣并愿意做 SIG 范围内工作的人加入并参与贡献。

#### 对 CentOS Stream 9 / EL9 的支持

Kmods SIG 为 CentOS Stream 9 提供了包， 也将会为 EL9 提供一旦 EL9 在 CBS 内存在。

#### 对 CentOS Stream 8 / EL8 的支持

Kmods SIG 会持续为 CentOS Stream 8 和 EL8 提供包。

#### 新的包

在 [Kmods SIG 的文档][11]处看可得到的包的列表。这份文档也提供了进一步的信息，比如如何启用 Kmods SIG 的库。

注意由 Kmods SIG 提供的内核模块还没有密匙签名。所以我们需要关掉安全启动来使用其中任意的内核模块。

如果遇到任何这些包的问题请在 [gitlab.com/CentOS/kmods][12] 的对应项目页面回报，如果遇到的问题不与任何包相关请在[这里][13]回复。

#### 近期活动

Kmods SIG 目前正在将其资源移至 [gitlab.com/CentOS/kmods][12]。转向 gitlab.com 允许我们使用 GitLab CI 来自动检测由于 kABI 变化而导致的内核模块重建，即，现在所有内容都是公开的，所有人都可以看到发生了什么。我们也改变了一些内核模块库的结构。在合适的地方我们会有专门的 source-git 和 dist-git 库，dist-git 是从 source-git 自动生成的，手动改变只会发生在 source-git 库。这些改变的实施是为了让每个人都尽可能简单的去贡献代码或是修复漏洞。

#### 健康与活跃度

Kmods SIG 维持着一个健康的开发节奏。

#### 交流

常规会议会在每个月的第一周的周一 1600 UTC 举行，位于 #centos-meeting。每个人都欢迎加入！你也可以在任何时候从 #centos-kmods 接触到 SIG 成员。

#### 公开问题

- **内核模块签名：**这需要 Infra SIG 的合作与进一步讨论。特别是如何安全地存储 CBS 可以使用的 SIG 特殊钥匙，但未经授权人员无法访问。
- **驱动硬盘：** SIG 想要提供在不支持设备上安装 CentOS Stream 所需要的驱动硬盘。目前状态可在 [此处][14] 追踪。

#### 需要委员会解决的问题

Kmods 询问了关于 SIGs 为 RHEL 8 和 9 创造内容的可能性的澄清。公开问题包括了对发布包的支持，详见标签 extras-common，以及 多久后 SIGs 可以开始搭建 RHEL，例如，直到“完全支持”或“维护支持”的 RHEL 生命末期。

### Automotive SIG

#### 成员制度更新

此 SIG 无正式成员加入流程。邮件列表里有94名订阅者来自至少30家组织，虽然不是所有订阅者都使用企业邮箱，也有人是以个人名义参加的。

#### 最近季度发布 （或最近发布，季度内可能无发布）

SIG 提供了一个新的发行版：Automotive Stream 发行版 (AutoSD)，一个 CentOS Stream 衍生版本旨在满足自动驾驶 OS 的需求，延伸至 Red Hat 最终的车载 OS 产品的上流项目。AutoSD 已经被多个组织下载和使用，他们都已做出评价或提出问题，所以我们知道 AutoSD 具备一定吸引力，当然我们没有具体的使用数据。

#### 健康报告和常规活动陈述

SIG 每个月有两个公开会议，一个正式会议以及一个非正式的“办公室时间”，每个会议都有25-40人参加，其中有来自7-10个不同组织。此 SIG 是所有参与者的贡献与共同利益的社区成果。全部正式会议都被记录并在一下页面发布：
[https://wiki.centos.org/SpecialInterestGroup/Automotive/Meetings][15]

几名 Red Hat 员工对项目做出了最初贡献，他们也提供了搭建和测试所需要的基础设施。我们占用了一个 gitlab 库用以搭建软件并常规使用 CI，搭建指南在文档页面 [https://sigs.centos.org/automotive/][16]。例图已呈现并可以与定制与搭建指南一起被下载。

这是目前活动的高度总结：

- 所有工作已经被转移到 GitLab 上 CentOS 的命名空间下，这是为了巩固我们作为社区项目的愿景：[https://gitlab.com/centos/automotive][17]
- CI/CD 基础设施已经就位
- 固件体积已被减小
- 已经可以通过 LUKS 加密
- Linux chroot 已经能在安卓设备上工作
- 清单现在启用了 EFI 运行服务
- 避开缓存结构
- 镜像可下载：[https://autosd.sig.centos.org/][18]
- 得力于社区与企业的贡献，文档现已被大幅扩展：[https://sigs.centos.org/automotive/][16]
- 文档现在包括了详细的贡献指导：[https://sigs.centos.org/automotive/contributing/contributing-to-auto-sig-repo/][19]
- 会议内正在进行的讨论集中在已支持的硬件和对文档的期望
- 新的会议页面包含了全部会议记录：[https://wiki.centos.org/SpecialInterestGroup/Automotive/Meetings][15]
- 得力于来自 Fedora 一些帮助， 实时交流已从 IRC 转移到 Matrix：[https://app.element.io/#/room/#centos-automotive-sig:fedoraproject.org][20]

#### 如果任何需要委员会知道的问题，请在此提出

没有，继续出色的工作 🙂

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
