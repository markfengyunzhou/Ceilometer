## step 1: 
```
curl -i -X POST http://192.168.147.130:35357/v3/auth/tokens -H "Content-type: application/json" -d '{"auth": {"identity": {"methods": ["password"], "password": {"user" : {"id": "09fd1ed8be4b4805be52afd1d06ec044", "password": "admin"}}}, "scope" : {"project" : {"id" : "0c05d69ecac3431d9853657b30e5de6d"}}}}' | grep Token
```

## step 2:
```
curl -g -i -X 'GET' 'http://192.168.147.130:8041/v1/resource/instance_disk' -H 'X-Auth-Token: 6a87be2d125a4be89f8b89f859408f11'
```

## instance_disk info:
```
[
    {
        "created_by_user_id": "f62ba41eb2fb431a9f240142914c033a",
        "metrics": {
            "disk.device.latency": "2095ccd9-fd6b-4ff7-9190-ab5209e4e04f",
            "disk.device.read.bytes.rate": "554ab113-5657-4ae6-82ca-feefbb4873a8",
            "disk.device.capacity": "29d3b1ec-a8b2-4190-8eff-0cd9e1c8a779",
            "disk.device.write.requests": "0bf60f9a-d245-4b54-b4cc-da28ddd361b0",
            "disk.device.allocation": "9353ad50-1bb6-4dcc-81f4-50fcba186907",
            "disk.device.write.bytes.rate": "e97975d3-ad5d-4c92-b7e6-e7fe0cce7dba",
            "disk.device.write.requests.rate": "10a38192-baa0-4bf6-b615-4c8e849bc4ee",
            "disk.device.iops": "334386d6-d1e9-4a38-9705-f23d4038082e",
            "disk.device.read.bytes": "0ec0a8d7-034c-4ce4-a546-e11c6a675a07",
            "disk.device.read.requests": "3e380e8f-95f8-4ad7-9eda-9fa3d0cab9d6",
            "disk.device.read.requests.rate": "ee6525bd-c340-403f-bfad-57122e131f5d",
            "disk.device.write.bytes": "a915c4b5-0bc1-4fcc-8a74-f86b2ecb5be2",
            "disk.device.usage": "716ac87c-1ea8-48b7-8f63-4152e3304c91"
        },
        "started_at": "2017-04-12T01:32:48.413044+00:00",
        "revision_start": "2017-04-12T01:32:48.413092+00:00",
        "revision_end": null,
        "creator": "f62ba41eb2fb431a9f240142914c033a:8175731463a2490dbcb11f86d1fc3730",
        "created_by_project_id": "8175731463a2490dbcb11f86d1fc3730",
        "id": "ff91d683-2ed0-57cc-a2a7-5b33e8302c29",
        "instance_id": "fde0a7bc-e8ab-438d-b44f-f28d1f2d5216",
        "original_resource_id": "fde0a7bc-e8ab-438d-b44f-f28d1f2d5216-hda",
        "user_id": "0a832ed8f5b2488a9ab5748c8d88afb9",
        "project_id": "51db5d5b6d924407b7b985178426e030",
        "type": "instance_disk",
        "ended_at": null,
        "name": "hda"
    },
    {
        "created_by_user_id": "f62ba41eb2fb431a9f240142914c033a",
        "metrics": {
            "disk.device.latency": "199f9a3d-f3d0-4be3-b918-eb21080298c1",
            "disk.device.read.bytes.rate": "96005224-57e4-416f-995b-56b3960e35c9",
            "disk.device.capacity": "68ca6341-7afe-4888-b722-47b3d69943a3",
            "disk.device.write.requests": "a295b3a2-96d3-4d67-b57e-d604f14e3b52",
            "disk.device.allocation": "ba19f995-104c-4cf2-8549-0247a3c854ee",
            "disk.device.write.bytes.rate": "b1b663e5-28ac-4266-8fc2-3b548f7e5861",
            "disk.device.write.requests.rate": "486bb5ec-ff65-4024-9c0f-d352af6de646",
            "disk.device.iops": "3a0e971b-b142-4728-bfa7-0ff1b3de9f55",
            "disk.device.read.bytes": "433a1932-77d2-4467-b10c-d4f8420b9f37",
            "disk.device.read.requests": "cff21c7a-70d2-481c-b343-973806488d65",
            "disk.device.read.requests.rate": "8b69b106-8898-4f09-849a-60bf34d6252f",
            "disk.device.write.bytes": "ea2a12d8-bed9-4f41-b006-ad8b2d234a53",
            "disk.device.usage": "4127fbde-a0c4-476d-b14c-cd0252bd3de8"
        },
        "started_at": "2017-04-12T02:02:32.558710+00:00",
        "revision_start": "2017-04-12T02:02:32.558766+00:00",
        "revision_end": null,
        "creator": "f62ba41eb2fb431a9f240142914c033a:8175731463a2490dbcb11f86d1fc3730",
        "created_by_project_id": "8175731463a2490dbcb11f86d1fc3730",
        "id": "4c3f9972-e2f2-56ce-814a-7b011e20869e",
        "instance_id": "9f676677-37dc-4972-bf67-fb31e2dd7b30",
        "original_resource_id": "9f676677-37dc-4972-bf67-fb31e2dd7b30-hda",
        "user_id": "0a832ed8f5b2488a9ab5748c8d88afb9",
        "project_id": "51db5d5b6d924407b7b985178426e030",
        "type": "instance_disk",
        "ended_at": null,
        "name": "hda"
    }
]
```
