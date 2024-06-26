---
title: 管理开源项目的工具
---

开源项目工具的战略应用之路始于一个精心策划、组织有序、有实权的开源项目办公室，用以指导和管理其创建、分发和使用（开源项目）。但这只是第一步。要让这样的办公室运转顺畅，你需要正确的工具。这些至关重要的工具将用于跟踪目标和指标，涉及从工程和法务到执行领导、公关和市场营销，再到人力资源等部门，并为每个功能提供所需的所有资源，以收集数据、提供绩效快照，并管理公司内部对开源的日常使用

本指南提供了关于如何开始构建您的开源工具集的详细信息和场景，包括了解用于跟踪和管理您的开源项目的最重要工具的信息。许多工具是由Linux基金会和其他行业领先者创建并开源的，为您的项目提供了免费和便捷的访问。您还将找到一个示例仪表板设置，该设置将来自多个工具的信息汇总进行集中审查。

**Table of Contents**

- [为什么您需要特殊的工具来管理开源项目](#为什么您需要特殊的工具来管理开源项目)
- [如何选择和规划您的工具](#如何选择和规划您的工具)
  - [利用现有工具](#利用现有工具)
  - [创建仪表板](#创建仪表板)
- [基本工具集的要素](#基本工具集的要素)
  - [自动化流程](#自动化流程)
  - [管理关键任务](#管理关键任务)
  - [源代码管理](#源代码管理)
  - [许可合规性](#许可合规性)
- [管理源代码的工具](#管理源代码的工具)
  - [错误和问题跟踪](#错误和问题跟踪)
  - [归档和发布管理](#归档和发布管理)
- [项目健康跟踪工具](#项目健康跟踪工具)
  - [为了更好的代码审查：](#为了更好的代码审查)
  - [对于贡献者许可协议](#对于贡献者许可协议)
  - [GitHub 在企业级上的管理](#github-在企业级上的管理)
  - [项目质量](#项目质量)
- [沟通与协作工具](#沟通与协作工具)
- [企业级 GitHub 管理工具](#企业级-github-管理工具)
- [结束语](#结束语)
- [致谢](#致谢)

## 为什么您需要特殊的工具来管理开源项目

一旦您的开源项目办公室开始运作，就该收集合适的软件工具，让您的开发团队能够管理、跟踪、指导和推进他们的开源项目、消费、贡献和发布。

这些工具至关重要，因为将开源用于业务战略需要其自己的方法论和流程，这与使用和发布专有软件时所需的方法截然不同。开源工具使公司能够完成各种任务：

* 提供协作和代码构建的工作场所。
* 管理项目健康状态。
* 自动化关键和可重复的任务，如代码审查、跟踪和许可证合规性。
* 生成数据以证明您的项目办公室和开源战略的投资回报率。
* 监督项目质量，并确保在出现问题时设置防护措施。
  
在开启您的开源之旅时拥有正确、针对性的工具也会让开发人员和其他员工的工作更轻松，为结果提供更好的洞察力，并成为公司开源项目成功合作和沟通的基础。

> “如果您有超过100个代码仓库或100名需要管理的人员，您真的不能再让人用电子表格手动管理了。虽然，人们仍然会这样做。但这开始变得临时和繁琐。这就是工具发挥作用的地方。它们让您能够扩展规模。” – [Jeff McAffer](https://twitter.com/jeffmcaffer)，微软开源项目办公室主任

## 如何选择和规划您的工具

公司对需要哪些开源工具的早期讨论大多取决于其业务、产品和服务以及它如何为客户和员工提供服务。随着其开源项目办公室制定规划过程和战略地图，工具可以被选择以整合公司的目标、流程和基础设施。

最终，了解您需要哪些工具的唯一方法是了解您想要通过开源做什么。

以下是为管理您的开源项目办公室选择所需工具的基本步骤：

1. 向开发人员和社区成员获取认可和选择偏好。为了实现这一目标，您需要与开发人员和社区成员进行详细讨论。他们可以描述哪些工具已经或可能最适合他们使用。认真对待这些建议和请求。倾听那些将带您达到目标的人的意见。他们很可能已经在使用许多这些工具了，所以要从他们的经验中受益。
2. 了解业务关键应用程序所需的软件依赖关系和集成。这意味着了解和知道您的业务依赖哪些开源软件，以便您能够及时了解安全问题并确保软件的连续性。
3. 研究现有工具，并决定您可以直接使用或根据需要进行构建的工具。不要为每个工具从头开始。看看您所在的开源社区中正在使用的工具，以及有关这些工具的建议和反馈。逗留于在线开发社区中，看看哪些工具有效，并寻求建议和意见。在开源会议上提问，在“兴趣小组”会议上与其他开发者交流，向已经在做您想做的事情的人学习。

一旦选择了工具，就必须进行实施，这还需要几个额外的步骤：

1. 创建内部基础设施以支持、管理和使用这些工具。通过您新成立的开源项目办公室，指定某人负责维护和构建内部基础设施，该基础设施将通过在线内部门户网站分发工具，并将其组织成任务和功能。在这个工具门户中，您可以将工具提供给所有开发人员，或通过根据他们的工作和要求的认证和权限来限制它们对特定用户的使用。
2. 为将使用这些工具的员工提供培训计划。仅仅获取工具是不够的。现在，你必须确保你的开发人员知道如何使用这些工具，并且正在掌握它们的功能。在这个阶段，无论是在线培训、课堂教学还是小型午间小组设置的培训项目，都将对充分利用这些工具带来重要影响。询问你的开发人员哪种学习方法最适合他们，并让他们选择他们想要的学习方式。
3. 确保这些工具在您的组织中得到中心化的展示。让开发人员能够轻松找到并使用它们，最好是集成到跟踪开发进度的任何现有开发者仪表板中。同样，内部工具门户将帮助您的公司组织和分发运营关键工具。
  
在选择工具时，考虑到实施也是有帮助的，因为这也可能影响您的决策。例如，一个学习曲线陡峭的工具可能需要更多的培训。

### 利用现有工具

一旦您对团队需要满足组织开源目标的工具有了清晰的想法，以及自身依赖和基础设施的可能限制，第一步就是探索并了解已经构建好并可供您使用的现有工具。由于大多数工具本身都是开源的，如果它们起初不符合您的确切需求，您的开发团队可以联系工具的构建者，看看他们是否可以合作并贡献，通过添加功能将工具引入新方向。

具有讽刺意味的是，许多开源项目办公室并不总是重用其他人开发的工具，或与其他公司合作共同开发管理其开源项目所需的工具。他们通常想这样做，但许多企业，包括Facebook和微软，在真正成为讨论话题之前就已经拥有现有的工具套件。因为他们已经有了自己的工具集，并已经做出了这些投资，所以似乎对采用其他公司的工具的欲望较小。

这就是刚开始构建自己开源项目的公司具有显著优势的地方。由于他们现在正在建立自己的开源项目办公室并深入开源，他们不必受到这些限制的困扰。

相反，他们可以明智地利用他人的经验和成功，并使用近年来由领先的公司创建的经过验证的工具来构建他们的开源工具箱。Linux基金会的开源行业组织，[TODO Group](http://todogroup.org/)（开放谈论，开放开发），在本文档中收集了这些工具的列表。

### 创建仪表板

除了合适的工具之外，公司还应该结合中央仪表板，允许他们实时监控和跟踪其开源项目和开发。许多公司可能已经有了这样的仪表板用于现有的开发工作和应用程序，并且可能将现有的仪表板与他们的开源工作集成起来。如果没有，他们应该创建或采用新的仪表板来改进他们的开源部署管理。

>“关于仪表板，有许多创建它们的方式，从公司想要如何显示与开发相关的信息的角度来看，这真的是一种艺术。有些人构建这些带有旋转仪表板的花哨屏幕，但关键是要有一个中心位置，最好与您现有的开发仪表板共同位置，人们可以前去了解更多关于开源项目健康状况、指标等信息。” – [Chris Aniszczyk](https://twitter.com/cra)，云原生计算基金会COO。

## 基本工具集的要素

用于管理和报告开源项目的工具的丰富可用性可能会很快变得令人不知所措。如果您的开源项目刚刚起步，将研究重点放在您需要启动和运行的几个基本工具上将会有所帮助。

然后，随着您的项目的发展和对这些工具的使用经验增加，您可以开始采用新的工具来帮助您根据需要自动化和简化流程。请记住，您希望选择的工具能够补充和支持您的内部文化和流程，而不是引导它们。

以下各节介绍了几乎所有开源项目日常使用的基本工具类别。这是组织您的研究的好方法。

### 自动化流程

自动化流程的工具是您公司开源项目中最重要的选择和使用的工具之一。这些工具的任务范围广泛，包括自动化贡献者许可协议（CLA）的流程，CLA是一种法律文件，声明开发人员创建了代码并未非法从其他地方复制。传统上，这些协议是通过打印协议，然后签署并传真来手动完成的。但在电子邮件和即时通讯的世界中，这种做法现在已经过时了。相反，该过程可以通过请求电子签名并随后跟踪和处理提交的机器人来自动化。

其他自动化工具可以告诉您确切是谁在为您的项目做出贡献，并有助于消除程序摩擦，从而减慢随着项目规模变大而需要满足公司需求的进展速度。

根据微软开源项目办公室的说法，该办公室管理着GitHub上的约8000个代码仓库，涉及约11000个贡献者，公司在2016年收到了约40000个内部请求，要求在项目中使用开源。为了管理这些请求以及创建的代码和正在更新的代码版本，公司转而使用可以自动化管理这些混乱现状的工具。由于代码可能在可能涉及数百个其他项目中使用，因此必须仔细跟踪，以便如果出现安全漏洞，可以迅速绘制出所有软件影响的范围并进行修复。在如此大规模的情况下，自动化是至关重要的，手动更新几乎是不可能的。

![微软的Azure开源门户显示了一些有用的信息，比如GitHub上每日用户的数量。来源：https://www.jeff.wilcox.name/2015/11/azure-on-github/](/img/guides/tools-for-managing-open-source-programs1.png)

### 管理关键任务

另一种需要考虑和获取的重要工具是那些帮助管理关键任务的工具，例如项目管理、跟踪项目健康状况，并确保开发人员、开源社区和公司内部之间清晰快速的沟通。

### 源代码管理

大多数通过开源项目办公室开发的企业软件项目都使用 [GitHub](https://GitHub.com/about) 作为它们的集中式托管和开发平台。

GitHub是一个在线源代码管理站点，允许开源开发人员将其代码管理和存储在一个中心的“仓库”或存储空间中，参与者可以在其中进行协作和共同构建代码。今天，有大约6400万个开源编码项目托管在GitHub上，涉及约2300万名开发人员。

GitHub用户可以添加代码，审查提交的代码，提出更改建议，获取和提供反馈，并使用该服务进行项目管理。GitHub使用 [Git版本控制系统](https://git-scm.com/)，这是由Linux创始人Linus Torvalds开发的开源项目，为正在协作的代码和人员提供组织。每个“贡献者”都有自己的项目仓库副本，他们可以在自己的计算机上进行更改，然后将其提交回项目以供将来包含。然后，项目组织者会审查、讨论、修改并批准或拒绝该“拉取请求”（此处有示例）(https://GitHub.com/GitHub/opensource.guide/pull/402/files)，或代码贡献。

### 许可合规性

代码扫描和合规性工具同样重要，它们有助于跟踪代码来源和许可要求。对于公司来说，监控引入其自身基础设施、产品和服务的开源代码以确保符合许可要求至关重要。

例如，您的应用程序可能包含数千个开源组件。为了保护公司免受法律问题的困扰，了解这些细节至关重要。在高风险的情况下，用户必须深入代码以深入验证和确认许可证是否符合他们所说的内容，这取决于您的业务在风险光谱上的位置（请参阅我们关于使用和分发开源代码的指南）。

>“您必须了解您的风险概况，因为最终扫描的一切都是关于风险管理。您可以把头埋在沙子里，然后只是相信并希望自己没事。或者您可以说‘如果我被起诉，那将毁了我的生意。’您需要真正确定（风险所在）。所以，您打开软件包，然后查看所有代码行，并找到可能存在风险的所有内容。” – Jeff McAffer，微软开源项目办公室主任。

## 管理源代码的工具

正如我们之前讨论过的，GitHub是当今大多数开源项目办公室的首选源代码管理系统。但仅仅依靠GitHub可能无法满足您的所有项目的代码管理需求——特别是在您扩大努力的规模时。

一些用于开源世界的工具旨在通过添加它所缺少的功能来改进GitHub，例如支持检查开发者证书的工具，以确保代码可以在开源项目中合法许可和使用。

在代码审查方面，GitHub也存在一些不足，因此有一些可用的工具可以自动将问题代码发送回创建者，并要求他们进行审查和进行必要的更改。GitHub没有强制某人审查其代码的方法，因此这些巧妙的工具将使工作流程更加顺畅。

其他针对GitHub的特定工具扩展了GitHub的性能指标功能，这些功能往往非常特定于项目，而不是提供整个组织的详细信息。对于维护多个开源代码仓库并跨多个GitHub项目进行的公司，需要更好的工具来组织和汇总它们以理解其中的意义。来自Amazon、Netflix和微软的各种工具可帮助处理这些任务。

以下是一些最流行和最有用的源代码管理工具，它们可以简化和帮助您的GitHub存在：

**源代码扫描和许可证合规性**

[Black Duck 软件组成分析](https://www.synopsys.com/software-integrity/security-testing/software-composition-analysis.html) – Synopsys 的 Black Duck 软件组成分析 (SCA) 帮助团队管理在应用程序和容器中使用开源和第三方代码所带来的安全、质量和许可证合规风险。

[版权审查工具](https://wiki.debian.org/CopyrightReviewTools) – 这一套开源命令行工具帮助简化初始版权文件的结构以及后续的审查和更新。

[FlexNet Code Insight](https://www.revenera.com/protect/products/flexnet-code-insight.html) – Revenera 提供的 FlexNet Code Insight 帮助开发人员、法律团队和安全人员自动化公司开源使用。

[FOSSA](http://fossa.io/) – 这是一款商业工具，可在后台自动执行代码依赖跟踪和许可证合规扫描。

[FOSSID](https://fossid.com) - FOSSID 是一款用于许可证和漏洞扫描的商业工具。FOSSID 不依赖声明的组件和许可证，而是使用大型项目和代码片段数据库来扫描代码片段。这可以检测复制/粘贴的代码，或者那些未正确保留许可证声明的代码。特别是在审核从第三方收到的代码或准备开源最初仅供内部使用的代码时，这非常有用。

[FOSSology](https://www.fossology.org/) – 一个 Linux 基金会项目，FOSSology 是一个开源许可证合规软件工具包，可以从命令行运行许可证、版权和出口控制扫描。还提供了数据库和网页界面来创建合规工作流。

![Linux 基金会的 FOSSology 合规工具](/img/guides/tools-for-managing-open-source-programs3.png)

[REUSE](https://reuse.software/) – 一个免费的软件工具，帮助在代码库中采用和检查许可证的应用。它基于最佳实践，包括 SPDX 规范。它提供一个徽章 API 服务来标记合规性。

[scancode-toolkit](https://github.com/nexB/scancode-toolkit) – 来自 nexB 的开源 ScanCode 工具套件，扫描代码中的许可证、版权和依赖项，以发现、探索和清点代码中使用的开源和第三方组件。

[SPDX](https://spdx.dev/) – 软件包数据交换 (SPDX) 规范是一种用于描述软件包的组件、许可证和版权的标准格式。SPDX 标准通过标准化开发者和公司之间共享许可证信息的方式来帮助遵守自由和开源软件许可证。SPDX 规范由 Linux 基金会主办的 SPDX 工作组开发。该小组提供开源[工具](https://spdx.dev/tools)来帮助使用 SPDX 文档的用户。

[Vigiles](https://timesys.com/solutions/vigiles-vulnerability-management/) – Vigiles 是一个商业软件组成分析 (SCA) 和 CVE 监控工具，优化用于嵌入式 Linux，并适用于所有开源软件。它提供了跟踪、分类、修复和记录影响设备的 CVE 的完整过程。

[WhiteSource](https://www.whitesourcesoftware.com/) – 提供许可、安全、代码质量和报告分析，通过自动和持续扫描数十个开源代码库来实时管理开源组件。

### 错误和问题跟踪

[Bugzilla](https://www.bugzilla.org/) – 开源、服务器端软件，具有高级查询工具，可以记住搜索结果，集成的电子邮件功能和全面的权限系统。Mozilla 将 Bugzilla 用作其错误跟踪系统。

[GitHub Issues](https://help.github.com/articles/about-issues/) – GitHub 自带的反馈和错误跟踪工具，GitHub Issues 是 GitHub 项目托管的一部分。

[GitLab](https://about.gitlab.com/) – 这个错误跟踪工具在单一用户界面中统一了问题跟踪、代码审查、Git 仓库管理、活动流、Wiki 等功能，以帮助您的开源项目。GitLab 可作为服务或商业软件使用。

[JIRA](https://www.atlassian.com/software/jira) – 来自 Atlassian 的 JIRA 包含自定义过滤器、开发者工具集成、可自定义的工作流和丰富的 API，以将 JIRA 与其他应用程序集成。JIRA 可作为商业软件使用。

### 归档和发布管理

[Artifactory](https://www.jfrog.com/artifactory/) – Artifactory 是 JFrog 的一个仓库管理器，支持用任何编程语言创建的软件包。它与所有主要的 DevOps 和持续集成、持续部署工具集成。Artifactory 可作为商业或开源工具使用。

[Docker Hub](https://hub.docker.com/) – 一个基于云的注册服务，允许用户链接到代码仓库并构建和测试他们的镜像。Docker Hub 是一个集中资源，用于容器镜像的发现、分发和变更管理，以及开发管道中的协作和工作流自动化。

[github-release](https://github.com/github-release/github-release) – GitHub 的开源内置功能，让用户[打包和编辑项目的发布](https://help.github.com/articles/about-releases/)，使其他社区成员可以使用这些项目。

## 项目健康跟踪工具

随着开源项目的成长和成熟，监控和跟踪其整体健康状况是企业开源项目的核心任务。为了实现这一目标，您必须收集工具，报告个别开源项目在其社区中的表现和接受程度 - 通常涵盖数十、数百甚至数千个项目。这些工具还必须能够将数据整合成有意义、有用且可操作的信息，以便全面了解整个开源项目组合的综合表现。

![Amazon 的开源项目仪表板可用于一次查看和监视多个 GitHub 组织和/或用户。来源: https://github.com/amzn/oss-dashboard](/img/guides/tools-for-managing-open-source-programs4.png)

归根结底，重点在于你能从数据中获得的关键和有用的信息——而不是关于虚荣指标，比如详细说明一个项目记录了多少“关注者”星标，自项目启动以来有多少贡献者参与，或其他缺乏重要背景信息的指标。

最好的项目健康工具还必须帮助项目团队对支持他们努力的社区做出响应，并鼓励贡献开发人员的参与和多样性。这意味着工具帮助维护者快速回应社区成员发布的问题或反馈，以便他们保持热情参与，不会感到无聊而转移到其他项目。

一些开源社区可能会有大量的贡献者，而其他社区可能只有一小部分特定群体的社区成员。项目健康工具需要能够处理各种规模的项目。

> “关于现有的工具和系统，我的希望是，我们很快就会达到这样一个观点：公司的开源项目办公室不应该再需要自己创建任何工具或技术。他们应该能够找到并使用现有的开源工具，用于管理他们的开源项目。” - [Jeff McAffer](https://twitter.com/jeffmcaffer)，微软开源项目办公室主任

以下是一些最受欢迎和最有用的项目统计和项目健康跟踪工具：

* [Gittagstats](https://github.com/mcharleb/gittagstats) – Gittagstats 是一个开源工具，用于从 Git 仓库的一组标签生成统计报告。该工具由高通公司创建。

* [GrimoireLab](https://chaoss.github.io/grimoirelab/) – GrimoireLab 有各种开源工具，用于测量和可视化开源项目的统计数据，从 Git仓库、GitHub 拉取请求或 Bugzilla 票据到邮件列表、Meetup 群组或 Slack 频道。GrimoireLab 是 [CHAOSS](https://chaoss.community) 的一个项目，这是一个关于开源开发指标的协作组。

* [OSS Tracker](https://github.com/Netflix/osstracker) – 来自 Netflix 的 OSS Tracker 收集有关 GitHub 组织的数据，并将其汇总到该组织的所有项目中，以单一用户界面展示。所有仓库都列出来，指标被组合为一个组织，但社区管理员也可以将项目组织成功能区域，并指定管理员来分配管理和工程师的领导。 

> “目标是拥有工具，以及透明的数据和与指标相关的信息，可以用来指导组织。” - [Chris Aniszczyk](https://twitter.com/cra)，云原生计算基金会首席运营官

TODO Group 还提供了一个[有用的列表，添加了其他工具](https://GitHub.com/todogroup/awesome-oss-mgmt)。

### 为了更好的代码审查：

* [PullApprove](https://about.pullapprove.com/) – 通过改进同行审查、强制样式指南、捕获错误并对代码进行安全检查，使代码贡献（或拉取请求）更加正式化，从而提高代码质量。
* [sentinel](https://github.com/habitat-sh/sentinel) – 一个仓库管理机器人，用于审查和测试代码贡献，构建仓库的维护者列表，并与用户沟通拉取请求的状态。

### 对于贡献者许可协议

[CLA Assistant](https://github.com/cla-assistant/cla-assistant) – 由 SAP 贡献，CLA Assistant 通过处理用户的法律贡献方面，简化了工作流程。该助手在用户进行代码贡献时要求代码贡献者签署 CLA，并使用其 GitHub 帐户对每个贡献者进行身份验证。如果对 CLA 进行更改，它还会自动更新拉取请求的状态，并在每个新的拉取请求中要求用户重新签署 CLA。

![SAP 的 CLA Assistant 工具](/img/guides/tools-for-managing-open-source-programs5.png)

[CLA Portal](https://github.com/vmware/claportal) – 来自VMware，CLA Portal为向你的GitHub仓库提交拉取请求的贡献者增加了一个工作流程，以便他们能数字化签署CLA。当开发者打开一个拉取请求时，如果需要，他们会收到签署协议的提示。此外，还包括了CLA起草、CLA与项目的映射及协议审核的管理员界面。

[DCOB](https://github.com/chef/dcob) – 该机器人有助于强制执行针对拉取请求中每个代码变更的开发者原创证书签名。DCOB根据[开发者原创证书](http://developercertificate.org/)的要求，为每个被接受的代码变更设置状态。

[EasyCLA](https://github.com/communitybridge/easycla) - 由 Linux Foundation 提供，用于简化 CLA 流程。它专注于 Linux Foundation 项目，但会根据情况考虑 Linux Foundation 之外的项目。除了典型的 CLA 工具之外，它还支持对企业贡献者进行白名单设置。它与 GitHub 拉取请求集成。

### GitHub 在企业级上的管理

* [hubcommander](https://github.com/Netflix/hubcommander) - 一个用于GitHub组织管理的Slack机器人，HubCommander采用了对话驱动开发，以帮助管理GitHub项目。它创建了一种简单的方法来执行特权GitHub组织管理任务，无需向你的GitHub组织成员授予管理员或所有者权限。
* [opensource-portal](https://github.com/Microsoft/opensource-portal) – 来自微软的此工具旨在帮助大型组织进行大规模的GitHub管理操作、入职等事宜。这是微软开源程序办公室提供的一套工具之一。
* [settings](https://github.com/bkeepers/github-configurer) – 此应用将.github/settings.yml中定义的仓库设置同步到GitHub，为仓库启用拉取请求。
* [zappr](https://github.com/zalando/zappr) - zappr是一个为增强项目工作流程而构建的GitHub集成。来自Zalando，zappr通过消除围绕拉取请求审批的瓶颈，并帮助项目所有者在合并到项目主分支前阻止“失控”的拉取请求，从而帮助开发者提高生产力并提升开源项目的质量。

### 项目质量

* [CII 最佳实践徽章](https://bestpractices.coreinfrastructure.org/) – 来自 Linux 基金会的核心基础设施倡议 (CII) 最佳实践徽章是自由/开源软件 (FLOSS) 项目展示他们遵循最佳实践的一种方式。项目可以通过使用此 Web 应用程序自愿免费进行自我认证，解释他们如何遵循每个最佳实践。
* [CodeClimate](https://codeclimate.com/) – Code Climate 让组织能够通过在开发工作流程中完全可配置的测试覆盖率和可维护性数据来控制他们的代码质量。对于开源项目，它是免费的！

## 沟通与协作工具

当然，开源开发不仅仅关乎代码。它还需要在企业内外工作在项目上的多样化群体之间进行健康的沟通和合作，以及公司开源项目办公室的员工。

为此，开发人员可以利用他们可能已经在其他项目中使用的工具，包括 [互联网中继聊天（IRC）](http://www.irc.org/links.html)，开发人员可以在其中发布查询并获取与开发相关主题有关的[快速响应](http://blog.andrewray.me/irc-the-secret-weapon-of-developers/)。另一个例子是 [TWiki](http://twiki.org/)，它是一个开源企业 Wiki 和 Web 协作平台，开发人员可以在其中讨论代码、项目和相关主题。

通过社交媒体平台、网页门户、开源项目仓库以及其他可以发现并促进输入、问题和讨论的地方，也能促进沟通。

还有 [Slack](https://slack.com/)，它是一个在线团队项目管理和沟通平台，用户可以访问和共享消息和文件、组织工作流程、进行信息搜索等。Slack 可以配置为接收支持请求、代码提交、错误日志等任务的通知。

在宣传公司的参与和支持开源时，不要忘记公司的公共关系和营销人员。社交媒体账号包括 Twitter、Reddit、Facebook、LinkedIn 等网站都很重要，还有内部和外部博客和网站的使用。客户关系管理 (CRM) 软件以及电子邮件群发和新闻通讯，可以帮助公司让客户和客户了解他们的开源进展。

## 企业级 GitHub 管理工具

当涉及到公司为其企业开源项目提供和使用的工具时，最重要的无疑是那些帮助公司管理其企业级 GitHub 运营的工具。GitHub 是许多操作的理想平台，但对于谷歌、微软、Facebook、Twitter、LinkedIn 等大型复杂公司来说，使用标准的 GitHub 服务有许多限制。

大型企业需要更多的功能，包括身份管理、设置和权限管理、安全性和双因素认证的执行，以及更深入地理解和跟踪代码仓库的方法。

这就是为什么需要构建专门的自动化工具来处理诸如入职、离职、执行安全政策以及为开发人员提供仓库访问请求等任务。

微软根据其自身的独特需求构建了自己的工具来处理许多此类任务，以简化和改进其开源计划。迄今为止，微软在 GitHub 上有着[健康的存在](https://github.com/Microsoft)，拥有超过 4000 个仓库，涉及超过 4500 名开发人员。

> “随着规模的扩大，管理你的 GitHub 业务变得重要。你会得到一个 GitHub 组织，这是一系列仓库，然后你会有成员和团队。管理所有这些东西变得有点复杂，尤其是当它开始扩展到数百个仓库、数百人和多个 GitHub 组织时。” – [Jeff McAffer](https://twitter.com/jeffmcaffer)，微软开源项目办公室主任

微软创建的工具之一是一个定制的自助 [GitHub 管理和入职门户](http://www.jeff.wilcox.name/2015/11/azure-on-github/)，用于组织其项目、仓库和团队。在最简单的层面上，这个基于网络的门户允许开发人员将他们的微软公司 ID 映射到他们的 GitHub ID，从而增强系统安全性，并有助于简化大量重要项目中涉及的开发人员的组织工作。

该门户还允许员工通过 GitHub 和微软进行身份验证，从而创建他们身份的“虚拟链接”，使他们能够在工作中获得所需权限，具体取决于他们的工作角色。如果员工离开公司，该系统可以进行调整，以根据需要删除或重新分类他们的访问权限。

该门户运行在一个或多个云服务器上，并依靠缓存来帮助会话管理并减轻 GitHub API 的压力。作为其不断增长的开源努力的一部分，微软门户每天平均有大约 1000 名独特用户使用这个工具，这些努力现在包括了超过 10000 名使用、贡献和发布开源代码的工程师。

## 结束语

嘿，把你的公司引入开源世界并不简单。但是包括微软和谷歌在内的许多其他公司已经在你之前做到了这一点，并提供了详细的路线图、代码、建议等，以使你的旅程更加轻松。

创建一个开源项目办公室并选择一套关键工具来启动你的工作，这是你力所能及的事情。而且它们很可能已经激发了你开发人员的极大期待，其中许多人可能已经在自行（或在工作中秘密地）为开源项目做出贡献。

通过在开源项目上进行协作并邀请其他人与你合作，你的公司可以获得无可估量的利益，并通过充满活力和创新推动其进步。

拥有合适的工具对推动公司开放创新至关重要。

## 致谢

贡献者所属组织以文章于2019年最初发布时为准：

* [Chris Aniszczyk](https://twitter.com/cra)，CNCF 的首席运营官。
* [Jeff McAffer](https://twitter.com/jeffmcaffer)，微软开源项目办公室主任。
