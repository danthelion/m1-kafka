# m1 mac patched confluent kafka (7.0.0) minimal avro python example 😮‍💨

1. install dependencies

```shell
pip install -r requirements.txt
```

3. patch `confluent_kafka/schema_registry/avro.py`

```python
def __init__(self, schema_str, schema_registry_client, from_dict=None, return_record_name=False):
```

3. patch `confluent_kafka/schema_registry/avro.py`

```python
def __init__(self, schema_str, schema_registry_client, to_dict=None, conf=None):
```

4. run kafka locally in Docker

```shell
docker-compose up broker
# wait until broker properly starts
docker-compose up
```

5. start consumer

```shell
python consumer.py
```

6.produce records

```shell
python producer.py
```
