## resource rest api
```
curl -g -i -X 'GET' 'http://192.168.147.130:8041/v1/resource' -H 'X-Auth-Token: 4da8068605f8413fb31054823308516c'
```
```
{
    "instance_network_interface": "http://192.168.147.130:8041/v1/resource/instance_network_interface",
    "ceph_account": "http://192.168.147.130:8041/v1/resource/ceph_account",
    "network": "http://192.168.147.130:8041/v1/resource/network",
    "host_network_interface": "http://192.168.147.130:8041/v1/resource/host_network_interface",
    "generic": "http://192.168.147.130:8041/v1/resource/generic",
    "ipmi": "http://192.168.147.130:8041/v1/resource/ipmi",
    "image": "http://192.168.147.130:8041/v1/resource/image",
    "host_disk": "http://192.168.147.130:8041/v1/resource/host_disk",
    "swift_account": "http://192.168.147.130:8041/v1/resource/swift_account",
    "volume": "http://192.168.147.130:8041/v1/resource/volume",
    "instance": "http://192.168.147.130:8041/v1/resource/instance",
    "host": "http://192.168.147.130:8041/v1/resource/host",
    "instance_disk": "http://192.168.147.130:8041/v1/resource/instance_disk",
    "stack": "http://192.168.147.130:8041/v1/resource/stack",
    "identity": "http://192.168.147.130:8041/v1/resource/identity"
}
```
## resource type info
```
curl -g -i -X 'GET' 'http://192.168.147.130:8041/v1/resource_type' -H 'X-Auth-Token: 4da8068605f8413fb31054823308516c'
```
```
[
    {
        "attributes": {},
        "state": "active",
        "name": "ceph_account"
    },
    {
        "attributes": {},
        "state": "active",
        "name": "generic"
    },
    {
        "attributes": {
            "host_name": {
                "min_length": 0,
                "max_length": 255,
                "type": "string",
                "required": true
            }
        },
        "state": "active",
        "name": "host"
    },
    {
        "attributes": {
            "host_name": {
                "min_length": 0,
                "max_length": 255,
                "type": "string",
                "required": true
            },
            "device_name": {
                "min_length": 0,
                "max_length": 255,
                "type": "string",
                "required": false
            }
        },
        "state": "active",
        "name": "host_disk"
    },
    {
        "attributes": {
            "host_name": {
                "min_length": 0,
                "max_length": 255,
                "type": "string",
                "required": true
            },
            "device_name": {
                "min_length": 0,
                "max_length": 255,
                "type": "string",
                "required": false
            }
        },
        "state": "active",
        "name": "host_network_interface"
    },
    {
        "attributes": {},
        "state": "active",
        "name": "identity"
    },
    {
        "attributes": {
            "container_format": {
                "min_length": 0,
                "max_length": 255,
                "type": "string",
                "required": true
            },
            "disk_format": {
                "min_length": 0,
                "max_length": 255,
                "type": "string",
                "required": true
            },
            "name": {
                "min_length": 0,
                "max_length": 255,
                "type": "string",
                "required": true
            }
        },
        "state": "active",
        "name": "image"
    },
    {
        "attributes": {
            "display_name": {
                "min_length": 0,
                "max_length": 255,
                "type": "string",
                "required": true
            },
            "host": {
                "min_length": 0,
                "max_length": 255,
                "type": "string",
                "required": true
            },
            "image_ref": {
                "min_length": 0,
                "max_length": 255,
                "type": "string",
                "required": false
            },
            "flavor_id": {
                "min_length": 0,
                "max_length": 255,
                "type": "string",
                "required": true
            },
            "server_group": {
                "min_length": 0,
                "max_length": 255,
                "type": "string",
                "required": false
            }
        },
        "state": "active",
        "name": "instance"
    },
    {
        "attributes": {
            "instance_id": {
                "required": true,
                "type": "uuid"
            },
            "name": {
                "min_length": 0,
                "max_length": 255,
                "type": "string",
                "required": true
            }
        },
        "state": "active",
        "name": "instance_disk"
    },
    {
        "attributes": {
            "instance_id": {
                "required": true,
                "type": "uuid"
            },
            "name": {
                "min_length": 0,
                "max_length": 255,
                "type": "string",
                "required": true
            }
        },
        "state": "active",
        "name": "instance_network_interface"
    },
    {
        "attributes": {},
        "state": "active",
        "name": "ipmi"
    },
    {
        "attributes": {},
        "state": "active",
        "name": "network"
    },
    {
        "attributes": {},
        "state": "active",
        "name": "stack"
    },
    {
        "attributes": {},
        "state": "active",
        "name": "swift_account"
    },
    {
        "attributes": {
            "display_name": {
                "min_length": 0,
                "max_length": 255,
                "type": "string",
                "required": false
            },
            "volume_type": {
                "min_length": 0,
                "max_length": 255,
                "type": "string",
                "required": false
            }
        },
        "state": "active",
        "name": "volume"
    }
]
```
