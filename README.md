hi
这是一个低成本的私人云项目
是对互联网大厂的云服务的一种低成本的模仿，主要也是依赖于开源项目
期望可以达到的功能，开箱即用，可以支持个人进行的各种开发工作，包括且不限于：代码管理、提交任务、部署服务等。

1. 主机核心节点要求，8G内存以上，毕竟希望安装一个spark玩一玩。
二手成本低于600。如果对主机大小没要求，可以低于500。【20220802价格】——但是可能只是win系统，刷linux需要额外的钱。具体配置可以参考【todo】这篇文章，总之不是一个很难的任务。
【树莓派】树莓派的价格涨了太多，而性能并不是很划算。20220810的价格，700-900元的现货，完全可以组装i5-32G的平台。我的手中是有树莓派的，打算只是做一些网络下载机使用。

2. 预期的主机要素：
    1. 存储系统：HDFS，对象存储，k-v，独立部署的文档系统，图数据库，消息队列
    2. 计算系统：GPU节点，存储节点，计算节点，下载节点。
    3. 日志系统，资源（主机，容器，代码，镜像）管理，任务管理，网络管理，报警系统。
    4. 开箱即用。（现在还不太明白，可能还是基于网络安装的）

3. 期望支持的任务：下载，云服务，大数据，代码管理，任务管理，人工智能。

4. 一些设计
    整体是一个简单的总分结构，一个核心节点，管理各种从属节点。稳定性和高可用等功能开发完了再说。
    鉴权等权限管理的问题先淡化。目标是面向个人开发者的低成本、开箱即用的方案。

5. 工作计划：
    1. 安装主机。已基本就绪。
    2. 先弄一个管理页面，然后支持主机注册和发现
    3. 部署代码管理，能提交代码
    4. 部署docker，可以镜像管理。整体上稀疏权限问题，之后再优化
    5. 基于docker的任务提交管理系统
    6. 部署HDFS，能提交spark任务
    7. 部署各种数据库，mysql， redis，kafka，对象存储
    8. 开发安装部署。（安装各种包，分两种，一个是主机，一个是从机。主机管理各种，从机client汇报）
    9. 边做边写日志，边传代码。细化各种系统，例如日志、报警等

