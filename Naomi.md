---
timezone: Pacific/Auckland
---

> 请在上边的 timezone 添加你的当地时区，这会有助于你的打卡状态的自动化更新，如果没有添加，默认为北京时间 UTC+8 时区
> 时区请参考以下列表，请移除 # 以后的内容

timezone: Pacific/Honolulu # 夏威夷-阿留申标准时间 (UTC-10)

timezone: America/Anchorage # 阿拉斯加标准时间 (UTC-9)

timezone: America/Los_Angeles # 太平洋标准时间 (UTC-8)

timezone: America/Denver # 山地标准时间 (UTC-7)

timezone: America/Chicago # 中部标准时间 (UTC-6)

timezone: America/New_York # 东部标准时间 (UTC-5)

timezone: America/Halifax # 大西洋标准时间 (UTC-4)

timezone: America/St_Johns # 纽芬兰标准时间 (UTC-3:30)

timezone: America/Sao_Paulo # 巴西利亚时间 (UTC-3)

timezone: Atlantic/Azores # 亚速尔群岛时间 (UTC-1)

timezone: Europe/London # 格林威治标准时间 (UTC+0)

timezone: Europe/Berlin # 中欧标准时间 (UTC+1)

timezone: Europe/Helsinki # 东欧标准时间 (UTC+2)

timezone: Europe/Moscow # 莫斯科标准时间 (UTC+3)

timezone: Asia/Dubai # 海湾标准时间 (UTC+4)

timezone: Asia/Kolkata # 印度标准时间 (UTC+5:30)

timezone: Asia/Dhaka # 孟加拉国标准时间 (UTC+6)

timezone: Asia/Bangkok # 中南半岛时间 (UTC+7)

timezone: Asia/Shanghai # 中国标准时间 (UTC+8)

timezone: Asia/Tokyo # 日本标准时间 (UTC+9)

timezone: Australia/Sydney # 澳大利亚东部标准时间 (UTC+10)

timezone: Pacific/Auckland # 新西兰标准时间 (UTC+12)

---

# {Naomi}

1. 自我介绍
2. 你认为你会完成本次残酷学习吗？必须的

## Notes

<!-- Content_START -->

### 2024.09.19
# Chapter3运输层

运输层位于应用层和网络层之间，是分层的网络体系结构的重要部分。主要关注TCP和UDP运输层协议

# 3.1 运输层服务

发送端的应用程序-》发送端运输层-〉发送端网络层-》接受端网络层-》接受端运输层

- **发送端应用程序 → 发送端运输层**：
    - 发送端的应用程序将数据发送给运输层。运输层会将应用程序的数据分割成较小的块（报文段，segment），并为每个报文段加上运输层首部。运输层的首部包含端口号、序列号、校验和等信息，以便在接收端进行数据的重组和校验。
- **发送端运输层 → 发送端网络层**：
    - 运输层将封装好的报文段交给网络层。网络层会将报文段封装进网络层的数据报（数据包），并加上网络层首部，通常包括源 IP 地址、目的 IP 地址等信息。
- **发送端网络层 → 接收端网络层**：
    - 网络层将封装好的数据报通过路由器传递到网络中的下一个节点，经过多个路由器转发，最终到达目的地网络层。路由器只处理数据报的网络层信息（例如 IP 地址），而不关心封装在数据报中的运输层报文段。

运输层的类比：2个家庭间的通信，Ann和Bill负责各自家庭内部的收发邮件

Ann和Bill都是在各自家里进行工作的;例如，他们并没有参与任何一个中间邮件中心对邮件进行分拣，或者将邮件从一个邮件中心送到另一个邮件中心之类的工作。类似地，运输层协议只工作在端系统中。在端系统中，运输层协议将来自应用进程的报文移动到网络边缘(即网络层)但对有关这些报文在网络核心如何移动并不作任何规定。事实上，如图3-1所示，中间路由器既不处理也不识别运输层加在应用层报文的任何信息

UDP(用户数据报协议)，它为调用它的应用程序提供了一种不可靠、无连接的服务。另一种是TCP(传输控制协议)，它为调用它的应用程序提供了一种可靠的、面向连接的服务

每台主机有一个IP地址。因特网网络层协议有一个名字叫IP，即网际协议。IP为主机之间提供了逻辑通信。

UDP 和 TCP 的主要职责之一就是在 IP 提供的**主机到主机**传递服务的基础上，进一步扩展为**进程到进程**的传递服务。主机间的信息传递因为有UDP和TCP的存在，扩展成了端系统上的两个进程之间的信息传递



<!-- Content_END -->
