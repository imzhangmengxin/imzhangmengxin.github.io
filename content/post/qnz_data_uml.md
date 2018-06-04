---
title: "数仓模型"
date: 2017-03-04T21:57:45+08:00
lastmod: 2017-09-30T01:37:56+08:00
update: 
draft: false

tags: ["数仓","架构"]
categories: ["UML"]
hiddenFromHomePage: false

sequenceDiagrams: 
  enable: true
  options: "{theme: 'hand'}"
---

## 一元结构

```sequence
title: 一元架构
participant 生产库 as A
note left of A :数据实时,查询压力大
A->A :结果表计算完成ETL过程
```

## 二元结构

```sequence
title:二元架构
participant 线上库 as A
participant 离线库 as B
note right of B : 可以定期备份实时性要求低
A -> B :数据定期更新
B -- B :自更新宽表离线计算
note over B :ETL等过程交给存储过程,表等
B --> A :只执行查询任务
```

## 三元结构

```sequence
title: 三元架构
participant 线上主库 as A
participant 备份从库 as B
participant 离线统计库 as C
A - B :实时同步
B -- A :读写分离,灾难恢复
B - C : ETL选择用户关心业务表
C --C :宽表计算,统计输出
note over C :数据异常监控报警反馈
```