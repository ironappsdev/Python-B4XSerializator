# B4X Serializator

A Python library for serializing objects to B4X format, enabling seamless data exchange between B4X clients/servers and Python applications.

## Usage

```python
from B4XSerializator import B4XSerializator

serializer = B4XSerializator()
my_dict = {
        "key1": "value1",
        "key2": False,
        "testKey": 123,
        "nestedList": [1, 2, 3],
        "nestedDict": {"innerKey": "innerValue"},
        "byteData": b'\x00\x01\x02',
        "floatVal": 3.14,
        "longInt": 1234567890123456789,
        "shortInt": 12345,
        "byteInt": -128,
        "nullValue": None
    }
bytes_data = serializer.convert_object_to_bytes(my_dict)
```

## Purpose

This library allows Python servers to communicate with B4X clients (and vice versa) by converting Python objects into B4X-compatible byte format. Common use case: Python server serving B4X mobile/desktop applications.