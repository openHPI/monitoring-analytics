# Using Template tasks
[Link to Documentation](https://docs.influxdata.com/kapacitor/v1.5/working/template_tasks/)

## Available Templates
 * __generic_ht_alert:__ A template for triggering alerts based on provided lambda functions. No windowing. (Example: crit if usage_idle < 90)

## Define a Template in Kapacitor
```
kapacitor define-template generic_ht_alert -tick /home/kapacitor/templates/hard-threshold.tick
```
```
kapacitor show-template generic_ht_alert
```

## Define a Task based on Template
```
kapacitor define cpu_alert -template generic_ht_alert -vars /home/kapacitor/cpu_vars.json
```
```
kapacitor show cpu_alert
```
