容器实践指南
============================================================

![An executive's guide to containers](https://opensource.com/sites/default/files/styles/image-full-size/public/images/business/containers_2015-1-osdc-lead.png?itok=E1imOYe4 "An executive's guide to containers") 图片来源：[Maersk Line][1]. [CC SA-BY 4.0][2]

与互联网领域的领导们关于"容器"的讨论通常被总结如下：

_作为一名CxO，我面临杠杆时间术的持续的压力。IT预算不断减少，我只有有限的资源。然而，交付的工作量却比以往更多。我花费太多的时间致力于解决预算的约束。另外，互联网的格局正在经历一个快速的改变，而且新的技术一直在被引进。我从我最信任的顾问那听来的最新的话题是一个"容器策略"的实现。我想理解:_

1. _什么是容器？_
2. _过渡到容器的企业价值是什么？_
3. _为什么我现在应该转移到容器？如果我不采纳会有一些坏处吗？_
4. _容器是否已经足够成熟用于企业消费？_
5. _我如何让我的企业因使用容器而快速地发展？_

让我们从最开头开始。

### 容器

在过去的10年左右，企业已经从物理基础设施转向了虚拟机(VMs)。转向VMs的关键优势是可以减少数据中心足迹。通过在同一个物理盒子上运行多个虚拟机，你可以在更少数量的物理机器上安装更多的应用程序。使用容器是另一种更轻量地打包应用程序的方式，而且其交付模式更快。它们是一种在单独的盒子里运行多个应用程序进程的奇特方式，无论那个盒子是一个虚拟机还是一个物理机。另外，容器在DevOps的上下文切换、微服务和云战略方面也有重要作用。

### 容器vs虚拟机

容器和虚拟机在一些方面并不相同。一台虚拟机尽管不是物理机，但是它表现地就像是一台物理机。虚拟机是一个包含所有东西的独立的环境，从一个完整的(来宾)操作系统开始。在另一方面，容器是共享相同物理机或虚拟机上资源的进程。容器显然更加有趣，因为：

*  相比较而言，虚拟机要重一些，而容器更轻。因为容器只包括了它们所运行的程序所需要的库。
*  虚拟机需要花费几分钟来启动，而容器在几秒钟内就可以启动。
*  通常，更多的容器比虚拟机更加适合你的基础设施。
 ![Containers versus VMs](https://opensource.com/sites/default/files/containersvmvscontainers.png "Containers versus VMs")


技术已经发展到足以保持这些容器安全、彼此独立，而且正确的设计选择可以保证那些坏掉的容器不会影响运行在同一个盒子里的其他容器的性能。实际上，操作系统是被构建来优化和运行容器本身。

然而，当你转向容器时，你需要做出正确的选择。你需要做足够的尽职的调查，所以，你选择合适的技术合作伙伴和能够制作容器的制造商。开源技术起着很关键的作用。开源的[Docker项目][5]使得分层格式的容器很容易构建和使用。[开放容器计划][6](OCI)已经成为被所有主要技术供应商所支持的开源容器标准。如Red Hat这样的开源技术提供商准备好了为容器而准备的安全的操作系统。例如， Red Hat Enterprise Linux 7.x (包括Red Hat Enterprise Linux原子主机)被进行优化以在本机上运行容器，同时也提供监控和管理容器的工具。其他的开源项目如来自Tectonic的CoreOS也正在进入市场。的确，容器正等着被企业所采用。

### 容器平台

容器平台让容器成为企业消耗品。在过去的十年中，你可能在你的企业里处理过虚拟机散乱的问题，容器散乱比那要糟糕好几倍。在你的数据中心不同主机上运行不同规模的容器，保证你的应用程序的高可用性，尽管容器故障、自动化健康检查和基于流入的工作载荷的自动化容器缩放等等，这些是你能期待容器平台应该有的一些关键特性。

当在一个被定位为容器即服务模型(CaaS)的平台上运行容器时，这些平台的一些其他特性如自动化生成和部署使这个平台成为平台即服务模型(PaaS)。虽然CaaS能让你规模化运行容器，但是，PaaS可以让你利用你的源代码编译、创建容器，为你运行那些容器。另外，这些平台提供了完整操作管理特性，例如，集群的管理和监控、容器的安全缺陷检测、运行安全的容器、跟踪日志和度量等等。

尽管一引起技术供应商正在使用他们的专有技术来构建容器平台，但总的来说，一些公司正在围绕建立在[Kubernetes][7](K8S)的基础上的开源技术来规范他们自己。K8S是一项由Google发起的开源项目，现在很多大平台的供应商也支持它。KBS也是[云端原生计算基金会][8](CNCF)的一部分,CNCF正在发展成以云为中心技术的标准体。当你在容器平台上做出选择时，围绕开源流程编排技术的标准化是非常重要的。它基本上允许你移植到不同的容器平台，如果你不喜欢你第一次做的选择。K8S还允许你的容器工作载荷移植到不同的公有云。这些就是为什么我们会看到越来域越多的技术公司正在使用Kubernetes的原因。

一些企业正在试图通过拼接几个包括K8S在内开源项目来打造他们自己的DIY容器平台。这确实是比继续跟随专有技术要更好的一种解决方案，但是要完成这项工作也仍然包含很多需要探讨的地方。然而，一个企业的维护和保持这样的DIY平台的能力应该被认真考虑。许多企业并不是做着创建IT平台的工作，然而他们希望运行自己的主流业务。有很多可行的基于K8S的解决方案，比如[红帽OpenShift平台容器][9]、[Apprenda][10]、[Deis][11]和[Rancher][12]，它们提供一个平台的为企业准备的版本。这些解决方案中的每种都有不同完整程度的功能。

这些解决方案是由供应商认证和支持。有些方案是完全的开源PaaS解决方案，而另外一些可能是CaaS。根据你的企业的需求，这些解决方案可以作为比DIY容器平台更好的替代品。

### 企业的担忧和它们与容器的关系

今天，几乎每个企业都正在与数字变换打交道，这些数字变换影响包括DevOps战略、微服务和云等多个领域。容器在这些领域中的每一个中都起着相当重要的作用。

### DevOps策略

IT组织被分成运维和应用开发，他们作为两个独立的团队运作，每一队都只有他们自己的一套目标。大多数企业为了将这两个团队联合起来正在朝DevOps的方向前进。

容器在DevOps倡议的成功中发挥着重要的作用。在DevOps中成功的关键标准之一是增加开发人员在运营中的股份。开发人员不仅应该把代码交给运维人员，而且他们还应该考虑他们的代码是如何在生产环境中运行的。普遍的技术是采用"架构即代码"，而不是提供几页容易出错的安装说明指示，开发团队应该提供像编程时的环境配置。


这恰恰就是容器可以解决的问题。可以作为容器的模版的容器镜像包括整个堆栈，从基本操作系统到应用程序代码。利用容器，开发人员将不再只是从Dev到QA再到Prod这样生成应用程序;相反，他们将传递一个版本化的容器镜像，这个镜像包括生成的运行程序和它运行需要的环境。容器是包罗万象的，从操作系统库到中间件再到应用程序的所有东西都被整合进一个镜像里面。因此，容器在开发环境运行的方式和它在质量保证环境和生产环境下运行的方式完全一样。容器是DevOps成功的重要因素。

 ![Container-based model](https://opensource.com/sites/default/files/containerbasedmodel.png "Container-based model") 

 另外，容器平台正在进一步发展。典型的持续集成和交付（CICD）工具，如Jenkins，
可以作为容器，这个容器能在容器平台本身而不需要额外的基础设施运行整个CICD过程。现在你可以使用PaaS平台来生成和运行你的CICD管道。

### 微服务策略

微服务是今天IT领域的另一个热门话题。应用程序是这样被设计的：把应用程序分解为离散化的小的服务，每个服务完成一个小任务。这些服务中的每一个都可以根据合适的技术用不同的编程语言进行编写。它们可以由小团队(双比萨团队)创建和管理，并且可以迅速地改变它们。所有这些要求再次需要用到容器。容器足够小到成为微服务的基础。容器能够支持任何你选择的技术和语言，容器容易创建和运行，并且可以快速地改变。微服务和容器现在已经不分彼此，如果有人说不使用容器来实现微服务，他们将会受到别人奇怪的表情。

实际情况是，虽然微服务有望让情况变得简单，但是他们的扩张也增加了复杂性。几个微服务的设计和开发模式即将能缓解它们的实现。这意味着开发人员现在急需这样一个开发平台，在这个平台下，开发人员可以轻松地部署和组织微服务，而且还能：

* 以一种语言不可知的方式实现这些微服务设计模式。
* 不会因代码入侵而增加代码的复杂性，因此，开发人员必须将许多模式的代码包括进他们的业务逻辑。
* 足够灵活以便部署在你所选择的基础设施上，并且不会把你捆绑在特定的云上。

这就是选择一个正确的容器平台所起作用的地方。在具体的基础设施上按照某一特定供应商的方法来实现这些微服务将会把你的应用程序捆绑在那些供应商的平台上。使用类似兼容OCI的容器的容器化微服务将可以保证你的微服务能够被运行在任何兼容OCI的平台上。

选择正确的容器平台来运行你的微服务是需要做的另一个重要的决定。今天，有很少的选择和许多的FUD。如果你作出选择时不足够慎重，其中一些选择会把你带到非标准的、特定供应商的路线上。

### 云策略

云战略是IT领域的又一个热门话题。无论你是否喜欢，服务模型都是不可避免的变化。如果你不将这作为IT服务进行提供，你的开发团队将可能会找到创建"shadow IT"的方法来访问云。另外，尽管使用云技术将会让你从资本支出转移到运营支出，但是，管理云支出是一个不断的挑战。

云可以提供虚拟机，在你添加额外的虚拟机之前，你想确认这个云上的CPU、内存和网络等资源都处于最佳使用状态。容器在这个地方扮演着很重要的角色。因为容器双虚拟机要小得多。并且，如果你的应用程序正运行在容器中，你可以在虚拟机中安装更多的容器，这比在每台虚拟机中运行一个应用程序组件要多很多。

公有云供应商有很多，其中Amazon Web Services (AWS)、Microsoft Azure和Google Cloud最受欢迎。另外，你可能想在你的基于OpenStack的数据中心里拥有你自己的私有云。这些云环境中的每一个都有他们自己的协议、API和工具。当你想让你的应用程序在云上运行时，你不想让您的应用程序业务流程按照云供应商的说明，也不想维护任何特定云的代码。与特定的云供应商锁定你的技术就像在未来几年内向供应商签署空白支票。

云的可移植性对您的云战略至关重要。你可以编写应用程序，而不用担心它们在哪里运行，容器平台可以将你和特定的云供应商协议隔离开来，从而避免你与一个云供应商锁定。

### 传统系统

微服务架构带给开发的优势很多，但并不是每个应用程序都可以重构它们自己，有些只能重构一部分。传统的应用程序被普遍接受，因为它们需要维护和管理。虽然容器可以实现微服务，但容器不仅仅只是微服务。可以想象，你可以将大型应用程序和微服务作为容器来运行，因此只要你选择正确的容器技术和正确的应用程序平台，就可以将许多(如果不是所有)的传统的应用程序作为容器运行。

### 总结

我希望对各种策略和容器的深入了解有助于你的公司对下一步进行评估。让我在评论里面了解您公司学习到的经验，或者说他们没能大步向前跨越，他们还需要我再提供一些什么信息。

------------------------------------------------------------------------------

作者简介：

Veer Muchandi -- 开源爱好者，容器和PaaS倡导者，喜欢学习和分享。

-------------------------------------------------------------------------------

via: https://opensource.com/article/17/1/container-strategy-for-executives

作者：[Veer Muchandi][a]
译者：[zhousiyu325](https://github.com/zhousiyu)
校对：[校对者ID](https://github.com/校对者ID)

本文由 [LCTT](https://github.com/LCTT/TranslateProject) 原创编译，[Linux中国](https://linux.cn/) 荣誉推出




[a]:https://opensource.com/users/veermuchandi
[1]:https://www.flickr.com/photos/maerskline/6955071566
[2]:https://creativecommons.org/licenses/by-sa/4.0/
[3]:https://opensource.com/article/17/1/container-strategy-for-executives?rate=DuiecCOvGMj-GXcdlJsN8xdZJ82yPUX1M3M9ZNkT99A
[4]:https://opensource.com/resources/what-are-linux-containers
[5]:https://opensource.com/resources/what-docker
[6]:https://opensource.com/business/16/8/inside-look-future-linux-containers
[7]:https://opensource.com/resources/what-is-kubernetes
[8]:https://www.cncf.io/
[9]:https://www.openshift.com/container-platform/
[10]:https://apprenda.com/
[11]:http://deis.io/
[12]:http://rancher.com/
[13]:https://jenkins.io/
[14]:https://opensource.com/resources/what-are-microservices
[15]:https://opensource.com/user/92826/feed
[16]:https://opensource.com/article/17/1/container-strategy-for-executives#comments
[17]:https://opensource.com/users/veermuchandi