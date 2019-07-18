# 产品优势

{{indexmenu_n>2}}

## 数据安全可靠

UDB
PostgreSQL多道防线保障了数据的安全可靠，高可靠性硬件保障了存储的数据有保障；PostgreSQL的高可用实例保证了有多个数据的冗余存储，同时用户甚至可以使用“创建从库”功能来创建更多数据库数据的备份，进一步增加数据的安全性。
UDB PostgreSQL高可用版支持“秒级回档”
功能，当用户出现人为误操作时，可以利用秒级回档功能把数据恢复到过去7天内的任意一秒。“秒级回档”可以成为用户使用UDB
PostgreSQL产品的“定心丸”。

## 协议完全兼容

UDB PostgreSQL
100%完全兼容PostgreSQL协议，并且默认安装了一些典型PostgreSQL扩展（比如PostGIS地理数据库），做到“开箱即用”的PostgreSQL服务体验。

## 高性能

提供快速高效的数据库查询和事务处理能力，轻松应对高并发、大规模数据处理需求。 每一个UDB
PostgreSQL实例背后有强大的硬件作为支撑。当用户对于硬件和性能有高要求时，可以选择高性能SSD磁盘作为存储介质；UCloud的操作系统内核团队对于每一台运行UDB
PostgreSQL实例的服务器进行了内核级别的调优，保证系统的高性能运行；而UDB
PostgreSQL实例的参数也进过专业DBA的调优，保证可以应对大部分使用场景。

## 高可用

UDB PostgreSQL支持高可用部署，也就是UDB PostgreSQL高可用实例。UDB
PostgreSQL高可用实例采用主从复制架构，主数据库提供服务的同时，有另一套数据库服务不断同步数据并随时待命，大体架构如图所示：

![image](/images/pg-v4.png)

UDB后台强大的自动容灾模块可以在UDB
PostgreSQL高可用实例服务出现问题时自动探测问题，并自动进行容灾，保证用户PostgreSQL数据库服务的稳定可靠。在UDB
PostgreSQL实例进行切换时，容灾模块会把待命的备用PostgreSQL服务提升为主库，并且在原来主服务启动之后回退到从库。整个过程中用户不需要任何人工干预和配置修改。整个容灾的示意图如下图所示：

![image](/images/pg-v4-01.png)

## 轻松应对复杂场景

轻松应对数据量更大、数据类型更复杂的业务场景，如数据挖掘、地图空间数据等；PostGIS扩展支持地理学领域的标准，适用于地图、LBS等业务场景。

## 快速部署

可在线快速部署实例，节省采购、部署、配置等自建数据库工作，缩短项目周期，帮助业务快速上线。

## 灵活弹性扩展

UDB PostgreSQL可依据业务的需要，动态按需扩展数据库资源。只要在控制台上进行几次点击，用户就可以动态调整UDB
PostgreSQL实例的内存和磁盘资源，满足不同业务阶段对于数据库性能和存储空间的需求。特别对于UDB
PostgreSQL高可用实例来说，在进行资源扩容的过程中，用户的数据库服务可以做到基本不停服，只有秒级的闪断。这样可以大大减少数据库的扩容对于数据库服务的影响时间，做到真正的“热升级”。

## 灵活易用

日常运维自动化，UDB
PostgreSQL大大简化了DBA的日常运维工作：做到通过界面点击，DBA可以在分钟级别内一键创建运行标准PostgreSQL协议的数据库服务；UDB
PostgreSQL服务做到每天自动备份，并上传到高可靠的备份存储集群中，省去了用户日常备份的相关工作；UDB
PostgreSQL实时收集数据库监控数据，用户可以通过配置监控阈值来做到及时接收数据库各种异常告警。

## 更低成本

可依据业务需求即时开通所需资源，无需在业务初期采购高成本硬件，有效减少初期的资产投入及避免资源闲置浪费。