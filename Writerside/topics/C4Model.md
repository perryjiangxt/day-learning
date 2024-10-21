# C4Model

创建C4模型是为了帮助软件开发团队描述和交流软件架构，无论是在前期设计会议期间还是在回顾性地记录现有代码库时。这是一种在不同详细级别创建“代码地图”的方法，就像您使用谷歌地图之类的东西放大和缩小您感兴趣的区域一样。

## C4Model分级

## System Context Diagram
系统上下文图是绘制和记录软件系统的一个很好的起点，允许您退后一步，看到大局。绘制一个图表，将您的系统显示为中心的一个盒子，周围是它的用户和与之交互的其他系统。细节在这里并不重要，因为这是您的缩小视图，显示了系统环境的大局。重点应该放在人员（参与者、角色、角色等）和软件系统上，而不是技术、协议和其他低级细节上。这是您可以向非技术人员展示的那种图表。

- 范围
  - 参与者、多个系统（如果有）

![image_7.png](image_7.png)

Diagram key

![image_8.png](image_8.png)

- 主要元素 
  - 相关的软件系统
- 其他支持的元素 
- users、actors、roles、participants 
- 直接连接到范围内软件系统的人员（例如用户、参与者、角色或角色）和软件系统（外部依赖项）。通常，这些其他软件系统位于您自己的软件系统的范围或边界之外，您对它们没有责任或所有权。

## Container diagram
一旦你理解了你的系统是如何适应整个 IT 环境的，一个真正有用的下一步是用容器图放大到系统边界。“容器” 是类似于服务器端 Web 应用程序、单页应用程序、桌面应用程序、移动应用程序、数据库模式、文件系统等。本质上，容器是一个单独可运行 / 可部署的单元（例如一个单独的进程空间），用于执行代码或存储数据。容器图显示了软件架构的高级形状以及责任是如何在其中分配的。它还显示了主要的技术选择以及容器如何相互通信。这是一个简单的、以技术为重点的高级图表，对软件开发人员和支持 / 运营人员都很有用。

示例图片

![image_9.png](image_9.png)

Diagram key

![image_10.png](image_10.png)

- 范围
  - 参与者、单个系统、已存在的系统、webApp、mobileApp
  - People and software systems directly connected to the containers.
- 其它
  - 此图未提及集群、负载均衡器、复制、故障转移等，因为它可能会因不同的环境（例如生产、暂存、开发等）而异。通过一个或多个部署图可以更好地捕获此信息。


## Component diagram
接下来，您可以进一步放大和分解每个容器，以识别主要的结构构建块及其交互。组件图显示了容器是如何由许多 “组件” 组成的，每个组件是什么，它们的职责以及技术 / 实现细节。

- 示例

![image_11.png](image_11.png)

- Diagram key

![image_12.png](image_12.png)

- 范围
  - 单独Container
- 主要元素
  - 此Container内部的Components
  - 参与者
  - 直接关联到的Components

## Code Diagram
最后，您可以放大每个组件以显示它是如何作为代码实现的；使用 UML 类图、实体关系图或类似的。这是一个可选的详细级别，通常可以从 IDE 等工具中按需获得。理想情况下，此图将使用工具（例如 IDE 或 UML 建模工具）自动生成，您应该考虑只显示那些允许您讲述您想要讲述的故事的属性和方法。除了最重要或最复杂的组件之外，不建议使用此详细级别。

- 示例图
![image_13.png](image_13.png)

## 其它

### 系统景观图 System landscape diagram
系统上下文、容器、组件和代码图旨在提供单个软件系统的静态视图，但在现实世界中，软件系统永远不会孤立存在。因此，特别是如果您负责软件系统的集合/组合，了解所有这些软件系统如何在给定的企业、组织、部门等中组合在一起通常很有用。本质上，这是所选范围内软件系统的映射，每个感兴趣的软件系统都有一组系统上下文、容器、组件和代码图。从实际的角度来看，系统景观图实际上只是一个系统上下文图，没有对特定软件系统的特定关注。

- 示例图
![image_14.png](image_14.png)
- Diagram key
![image_15.png](image_15.png)

### 部署图 Deployment Diagram
部署图允许您说明静态模型中的软件系统和/或容器实例如何部署到给定部署环境（例如生产、暂存、开发等）中的基础设施上。它基于UML部署图。部署节点表示软件系统/容器实例的运行位置；可能是物理基础设施（例如物理服务器或设备）、虚拟化基础设施（例如IaaS、PaaS、虚拟机）、容器化基础设施（例如Docker容器）、执行环境（例如数据库服务器、JavaEE Web/应用程序服务器、Microsoft IIS）等。部署节点可以nested.You可能还需要包括基础设施节点，如DNS服务、负载均衡器、防火墙等。请随意使用亚马逊网络服务、Azure等提供的图标来补充您的部署图…只要确保您使用的任何图标都包含在图表键/图例中。

- 示例图
![image_16.png](image_16.png)
- Diagram key
![image_17.png](image_17.png)
- 示例图2
![image_18.png](image_18.png)
- Diagram key
![image_19.png](image_19.png)
- 范围
  - One or more software systems within a single deployment environment (e.g. production, staging, development, etc).
  - 部署节点、软件系统实例和容器实例。





<seealso>
    <category ref="external">
        <a href="https://www.apiseven.com/blog">API博客</a>   
        <a href="https://c4model.com/introduction">C4Model官网</a>
    </category>
</seealso>