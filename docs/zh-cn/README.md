# Waterdrop [![Build Status](https://travis-ci.org/InterestingLab/waterdrop.svg?branch=master)](https://travis-ci.org/InterestingLab/waterdrop)

[![Join the chat at https://gitter.im/interestinglab_waterdrop/Lobby](https://badges.gitter.im/interestinglab_waterdrop/Lobby.svg)](https://gitter.im/interestinglab_waterdrop/Lobby?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

Waterdrop 是一个`非常易用`，`高性能`，能够应对`海量数据`的`实时`数据处理产品，构建于Apache Spark之上。

---

### 如果您没时间看下面内容，请直接进入正题:  

请点击进入快速入门：https://interestinglab.github.io/waterdrop/#/zh-cn/quick-start

Waterdrop 提供可直接执行的软件包，没有必要自行编译源代码，下载地址：https://github.com/InterestingLab/waterdrop/releases

文档地址：https://interestinglab.github.io/waterdrop/

各种线上应用案例，请见: https://interestinglab.github.io/waterdrop/#/zh-cn/case_study/base

如果您遇到任何问题，请联系项目负责人 Gary(微信: `garyelephant`) , RickyHuo(微信: `chodomatte1994`)，我们为您提供全程免费服务。

---

## 为什么我们需要 Waterdrop

Databricks 开源的 Apache Spark 对于分布式数据处理来说是一个伟大的进步。我们在使用 Spark 时发现了很多可圈可点之处，同时我们也发现了我们的机会 —— 通过我们的努力让Spark的使用更简单，更高效，并将业界和我们使用Spark的优质经验固化到Waterdrop这个产品中，明显减少学习成本，加快分布式数据处理能力在生产环境落地。

除了大大简化分布式数据处理难度外，Waterdrop尽所能为您解决可能遇到的问题：
* 数据丢失与重复
* 任务堆积与延迟
* 吞吐量低
* 应用到生产环境周期长
* 缺少应用运行状态监控


"Waterdrop" 的中文是“水滴”，来自中国当代科幻小说作家刘慈欣的《三体》系列，它是三体人制造的宇宙探测器，会反射几乎全部的电磁波，表面绝对光滑，温度处于绝对零度，全部由被强互作用力紧密锁死的质子与中子构成，无坚不摧。在末日之战中，仅一个水滴就摧毁了人类太空武装力量近2千艘战舰。

## Waterdrop 使用场景

* 海量数据ETL
* 海量数据聚合
* 多源数据处理

## Waterdrop 的特性

* 简单易用，灵活配置，无需开发
* 实时流式处理
* 高性能
* 海量数据处理能力
* 模块化和插件化，易于扩展
* 支持利用SQL做数据处理和聚合
* 支持Spark 2.x

## Waterdrop 的工作流程

```
Input[数据源输入] -> Filter[数据处理] -> Output[结果输出]
```

![wd-workflow](../images/wd-workflow.png ':size=300%')


多个Filter构建了数据处理的Pipeline，满足各种各样的数据处理需求，如果您熟悉SQL，也可以直接通过SQL构建数据处理的Pipeline，简单高效。目前Waterdrop支持的[Filter列表](zh-cn/configuration/filter-plugin), 仍然在不断扩充中。您也可以开发自己的数据处理插件，整个系统是易于扩展的。

## Waterdrop 支持的插件

* Input plugin

Fake, File, Hdfs, Kafka, S3, Socket, 自行开发的Input plugin

* Filter plugin

Add, Checksum, Convert, Date, Drop, Grok, Json, Kv, Lowercase, Remove, Rename, Repartition, Replace, Sample, Split, Sql, Table, Truncate, Uppercase, Uuid, 自行开发的Filter plugin

* Output plugin

Elasticsearch, File, Hdfs, Jdbc, Kafka, Mysql, S3, Stdout, 自行开发的Output plugin

## 环境依赖

需要以下Spark集群环境的任意一种：
* Spark on Yarn
* Spark Standalone
* Spark on Mesos

如果您的数据量较小或者只是做功能验证，也可以仅使用local模式启动，无需集群环境。

## [配置/文档](zh-cn/configuration/base)

## [部署和测试](zh-cn/deployment)

## [开发者指引](zh-cn/developing-plugin)

## [Roadmap](zh-cn/roadmap)

## 社区分享

* 2018-09-08 Elasticsearch 社区分享 [Waterdrop：构建在Spark之上的简单高效数据处理系统](https://elasticsearch.cn/slides/127#page=1)

* 2017-09-22 InterestingLab 内部分享 [Waterdrop介绍PPT](http://slides.com/garyelephant/waterdrop/fullscreen?token=GKrQoxJi)

## 应用案例

* [微博](https://weibo.com), 增值业务部数据平台

![微博Logo](https://img.t.sinajs.cn/t5/style/images/staticlogo/groups3.png?version=f362a1c5be520a15 ':size=200%')

* [新浪](http://www.sina.com.cn/), 大数据运维分析平台

![新浪Logo](../images/sina-logo.png ':size=170%')

* [一下科技](https://www.yixia.com/), 一直播数据平台

![一下科技Logo](https://imgaliyuncdn.miaopai.com/static20131031/miaopai20140729/new_yixia/static/imgs/logo.png ':size=170%')

* 永辉超市子公司-永辉云创，会员电商数据分析平台

![永辉云创Logo](../images/yonghuiyunchuang-logo.png)

Waterdrop 为永辉云创旗下新零售品牌永辉生活提供电商用户行为数据实时流式与离线SQL计算。

* 水滴筹, 数据平台

![水滴筹logo](../images/shuidichou-logo.jpg ':size=130%')

水滴筹在Yarn上使用Waterdrop做实时流式以及定时的离线批处理，每天处理3～4T的数据量，最终将数据写入Clickhouse。

* 其他公司 ... 期待您的加入，请联系微信: garyelephant

## 贡献观点和代码

提交问题和建议：https://github.com/InterestingLab/waterdrop/issues

贡献代码：https://github.com/InterestingLab/waterdrop/pulls

## 开发者

感谢[所有开发者](https://github.com/InterestingLab/waterdrop/graphs/contributors)

## 联系项目负责人

Garyelephant : garygaowork@gmail.com, 微信: garyelephant

RickyHuo : huochen1994@163.com, 微信: chodomatte1994
