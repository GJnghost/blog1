---
layout:     post
title:      『Class Note』计算机网络
subtitle:   计算机网络の课堂笔记（Updating…
date:       2020-04-09
author:     GJ
header-img: img/Others_four.jpg
catalog: true
tags:
    - Computer Network
    - Class Note
---

## 第一章 概述

### 1.1 计算机网络在信息时代的<u>作用</u>

 - 21世纪的一些重要的特征就是**数字化**、**网络化**和**信息化**，它是一个以**网络为核心**的信息时代。

 - 网络现已成为信息社会的命脉和发展知识经济的重要基础。

 - 网络是指“**三网**”，即**电信网络**、**有线网络**和**计算机网络**。

 - 发展最快的并起到**核心作用**的是**计算机网络**。

 - **因特网[^1]的发展**

   - 进入20世纪90年代以后，以因特网为代表的计算机网络得到了飞速的发展。
   - 已从最初的**教育科研网络**逐步发展成为**商业网络**。
   - 已成为仅次于全球电话网的**世界第二大网络**。
   - 现在人们的生活、工作、学习和交往都已离不开因特网。

- **计算机网络向用户提供的<u>最重要</u>的功能**

  - **连通性**——计算机网络使上网用户之间都可以交换信息，好像这些用户的计算机都可以彼此直接连通一样。

  - **共享性**——即**资源共享**。可以是信息共享、软件共享，也可以是硬件共享。

    

### 1.2 因特网的概述

#### 1.2.1 网络的网络

- 起源于美国的因特网，现已发展成为世界上最大的国际性计算机互联网。
- **网络**[^2]：由若干**结点**[^3]和连接这些结点的**链路**[^4]组成。
- **互联网**：是”**网络的网络**“[^5]
- 连接在因特网上的计算机都称为**主机**[^6]
- **Pay attention to**: 网络与因特网
  - **网络**把许多计算机连接在一起。
  - **因特网**则把许多网络连接在一起。
  - 因此，**互联网>因特网>网络>计算机**（或**结点**）

#### 1.2.2 因特网发展的三个阶段

- **第一阶段**

  - **第一阶段**是从单个网络**ARPANET**向互联网发展的过程。

  - 1983年**TCP/IP协议**成为ARPANET上的标准协议。

  - 人们把**1983**年作为**因特网的诞生时间**。
  - **<u>internet</u>和<u>Internet</u>的区别**
    - 以**小写字母i**开始的internet（互联网或互连网）是一个通用名词，它泛指由多个计算机网络互连而成的网络。
    - 以**大写字母I**开始的Internet（因特网）则是一个专有名词，它指定当前全球最大的、开放的、由众多网络相互连接而成的特定计算机网络，它采用**TCP/IP协议**作为通信的规则，且其**前身**是美国的ARPANET。

- **第二阶段（三级结构的因特网）**

  - **第二阶段**的特点：是建成了**三级结构**的因特网。
  - 三级计算机网络，分为**主干网**、**地区网**和**校园网**（或**企业网**）。

- **第三阶段（多层次ISP结构的因特网）**

  - **第三阶段**的特点：是逐渐形成了**多层次ISP结构**的因特网。

  - 出现了**因特网服务提供者ISP**[^7]

  - 用户通过ISP上网

    ```mermaid
    graph LR
    A(用户)-->|有线| D{ISP<sub>1</sub>}
    B(用户)-->|有线| D{ISP<sub>1</sub>}
    C(用户)-->|无线| E{ISP<sub>2</sub>}
    D --> F[因特网]
    E --> F
    ```

    根据提供服务的覆盖面积大小以及所拥有的IP地址数目的不同，ISP也分为不同的层次

  - 具有三层ISP结构的因特网的概念示意图

    ```mermaid
    graph TD
    A[主干ISP]---B
    A---c[--//就是把左右那俩ISP连起来//没有上面的线]
    A---C
    B[主干ISP]---D[地区ISP]
    B[主干ISP]---E[...]
    B[主干ISP]---F[地区ISP]
    C[主干ISP]---G[地区ISP]
    C[主干ISP]---H[--IXP--//没有上面的线]
    C[主干ISP]---I[地区ISP]
    D---J[大公司]
    D---K[本地ISP]
    F---O[本地ISP]
    F---P[本地ISP]
    O---Q[校园网]
    O---R[校园网]
    G---S[本地ISP]
    G---T[本地ISP]
    I---U[本地ISP]
    I---V[本地ISP]
    S---W[公司]
    S---X[主机A]
    S---Y[...]
    T---Z[...]
    U---a[...]
    V---b[主机B]
    ```

  ​		主机A→本地ISP→地区ISP→主干ISP→地区ISP→本地ISP→主机B

  ​		因特网交换点 IXP：允许两个网络直接相连并交换分组

