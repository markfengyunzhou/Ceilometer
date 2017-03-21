## 概念介绍

 Project > Resource > Meter
 
* Project: 项目 （身份管理-项目）

* Resource: 资源 （如：虚拟机）

* Meter: 计量项 （如：镜像、disk...）

* Sample: 某个 Poject 的某个 Resource 在某一时刻某 Meter 的数值 （如：cpu利用率、disk IO...）
  
     数值类型包括：

        * cumulative：累计值

        * delta：变化值

        * gauge：离散或者波动值

* Statistics: 某区间 Samples 的聚合值 （Count、Max、Min、Avg、Sum）



## Project & Resource List
```
ceilometer --os-username admin --os-password admin --os-auth-url http://100.2.30.82:5000/v3 --os-tenant-name admin resource-list
```
+--------------------------------------+-----------+----------------------------------+----------------------------------+
| Resource ID                          | Source    | User ID                          | Project ID                       |
+--------------------------------------+-----------+----------------------------------+----------------------------------+
| 1e05f8d2-c183-4b11-8777-aac3fda52d3b | openstack | None                             | 284e5148c8ce4ff78140dfc6df90112f |
| 2c6645c7-3bad-4d12-8c3d-fcfc49b469e8 | openstack | b4fbd043d2734b119b285a4710825937 | 6b5d7d3334d84d988fe14245f68f2e2e |
| 3b1abb90-a4d1-4d3b-a62c-7eb5dffaeeaa | openstack | None                             | 284e5148c8ce4ff78140dfc6df90112f |
| 440b782e-cef9-4560-b835-fea2331e5171 | openstack | None                             | 284e5148c8ce4ff78140dfc6df90112f |
| 48e1421e-d832-477e-9d46-96fb21bd55c8 | openstack | b4fbd043d2734b119b285a4710825937 | 284e5148c8ce4ff78140dfc6df90112f |
+--------------------------------------+-----------+----------------------------------+----------------------------------+
