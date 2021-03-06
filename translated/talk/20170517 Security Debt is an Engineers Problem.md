安全债务是工程师的问题
============================================================

![](https://cdn.thenewstack.io/media/2017/05/d6fe35b0-11416417-1257170530979237-7594665410266720452-o_2_orig-1024x641.jpg)

![](https://cdn.thenewstack.io/media/2017/05/ea8298a9-keziah-slide1-300x165.png)
>Keziah Plattner of AirBnBSecurity.

参加者上月在旧金山 Twitter 总部举办的 [WomenWhoCode Connect][5] 活动中了解到，就像组织会建立技术债务一样，如果他们不相应地计划，也会建立一个名为“安全债务”的东西，。

安全性已经成为软件开发过程中每步的重要组成部分，甲骨文首席安全官，[Mary Ann Davidson][6]强调，在 [WomenWhoCode][8] 就 [Zassmin Montes de Oca][7] 开发人员的安全性进行了主旨演讲。

在过去，除银行外，安全性几乎被所有人忽视。但安全性比以往任何时候都更重要，因为现在有这么多接入点。我们已经进入[物联网][9]的时代，窃贼可以劫持你的冰箱而看到你不在家。

戴维森负责 Oracle 的保障，“我们确保为建立的一切构建安全性，无论是内部部署产品、云服务，甚至是设备，我们有支持小组建立在客户的网站并报告数据给我们，帮助我们做诊断 - 每件事情都必须对其进行安全保护。

![](https://cdn.thenewstack.io/media/2017/05/8d5dc451-keziah-talking-225x300.jpg)

Plattner 与 #WWCConnect 人群交谈

AirBnB 的 [Keziah Plattner][10] 在分组会议中回应了这个情绪。她说：“大多数开发商并不认为安全是他们的工作，但这必须改变。”

她分享了工程师的四项基本安全原则。首先，安全债务是昂贵的。现在有很多谈论[技术债务][11]，她认为这些谈话应该也包括安全债务。

Plattner 说：“这个历史态度是‘我们会稍后考虑安全’”。当公司抓住软件效率和增长的唾手可得的成果时，他们忽视了安全性，但最初的不安全设计可能在未来几年会引起问题。

她说，很难为现有的脆弱系统增加安全性。即使你知道安全漏洞在哪里，并且已经预算了时间和资源进行更改，重新设计一个安全系统是耗时和困难的。

她说，所以这是关键，从一开始就建立安全性。将安全性视为技术债务的一部分以避免这个问题。并涵盖所有可能性。

根据 Plattner 说的，最重要的是难以让人们改变行为。没有人会自愿改变，她说，即使你指出新的行为更安全。我们都点点头。

Davidson 说，工程师们需要开始考虑他们的代码如何被攻击，并从这个角度进行设计。她说她只有两个规则。第一个从不信任任何未验证的数据，规则二见规则一。

她笑着说：“人们一直这样做。他们说：‘我的客户端给我发送数据，所以没有问题’， 不。。。”。

Plattner说，安全的第二个关键是“永远不信任用户”。

Davidson 说道：“我的工作是做专业的偏执狂。”她一直担心有人甚至无意中会破坏她的系统。这不是学术性的，最近有通过 IoT 设备的拒绝服务攻击。

### Little Bobby Tables

Plattner 说：“如果你安全计划的一部分是信任用户做正确的事情，那么无论你有什么其他安全措施，你系统本质上是不安全的。”

她解释说，重要的是要清理所有的用户输入，如[ XKCD 漫画][12]中的那样，因为她的儿子的中间名是 “DropTable Students”，妈妈擦掉整个学校的数据库。

所以清理所有的用户输入。检查。

她展示了一个 JavaScript 开发者在开源中使用 eval 的例子。她警告说：“一个好的基本规则是‘从不使用 eval()’”。 [eval()] [13]函数会计算 JavaScript 代码。“如果你这样做，你正在向随机用户开放你的系统。”

Davidson 警告说，她甚至将文档中的示例代码也包括在内。她笑着说：“因为我们都知道没有人复制示例代码”。她强调指出，任何代码都应进行安全检查。

![](https://cdn.thenewstack.io/media/2017/05/87efe589-keziah-path-300x122.png)

让它容易

Plattner 的建议三：要使安全容易。她建议采取阻力最小的道路。

对外，使用户选择选择安全而不是退出，或者更好使其成为强制性的。她说，改变人们的行为是科技中最难的问题。一旦用户习惯以非安全的方式使用你的产品，将来会变得非常困难。

在公司内部，她建议制定标准化安全性的工具，因此这不是个别开发人员需要考虑的内容。例如，将数据加密为服务，这样工程师可以仅调用服务来加密或解密数据。

她说，确保公司注重安全环境。在公司内切换到好的安全习惯。

作为最薄弱的环节，只有你是安全，所以重要的是每个人都有良好的个人安全习惯，并具有良好的企业安全环境。

在 Oracle，他们已经覆盖了。Davidson 表示，她厌倦了向没有安全培训的大学毕业的工程师解释安全性，所以她在 Oracle 写了第一个编码标准。现在有数百个页面以及很多贡献者，还有一些是强制性的课程。它们具有符合安全要求的度量标准。这些课程不仅适用于工程师，也适用于文档作者。她说：“这是一种文化。”

没有提及密码的关于安全性的讨论将会是安全的？Plattner 说：“每个人都应该使用一个好的密码管理器，但在工作中应该是强制性的，还有双重身份验证。”

她说，基本的密码原则应该是每个工程师清醒生活的一部分。密码中最重要的是它们的长度和熵 - 使按键的集合尽可能地随机。强健的密码熵检查器对此非常有用。她建议使用 Dropbox 开源熵检查器 [zxcvbn][14]。

Plattner说，另一个诀窍是在验证用户输入时使用一些故意减慢速度的如 [bcrypt][15]。慢速并不困扰大多数合法用户，但会惹恼试图强行进行密码尝试的黑客。

Davidson 说：“所有这些都为那些想要进入技术安全领域的人提供了工作安全保障，我们正在增加更多的代码，这就产生了系统性风险。只要我们继续在技术领域做有趣的事情, 我不认为任何人会没有一分安全工作。”

--------------------------------------------------------------------------------

via: https://thenewstack.io/security-engineers-problem/

作者：[TC Currie][a]
译者：[geekpi](https://github.com/geekpi)
校对：[校对者ID](https://github.com/校对者ID)

本文由 [LCTT](https://github.com/LCTT/TranslateProject) 原创编译，[Linux中国](https://linux.cn/) 荣誉推出

[a]:https://thenewstack.io/author/tc/
[1]:http://twitter.com/share?url=https://thenewstack.io/security-engineers-problem/&text=Security+Debt+is+an+Engineer%E2%80%99s+Problem+
[2]:http://www.facebook.com/sharer.php?u=https://thenewstack.io/security-engineers-problem/
[3]:http://www.linkedin.com/shareArticle?mini=true&url=https://thenewstack.io/security-engineers-problem/
[4]:https://thenewstack.io/security-engineers-problem/#disqus_thread
[5]:http://connect2017.womenwhocode.com/
[6]:https://www.linkedin.com/in/mary-ann-davidson-235ba/
[7]:https://www.linkedin.com/in/zassmin/
[8]:https://www.womenwhocode.com/
[9]:https://www.thenewstack.io/tag/Internet-of-Things
[10]:https://twitter.com/ittskeziah
[11]:https://martinfowler.com/bliki/TechnicalDebt.html
[12]:https://xkcd.com/327/
[13]:https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/eval
[14]:https://blogs.dropbox.com/tech/2012/04/zxcvbn-realistic-password-strength-estimation/
[15]:https://en.wikipedia.org/wiki/Bcrypt
[16]:https://thenewstack.io/author/tc/
