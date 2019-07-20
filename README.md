Introduction
---
- The secondary development druid dataSource connection pool
- has been added to allow you to perform drop function,create function
Documentation
```
        ......
        WallConfig wallConfig = new WallConfig();
        
        /*add the following line config*/
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
# [druid](https://github.com/alibaba/druid.git)

