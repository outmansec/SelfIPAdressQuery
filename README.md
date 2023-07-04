# SelfIPAdressQuery

一款基于javafx的自有IP地址查询工具

## 使用场景

- 在攻防演习中防守方人员会封禁大量IP地址,人员疏忽会导致自有地址被封禁,可以使用此工具进行批量筛选自有地址.
- IP地址归属批量查询.

## 功能介绍

- 通过IP地址查询数据库中符合的自有IP地址或自有IP段,不存在的IP地址通过离线模式或联网模式查询.
- 支持复制指定字段、清空查询列表、导出查询结果.
- 支持单个IP地址或单个IP段添加自有地址,批量导入按照数据库(Self.db)已有信息为模版批量添加.

## 帮助

- 离线模式数据基于ip2region,文件保存在/conf/ip2region.xdb.
- 联网模式数据基于纯真 IP 库 + ip2region + GeoIP2 整合.
- Self.db是基于sqllite构建的数据库,表SelfIP为自有IP地址,表SelfIPSubnet为自有IP段.
- 自有IP地址优先级高于自有IP段,如果查询IP地址两者均存在匹配,那么会优先显示自有IP地址.
- 软件运行环境JDK1.8.

## 运行图

<img width="764" alt="image" src="https://github.com/outmansec/SelfIPAdressQuery/assets/61048948/346e8a3c-4c06-4b57-9011-a3eea1cfe26b">
