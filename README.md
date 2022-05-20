## MIR开发指南

MIR开发指南2018 是MIN项目组开发的MIR开源项目面向科研开发者的开发指南，本文基于2022年的截止当前最新的版本进行翻译，如有错误可 pull request，大家共同维护。

<!-- vscode-markdown-toc -->
* 1. [介绍](#1介绍)
  * 1.1 [mird模块](#11mird模块)
* 2. [MIN网络分组介绍](../mir-zh/chapter2.md/#2min网络分组介绍)
  * 2.1 [MIN网络基本理念](../mir-zh/chapter2.md/#21-min网络基本理念)
  * 2.2 [MIN网络分组格式](../mir-zh/chapter2.md/#22-min网络分组格式)
* 3. [LogicFace模块](../mir-zh/chapter3.md)
  * 3.1 [底层接口设计](../mir-zh/chapter3.md/#31-底层接口设计)
  * 3.2 [LinkService模块](../mir-zh/chapter3.md/#32-link-service)
  * 3.3 [LogicFace](../mir-zh/chapter3.md/#33-logicface)
* 4. [包验证模块](../mir-zh/chapter4.md/#4-packet-validator包验证模块)
  * 4.1 [预处理流程](../mir-zh/chapter4.md/#41-pmir预处理流程)
  * 4.2 [Parallel Packet Validator](../mir-zh/chapter4.md/#42-parallel-packet-validator)
  * 4.3 [Ordered Parallel Packet Validator](../mir-zh/chapter4.md/#43-ordered-parallel-packet-validator)
* 5. [Table模块](../mir-zh/chapter5.md/#5table模块)
  * 5.1 [FIB(转发信息表)](../mir-zh/chapter5.md/#51-转发信息表fib)
  * 5.2 [CS(内容存储表)](../mir-zh/chapter5.md/#52-内容存储表cs)
  * 5.3 [PIT(未决兴趣表)](../mir-zh/chapter5.md/#53-未决兴趣表pit)
  * 5.4 [ST(策略表)](../mir-zh/chapter5.md/#54-策略表st)
* 6. [转发模块(Forwarder)](../mir-zh/chapter6.md/#6forwarder模块)
  * 6.1 [转发管道](../mir-zh/chapter6.md/#61-转发管道)
  * 6.2 [兴趣包处理路径](../mir-zh/chapter6.md/#62-兴趣包处理路径)
  * 6.3 [数据包处理路径](../mir-zh/chapter6.md/#63-数据包处理路径)
  * 6.4 [Nack包处理路径](../mir-zh/chapter6.md/#64-nack包处理路径)
  * 6.5 [通用推式包处理路径](../mir-zh/chapter6.md/#65-通用推式包处理路径)
  * 6.6 [转发过程优化浅谈](../mir-zh/chapter6.md/#66-转发流程优化浅谈)
* 7. [策略模块](../mir-zh/chapter7.md/#7-mir-strategy)
  * 7.1 [策略类基准](../mir-zh/chapter7.md/#71-策略类基准)
  * 7.2 [最佳路由转发策略](../mir-zh/chapter7.md/#72-最佳路由转发策略)
  * 7.3 [轮询转发策略](../mir-zh/chapter7.md/#73-轮询转发策略)
* 8. [Management协议](../mir-zh/chapter8.md/#8-management-协议)
  * 8.1 [基本机制](../mir-zh/chapter8.md/#81-基本机制)
  * 8.2 [管理包的基本格式](../mir-zh/chapter8.md/#82-管理包的基本格式)
  * 8.3 [基本模块](../mir-zh/chapter8.md/#83-基本模块)
  * 8.4 [一个管理兴趣包的前世今生](../mir-zh/chapter8.md/#84-一个管理兴趣包的前世今生)
* 9. [Plugin模块](../mir-zh/chapter9.md/#9-plugin-模块)
  * 9.1 [插件锚点](../mir-zh/chapter9.md/#91-锚点anchor-point)
  * 9.2 [插件调用顺序](../mir-zh/chapter9.md/#92-调用顺序)
  * 9.3 [如何使用插件系统扩展功能](../mir-zh/chapter9.md/#93-如何使用插件系统扩展功能)
  * 9.4 [使用插件系统开发的例子详探](../mir-zh/chapter9.md/#94-使用插件系统开发的例子详探)


<!-- vscode-markdown-toc-config
    numbering=true
    autoSave=true
    /vscode-markdown-toc-config -->
<!-- /vscode-markdown-toc -->
