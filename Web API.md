## 概念介绍

 ### Project > Resource > Meter
 
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
    ceilometer --os-username admin \
               --os-password admin \
               --os-auth-url http://100.2.30.82:5000/v3 \
               --os-tenant-name admin \
               resource-list
```
![](https://github.com/markfengyunzhou/Ceilometer/blob/master/Images/resources.png)

## Meter List
```
    ceilometer --os-username admin \
               --os-password admin \
               --os-auth-url http://100.2.30.82:5000/v3 \
               --os-tenant-name admin \
               --os-project-id 284e5148c8ce4ff78140dfc6df90112f \
               meter-list
```
![](https://github.com/markfengyunzhou/Ceilometer/blob/master/Images/meters.png)

## Statistics Examples
   
* 统计当前租户cpu（meter）使用信息

```
    ceilometer --os-username admin \
               --os-password admin \
               --os-auth-url http://100.2.30.82:5000/v3 \
               --os-tenant-name admin \
               statistics  
               -m cpu -p 10000000   
``` 
![](https://github.com/markfengyunzhou/Ceilometer/blob/master/Images/statistics_tenant.png)
   
* 统计某project的cpu（meter）使用信息

```
    ceilometer --os-username admin \
               --os-password admin \
               --os-auth-url http://100.2.30.82:5000/v3 \
               --os-tenant-name admin  \
               statistics  \
               -m cpu -p 10000000 -q project_id=284e5148c8ce4ff78140dfc6df90112f
```
![](https://github.com/markfengyunzhou/Ceilometer/blob/master/Images/statistics_project.png)

* 统计某resource的cpu（meter）使用信息

```
    ceilometer --os-username admin \
               --os-password admin \
               --os-auth-url http://100.2.30.82:5000/v3 \
               --os-tenant-name admin  \
               statistics  \
               -m cpu -p 10000000 -q resource_id=67de99c6-792c-4a02-ab1c-c92bb310fdc3
```
![](https://github.com/markfengyunzhou/Ceilometer/blob/master/Images/statistics_resource.png)

* 统计某user的cpu（meter）使用信息

```
    ceilometer --os-username admin \
               --os-password admin \
               --os-auth-url http://100.2.30.82:5000/v3 \
               --os-tenant-name admin  \
               statistics  \
               -m cpu -p 10000000 -q user_id=b4fbd043d2734b119b285a4710825937
```
![](https://github.com/markfengyunzhou/Ceilometer/blob/master/Images/statistics_user.png)
