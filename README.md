[![Build Status](https://travis-ci.org/alibaba/druid.svg?branch=master)](https://travis-ci.org/alibaba/druid)
[![Coverage Status](https://img.shields.io/codecov/c/github/alibaba/druid/master.svg)](https://codecov.io/github/alibaba/druid?branch=master&view=all#sort=coverage&dir=asc)  
[![Maven Central](https://maven-badges.herokuapp.com/maven-central/com.alibaba/druid/badge.svg)](https://maven-badges.herokuapp.com/maven-central/com.alibaba/druid/)
[![GitHub release](https://img.shields.io/github/release/alibaba/druid.svg)](https://github.com/alibaba/druid/releases)
[![License](https://img.shields.io/badge/license-Apache%202-4EB1BA.svg)](https://www.apache.org/licenses/LICENSE-2.0.html)


Introduction
---
- The secondary development druid dataSource connection pool
- has been added to allow you to perform drop function,create function
- 二次开发的 druid 数据库连接池
- 允许执行 drop function,create function等操作


Documentation
```
        ......
        WallConfig wallConfig = new WallConfig();
        
        /*add the following line config*/
        /*添加下面这行配置*/
        wallConfig.setCreateFunctionAllow(true);
        wallConfig.setSetAllow(true);
        
        
        
        WallFilter wallFilter = new WallFilter();
        wallFilter.setConfig(wallConfig);
        List<Filter> filters = new ArrayList<>();
        filters.add(wallFilter);
        datasource.setProxyFilters(filters);
        ......
```
---
# [druid github link](https://github.com/alibaba/druid.git)

