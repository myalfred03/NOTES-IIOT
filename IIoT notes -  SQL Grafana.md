**Timestream / Grafana**

**Select From Timestream**

ALL Data on Table

```
select * from "DB-data"."sensor-data"
```

Only a value of table with timestamp, these data streaming from a unique device

```
select time, measure_value::double as temp from "DB-data"."sensor-data" WHERE measure_name = 'temp' and "device-id" = 'gateway2'

```