- **万维网WWW的问世**

  - 因特网已经成为世界上规模最大和增长速率最快的计算机网络，没有人能够准确说出因特网究竟有多大。

  - 因特网的**迅猛发展**始于**20世纪90年代**。由欧洲原子核研究组织CERN开发的万维网**WWW**[^8]被广泛使用在因特网上，大大方便了广大非网络专业人员对网络的使用，成为因特网的这种指数级增长的主要驱动力。

  - **因特网的发展情况概况**

    |      |     网络数     |     主机数     |     用户数     |   管理机构数   |
    | :--: | :------------: | :------------: | :------------: | :------------: |
    | 1980 | 10<sup>1</sup> | 10<sup>2</sup> | 10<sup>2</sup> | 10<sup>0</sup> |
    | 1990 | 10<sup>3</sup> | 10<sup>5</sup> | 10<sup>6</sup> | 10<sup>1</sup> |
    | 2000 | 10<sup>5</sup> | 10<sup>7</sup> | 10<sup>8</sup> | 10<sup>2</sup> |
    | 2005 | 10<sup>6</sup> | 10<sup>8</sup> | 10<sup>9</sup> | 10<sup>3</sup> |

#### 1.2.3 关于因特网的<u>标准化工作</u>

- **因特网协会**

  ```mermaid
  graph TD
  A[因特网协会 ISOC]-->B[因特网体系结构研究委员会 IAB]
  B-->C[因特网研究部 IRTF]
  B-->D[因特网工程部 IETF]
  C-->|具体工作的管理|E[因特网研究指导小组 IRSG]
  D-->|具体工作的管理|F[因特网工程指导小组 IESG]
  E-->G[研究组 RG]
  E-->H[...]
  E-->I[研究组 RG]
  F-->J[领域]
  F-->K[...]
  F-->L[领域]
  J-->M[工作组 WG]
  J-->N[...]
  J-->O[工作组 WG]
  L-->P[工作组 WG]
  L-->Q[...]
  L-->R[工作组 WG]
  ```

- **制订因特网正式标准的四个阶段**

  - **因特网草案**[^9]——在这个阶段还**不是**RFC文档。
  - **建议标准**[^10]——从这个阶段开始就成为RFC文档。
  - **草案标准**[^11]
  - **因特网标准**[^12]

- **各种RFC之间的关系**

  6种RFC。即，除因特网草案。

  ```mermaid
  graph TD
  A(因特网草案)-->B[实验的RFC]
  B-->G
  B-.->C
  A-->C[建议标准]
  C-.->G
  A-->D[提供信息的RFC]
  C-->E[草案标准]
  E-.->G
  E-->F[因特网标准]
  F-->G[历史的RFC]
  D-->G
  ```

  






[^1]: Internet
[^2]:network
[^3]:node
[^4]:link
[^5]:network of networks
[^6]:host
[^7]:Internet Service Provider
[^8]:World Wide Web
[^9]:Internet Draft
[^10]: Proposed Standard
[^11]: Draft Standard
[^12]: Internet Standard

