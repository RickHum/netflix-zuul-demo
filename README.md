### Spring cloud netfiix zuul（Demo）

根据netflix官网[zuul-simple-webapp](https://github.com/Netflix/zuul/tree/1.x/zuul-simple-webapp)改成maven工程。

### netflix zuul说明

zuul主要用于对外提供API的网关，用官网话说是边缘服务（edge service）。其实，zuul只提供了一套开发网关的轻量框架。不同的业务系统对网关的要求不同，所以，要根据实际需求定制zuul的filter。

zuul 介绍说明 [What is Zuul](https://github.com/Netflix/zuul/wikiedge service)

主要用途（以下场景，zuul不提供实现，需要用户根据实际业务自行实现）

* 身份认证与安全管控-主要用户鉴于外部用户是否有权限访问内部接口权限。
* 动态路由-可以结合ribbon 实现动态路由功能。[demo](https://github.com/Netflix/zuul/tree/1.x/zuul-netflix-webapp)
* 压力测试-可以根据压力检测系统性能
* 限流、限量-可以基于zuul实现访问的限流、限量以及计费功能。
* 静态返回处理-如果后端服务宕机后，可以通过zuul返回默认数据或页面。
* 监控与统计分析

zuul的使用参考 官网 [Getting Started](https://github.com/Netflix/zuul/wiki/Getting-Started)

zuul 原理分析[How it works](https://github.com/Netflix/zuul/wiki/How-it-Works)

### 如何运行该demo

编译代码后，可以直接在tomcat中运行。

注意： jvm中需要配置“zuul.filter.root”，指定filter所在文件目录。









    