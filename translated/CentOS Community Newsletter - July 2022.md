[#]: subject: "CentOS Community Newsletter, July 2022"
[#]: via: "https://blog.centos.org/2022/07/centos-community-newsletter-july-2022/"
[#]: author: "CentOS Blog https://blog.centos.org"
[#]: collector: "lkxed"
[#]: translator: "yzuowei"
[#]: reviewer: " "
[#]: publisher: " "
[#]: url: " "

CentOS社区简讯， 2022年7月
======

## 项目新闻

### 夏日道场视频

我们在6月17日举办了一个[线上道场][1] 。 [座谈视频][2]现已可以观看了。

### DevConf 道场

CentOS 正在 [DevConf.US][3] 举办一个面对面道场。道场是一个无需花钱的迷你会议，这里将有许多以 Enterprise Linux 生态为主题的议程。这次道场将于8月17日波士顿大学举行。登记免费但是强烈推荐。我们在附近的住宿旅馆也有已经预定好的房间。详情请看[活动页面][4]。

演讲征集将持续至7月22日。我们很高兴能听到你对 CentOS 的体验和分享。

### 超大规模兴趣小组 （Hyperscale SIG） 聚会

CentOS 超大规模小组将会在2022年8月16日波士顿大学举办一个面对面聚会。聚会会跟8月17日的 CentOS 道场和8月18日至20日的 DevConf.us 在同一个地点举行。这次聚会对所有感兴趣的人开放——你不需要是特别兴趣小组的一员，我们欢迎所有感兴趣的人参与。

这次活动将会在波士顿大学的 GSU 310会议室举行，持续时间从上午9点到下午5点。虽然这是一次面对面活动，我们会尽我们最大努力去搭建一个会议桥，这样即便是远程参与者的也能够参加和互动。

请在 [https://www.eventbrite.com/e/centos-hyperscale-sig-meetup-dojodevconfus-2022-tickets-384259589777][5] 登记以帮助我们更好的规划这次活动。

### CentOS 持续集成 (CI)

CentOS 持续集成将会去硬件化。CentOS 持续集成团队将会淘汰已经到达生命末期的硬件。他们将会借此机会来现代化基础架构并转移到混合云环境。

[阅读公告][6]并观看 [有关CentOS 持续集成的道场议程][7]的视频。

### 替代镜像兴趣小组 (Alternate Images SIG) 提议

Troy Dawson 提议了成立[替代镜像特别兴趣小组][8]。这个兴趣小组将生产不由核心 CentOS Stream 负责的 ISO 镜像，其中包括自生镜像和替代安装镜像。讨论还在进行中。

## 特别兴趣小组报告

我们在每个月都会发布来自我们的[特别兴趣小组][9]轮流选出的季度报告。这个月的报告分别来自兴趣小组软件合集组，超大规模组， 内核模块组，以及汽车小组。

### 软件合集兴趣小组 (Software Collections SIG)

#### 目标

为各式软件合集以及相关工具提供一个上流开发环境。提供 RedHat 为 CentOS 著作并发布的合集包。

#### 成员

无成员变动。我们永远欢迎新的成员，期待他们能为缓解以下问题贡献力量。

#### 发布和安装包

上个季度无重大发布。RedHat 安装包被半常规地重建并发布。

#### 健康与活动

此小组大部分成员表现消极，成员主要专注于重建和维护现有的安装包。组内仅有一名活跃成员 (jstanek)，而这体现在各个地方：

- 网站 https://softwarecollections.org 依然在线，但其内容已经过时；目前服务存在技术问题妨碍了登录和内容更新。
- CentOS 基础架构的变化导致了破碎的持续集成；重建安装包不再被自动测试。目前已计划修复此问题，但完成时间未知。

简单来说，工作量的增长已经超出了 jstanek 的能力。我们非常欢迎新的成员。

### 超大规模兴趣小组 (Hyperscale SIG)

超大规模小组已经在 [CentOS 博客][9]中更新了他们的季度报告。

### 内核模块兴趣小组 (Kmods SIG)

这份报告涵盖了自上次报告以来发生的工作。上次报告可以在[这里][10]找到。

#### 目标

打包并维护 CentOS Stream 和 Enterprise Linux 的内核模块。

#### 成员更新

自上次报告以来无新成员加入。我们欢迎任何感兴趣并愿意做兴趣小组职责范围内工作的人加入并贡献。

#### 对 CentOS Stream 9 / EL9 的支持

内核模块小组为 CentOS Stream 9 提供了安装包， 当 EL9 进入社区构建服务时 (CBS) 也会为 EL9 一并提供。

#### 对 CentOS Stream 8 / EL8 的支持

内核模块小组会持续为 CentOS Stream 8 和 EL8 提供安装包。

#### 新安装包

在 [内核模块小组文档][11]处查看可下载的安装包列表。这份文档也提供了进一步的信息，例如如何启用内核模块小组仓库。

注意内核模块小组提供的内核模块上还没有密匙签名。所以启用这些模块需要关闭安全启动。

任何与安装包相关的问题请在 [gitlab.com/CentOS/kmods][12] 中对应项目下反馈，如果问题不与任何安装包相关请在[这里][13]反馈。

#### 近期活动

内核模块小组目前正在将其资源转移至 [gitlab.com/CentOS/kmods][12]。迁移 gitlab.com 允许我们使用 GitLab 的持续集成来自动检测由于内核应用二进制接口 (kABI) 变化而导致的内核模块重建，也就是说，现在所有内容都是公开的，所有人都可以看到发生了什么。我们也改变了一些内核模块仓库的结构。在合适的地方我们会安排专门的 source-git 和 dist-git 仓库，dist-git 是从 source-git 自动生成的，手动改变只会发生在 source-git 仓库。这些改变的实施是为了让每个人都尽可能简单地去贡献代码或是修复漏洞。

#### 健康与活动

内核模块小组保持着一个健康的开发节奏。

#### 交流

常规会议会在 #centos-meeting 举行，时间是每个月的第一周的星期一 1600 UTC。每个人都欢迎加入！你也可以在任何时候从 #centos-kmods 联系到小组成员。

#### 公开问题

- **内核模块签名：**这需要基建小组 (Infra SIG) 的合作和进一步讨论。特别是如何安全地存储社区构建服务可以使用的兴趣小组专用钥匙，但未经授权人员无法访问。
- **驱动光盘：**小组想要提供在未支持设备上安装 CentOS Stream 所需要的驱动光盘。[此处][14]可以追踪进度。

#### 对理事会的问题

内核模块小组要求有关特别兴趣小组为 RHEL 8 和 9 创造内容的可能性的澄清。公开问题包括了对发布包的支持，详见标签 extras-common，和多久后特别兴趣小组可以开始搭建 RHEL，例如，直到 RHEL 生命周期的 "Full Support" 或 "Maintenance Support"结束。

### 汽车兴趣小组 (Automotive SIG)

#### 成员更新

小组没有正式成员加入。邮件列表里有94名订阅者代表至少30家组织，虽然不是所有订阅者都使用企业邮箱，也有人是以个人名义参加的。

#### 最近季度发布 （或最近发布，季度内可能无发布）

小组提供了一个新的发行版：Automotive Stream 发行版 (AutoSD)，一个 CentOS Stream 衍生版本旨在满足汽车 OS 的需求，延伸至 Red Hat 最终的车载 OS 产品的上流项目。AutoSD 已经被多个组织下载和使用，他们都已做出评价或提出问题，所以我们知道 AutoSD 具备一定吸引力，当然我们没有具体的使用数据。

#### 健康报告和常规活动陈述

小组每个月有两个公开会议，一个正式会议以及一个非正式的“办公室时间”，每个会议都有25到40人参加，以及7到10个不同的组织。此小组是一项社区成果，其代表着所有参与者的贡献与共同利。全部正式会议都被记录并刊登在以下页面：
[https://wiki.centos.org/SpecialInterestGroup/Automotive/Meetings][15]

几名 Red Hat 员工对项目做出了最初贡献，他们也提供了构建和测试所需的基建。我们占用了一个 gitlab 仓库使用持续集成来常规地构建软件，构建指南在文档页面 [https://sigs.centos.org/automotive/][16]。例图已呈现并可以与定制与构建指南一起被下载。

这是目前活动的高度总结：

- 所有工作都已被移植到 GitLab 上 CentOS 的命名空间下，这是为了巩固我们作为社区项目的愿景：[https://gitlab.com/centos/automotive][17]
- 持续集成|持续部署 (CI/CD) 基建已经就位
- 固件体积已被减小
- 已经可以通过 LUKS 加密
- 正在为安卓设备开发 Linux chroot
- 清单现在启用了 EFI 运行服务
- 避开缓存结构
- 镜像可下载：[https://autosd.sig.centos.org/][18]
- 得力于社区和企业的共同贡献，文档现已被大幅扩展：[https://sigs.centos.org/automotive/][16]
- 文档现在包括了详细的贡献指南：[https://sigs.centos.org/automotive/contributing/contributing-to-auto-sig-repo/][19]
- 会议内正在进行的讨论集中在已支持的硬件和对文档的期望
- 新的会议页面包含了全部会议记录：[https://wiki.centos.org/SpecialInterestGroup/Automotive/Meetings][15]
- 得力于来自 Fedora 一些帮助， 同步交流已从 IRC 转移到 Matrix：[https://app.element.io/#/room/#centos-automotive-sig:fedoraproject.org][20]

#### 任何对理事会的问题

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
