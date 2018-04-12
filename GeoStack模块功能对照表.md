# GeoStack模块功能对照表（2018-04-11）

## 概述

本对照表仅对上层业务模块进行罗列，隔离驱动层、API对接层暂不做罗列。

## 模块

### 核心组件

| 模块                                       | 功能概述                                     |
| ---------------------------------------- | ---------------------------------------- |
| geostack-framework                       | GeoStack基础框架组件，包含：GeoLogger相关基类、SpringMVC Controller抽象类、消息命令对象、GeoStack异常类、Hibernate方言类、数据库初始化接口类、邮件、分页、SSH操作、日期时间处理、字符串处理、数组处理、加密、Ajax工具、数据库工具类、代理工具类、WebSocket工具类等。 |
| geostack-dictionary                      | 字典管理组件，包含云平台表单字典管理、监控项字典管理、监控日志级别字典管理、系统数据初始化等模块。 |
| geostack-processfactory                  | 业务处理工厂类组件，封装业务处理工厂bean获取和管理模块。           |
| geostack-dependence                      | 基础依赖组件，封装计算方案、repo服务器管理、应用投递方案管理、应用投递站点管理、模板管理等模块。 |
| geostack-dispatch                        | 智能调度模块，封装智能调度算法，实现计算资源的智能调度。             |
| geostack-telescopic                      | 智能伸缩模块，封装智能伸缩逻辑，定时查询资源的工作状态，实现计算资源的智能伸缩。 |
| geostack-core                            | 核心处理模块，封装云平台基础设施管理、静态主机管理、订单核心业务处理、磁盘扩容、系统依赖版本、云平台类型、二次开发、haproxy消息调用等功能。 |
| geostack-log                             | 日志管理模块，封装日志入库、日志查询、日志归档以及核心模块操作日志等功能。    |
| geostack-gistools                        | GIS工具投递模块，封装GIS工具应用的投递与删除等管理功能。          |
| geostack-servicegoods                    | 服务类型商品模块，封装GeoGlobe和GeoSmarter服务类型管理、服务投递、服务访问统计等功能。 |
| geostack-proxy                           | 服务代理模块，封装服务代理核心功能。                       |
| geostack-balance-core、geostack-balance-haproxy | haproxy负载均衡消息构建模块，封装服务添加删除、负载节点添加删除等功能。  |
| geostack-databasegoods                   | 数据库商品模块，封装MySQL、MySQL集群、MongoDB集群商品的投递功能。 |
| geostack-portal                          | 门户模块，封装商品类型展示和商品投递参数组织功能。                |
| geostack-quartz                          | 任务调度管理模块，实现调度任务的创建、配置、删除等功能。             |
| geostack-rest-manage                     | REST请求管理模块，封装用户私钥管理，实现REST请求权限控制功能。      |
| geostack-test                            | 测试组件，仅包含BaseTest一个测试抽象类，方便GeoStack综合运维各模块代码测试流程。 |

### 独立运维组件

| 模块              | 功能概述                                     |
| --------------- | ---------------------------------------- |
| geostack-soms   | SOMS运维管理模块，封装数据源管理、边界管理、金字塔管理、地统计模型管理，以及服务协议、服务类型、服务接口等读取功能。 |
| geostack-zabbix | zabbix监控对接模块，封装监控分组、监控主机类型、监控模板、触发器、监控项、网络发现、监控预警规则、预警邮件、监控状态、监控描述的配置管理功能。 |

### 监控组件

| 模块                      | 功能概述                                     |
| ----------------------- | ---------------------------------------- |
| geostack-monitor-common | 监控隔离驱动模块，定义了监控的隔离驱动的公共接口，屏蔽实现监控的细节。      |
| geostack-monitor-zabbix | 监控Zabbix适配层，Zabbix监控的适配实现。               |
| geostack-spark-api      | Spark监控的REST API包，提供了Spark的REST API的java封装，针对Spark服务器REST API信息的获取。 |
| geostack-zabbix-api     | Zabbix API包，Zabbix官方REST API的java封装，获取Zabbix监控信息。 |

### 用户系统

| 模块         | 功能概述                             |
| ---------- | -------------------------------- |
| Usersystem | 用户管理模块，封装用户、机构、角色、权限、菜单等模块的管理功能。 |

