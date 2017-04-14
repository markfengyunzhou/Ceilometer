## step 1: 
```
curl -i -X POST http://192.168.147.130:35357/v3/auth/tokens -H "Content-type: application/json" -d '{"auth": {"identity": {"methods": ["password"], "password": {"user" : {"id": "09fd1ed8be4b4805be52afd1d06ec044", "password": "admin"}}}, "scope" : {"project" : {"id" : "0c05d69ecac3431d9853657b30e5de6d"}}}}' | grep Token
```

## step 2:
```
curl -g -i -X 'GET' 'http://192.168.147.130:8041/v1/resource/instance_network_interface' -H 'X-Auth-Token: 6a87be2d125a4be89f8b89f859408f11'
```

## instance_network_interface info:
```
[
    {
        "created_by_user_id": "f62ba41eb2fb431a9f240142914c033a",
        "metrics": {
            "network.outgoing.packets.rate": "c9ca4c48-b2ad-4174-b0a6-30ddeffff2ad",
            "network.outgoing.packets.drop": "f96b9612-f062-4132-9868-fd0b0aacbaa2",
            "network.incoming.packets.drop": "2a480439-314e-4c92-837d-b0721e388440",
            "network.incoming.packets.error": "8a864576-0981-45cb-8350-5920b54eb286",
            "network.incoming.bytes.rate": "38128453-743a-40a6-9db2-1fe46e564e2e",
            "network.outgoing.bytes.rate": "1a425336-f88c-4bbd-9379-cc0faabe6903",
            "network.outgoing.packets.error": "8522eed1-cca3-4c8a-96a5-b5294b8237fc",
            "network.incoming.packets.rate": "298e176f-9b54-4716-bc03-2d3913dda45b",
            "network.outgoing.bytes": "f4773ae6-8e16-4e02-95ca-1bc28df1d8da",
            "network.incoming.bytes": "cf8a4a0e-1896-4d95-89c6-8b6f0f5ee817",
            "network.outgoing.packets": "fac960b4-a0e6-4ed6-9cf8-718949c81b94",
            "network.incoming.packets": "c0d1f211-bfa4-4008-a221-ba5221feea9c"
        },
        "started_at": "2017-04-12T01:32:47.861755+00:00",
        "revision_start": "2017-04-12T01:32:47.861802+00:00",
        "revision_end": null,
        "creator": "f62ba41eb2fb431a9f240142914c033a:8175731463a2490dbcb11f86d1fc3730",
        "created_by_project_id": "8175731463a2490dbcb11f86d1fc3730",
        "id": "de6df0a7-9b5a-5041-8391-02a07e78c1ba",
        "instance_id": "fde0a7bc-e8ab-438d-b44f-f28d1f2d5216",
        "original_resource_id": "instance-00000001-fde0a7bc-e8ab-438d-b44f-f28d1f2d5216-tap9d5950fc-b5",
        "user_id": "0a832ed8f5b2488a9ab5748c8d88afb9",
        "project_id": "51db5d5b6d924407b7b985178426e030",
        "type": "instance_network_interface",
        "ended_at": null,
        "name": "tap9d5950fc-b5"
    },
    {
        "created_by_user_id": "f62ba41eb2fb431a9f240142914c033a",
        "metrics": {
            "network.outgoing.packets.rate": "a01ab7a1-4f62-4d9b-b929-aa09e6f31a23",
            "network.outgoing.packets.drop": "e9b2b7a1-1b1c-45eb-bc7f-77c5b7677a73",
            "network.incoming.packets.drop": "805a2907-0f3c-467b-963d-3a7c2c7bfdfd",
            "network.incoming.packets.error": "6552f309-a49f-40cc-ae1d-94a7c0b1e4cc",
            "network.incoming.bytes.rate": "651e436a-2577-4c0b-86a4-e61318a1b1cb",
            "network.outgoing.bytes.rate": "01315ad1-bd0c-4405-9d34-f06060179f54",
            "network.outgoing.packets.error": "c2ab57bd-24e5-45a4-979d-87a67eda42f3",
            "network.incoming.packets.rate": "26cc434e-3efd-4c66-9b0b-7fa29ebd176e",
            "network.outgoing.bytes": "35f18caf-77f0-4a7e-bf25-1e110e20eaa0",
            "network.incoming.bytes": "53bc349a-f066-41ab-8509-92b4ce5f3461",
            "network.outgoing.packets": "04672cc4-89b7-4ec6-a115-cf54a3443759",
            "network.incoming.packets": "03002775-7482-4cef-99b2-5d6de568cf66"
        },
        "started_at": "2017-04-12T02:02:32.587368+00:00",
        "revision_start": "2017-04-12T02:02:32.587404+00:00",
        "revision_end": null,
        "creator": "f62ba41eb2fb431a9f240142914c033a:8175731463a2490dbcb11f86d1fc3730",
        "created_by_project_id": "8175731463a2490dbcb11f86d1fc3730",
        "id": "8ad56cf2-8e4f-5e11-b380-b89718783a3c",
        "instance_id": "9f676677-37dc-4972-bf67-fb31e2dd7b30",
        "original_resource_id": "instance-00000002-9f676677-37dc-4972-bf67-fb31e2dd7b30-tapdaefadb3-cb",
        "user_id": "0a832ed8f5b2488a9ab5748c8d88afb9",
        "project_id": "51db5d5b6d924407b7b985178426e030",
        "type": "instance_network_interface",
        "ended_at": null,
        "name": "tapdaefadb3-cb"
    }
]
```
