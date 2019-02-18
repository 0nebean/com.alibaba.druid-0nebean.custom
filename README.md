# druid

二次开发的druid连接池 增加了允许执行 drop function,create function 等功能,需做如下三行配置
```
        ......
        WallConfig wallConfig = new WallConfig();
        
        
        wallConfig.setCreateFunctionAllow(true);
        wallConfig.setMultiStatementAllow(true);
        wallConfig.setSetAllow(true);
        
        
        
        WallFilter wallFilter = new WallFilter();
        wallFilter.setConfig(wallConfig);
        List<Filter> filters = new ArrayList<>();
        filters.add(wallFilter);
        datasource.setProxyFilters(filters);
        ......
```

[![Build Status](https://travis-ci.org/alibaba/druid.svg?branch=master)](https://travis-ci.org/alibaba/druid)
[![Coverage Status](https://img.shields.io/codecov/c/github/alibaba/druid/master.svg)](https://codecov.io/github/alibaba/druid?branch=master&view=all#sort=coverage&dir=asc)  
[![Maven Central](https://maven-badges.herokuapp.com/maven-central/com.alibaba/druid/badge.svg)](https://maven-badges.herokuapp.com/maven-central/com.alibaba/druid/)
[![GitHub release](https://img.shields.io/github/release/alibaba/druid.svg)](https://github.com/alibaba/druid/releases)
[![License](https://img.shields.io/badge/license-Apache%202-4EB1BA.svg)](https://www.apache.org/licenses/LICENSE-2.0.html)

Introduction
---

- git clone https://github.com/alibaba/druid.git
- cd druid && mvn install
- have fun.

Documentation
---

- 中文 https://github.com/alibaba/druid/wiki/%E5%B8%B8%E8%A7%81%E9%97%AE%E9%A2%98
- English https://github.com/alibaba/druid/wiki/FAQ
- Druid Spring Boot Starter https://github.com/alibaba/druid/tree/master/druid-spring-boot-starter
