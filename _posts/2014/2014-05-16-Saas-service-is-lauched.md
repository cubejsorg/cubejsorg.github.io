---
layout: post
title: 我们SAAS服务正式上线了
categories: startup
tags: 
- tongdun
---

![tongdun](http://yikebocai.com/myimg/tongdun.png)

历时半年，我们的核心SAAS产品终于在今天迎来了第一个客户的正式上线，可喜可贺！

做一个好产品如同十月怀胎，历经千辛万苦，才修得正果，当然我们的阶段只能算是刚怀上，后面的路还有很长。还清楚地记住，我们第一版刚出来时去上海一家客户做演示时的窘态，原本觉得好好的功能接上投影仪之后投放出来的页面就错乱了，客户提出的功能我们的系统还不能很地满足，对他们的行业也不是非常了解，演示了一半人家就没兴趣了草草结束，原计划做的咨询合同也泡汤了。当时感觉真的很沮丧，刚开始就不顺，原来做客户是这么难。

好在大家没有受此影响，汲取教训不断完善产品，将不同行业的经验积累做成了模板，集成到了产品当中，使得客户一开始就能借助我们在风控行业的经验积累，来降低使用的门槛。记不清楚改了多少个版本了，从功能比较完善的1.0.0版本上线，已经发了两个比较大的版本变更，和至少8个小版本的变更，通过这种快速迭代的方式，不断改进产品功能，从现在看起来已像模像样，再拿今天的产品出去，我有信心可以满足大部分用户的需求。

除了产品上的改进，这段时间也建立了线上自动化发布流程，并建立了供客户测试的沙箱环境、供自己验证的预发布环境以及正式环境，为三个核心应用搭建了集群，对前端的Apache代理做了热备，部署了Zabbix监控体系，初步具备了高可用性。MySQL服务器还是个单点，下一步要做好最基本的主备，更远的规划是建立分布式数据库，从目前的发展趋势来看，很快数据库将成为业务发展的瓶颈。

提供SAAS服务，除了高可用性外，如何保证在大数据并发访问的情况下，能在最短的时间内给客户做出风险评估结果，减少对客户正常业务逻辑的影响，这就涉及到了性能的优化。我们提供的服务，还不像阿里的风控服务，都是为内部系统服务的，虽然每天有几十亿的事件量，但绝大部分都是异步处理，而我们的服务都是同步调用，这对系统的性能是个极大的挑战。

另外，为了能够快速升级产品，我们制定了小步快跑的研发策略，基本上在一到两周会发一个小版本上去，遇到线上bug，随时拉git分支进行修复，线上的集群部署方式和自动化发布脚本以及git优秀的分支开发支持，可以让我们快速迭代。

团队成员也有了很大进步，他们都是实习生或刚毕业不久的初级开发者，对互联网的整体技术框架可以说不怎么了解，也没有太多的经验积累，只能在快速试错中不断成长。在实践当中发现一个很有意思的事情，公测是个提升项目质量的绝佳方式，每次完成功能后一起对所有功能进行测试，都能发现大量的问题，并且问题在随后能得到快速修复，群众的眼睛真真是雪亮的。

客户接进来了只是迈出万里长征第一步，梦想和光荣就在前方，继续加油！