## mutinode模式下，api报gateway time out

原因：默认mongo未创建ceilometer专用db

解决：手动创建ceilometer db


```
mongo --host 192.168.1.30 --port 27017

use ceilometer

db.addUser({user:"ceilometer", pwd:"xxxxxx", roles:["readWrite", "dbAdmin"]})

show tables

```
