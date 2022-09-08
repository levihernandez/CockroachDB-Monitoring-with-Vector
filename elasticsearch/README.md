## Elasticsearch

> Create a pipeline for CRDB (Elasticsearch 7.6.2)

```bash
curl -X PUT "http://192.168.86.30:9200/_ingest/pipeline/crdb-monitor?pretty" -H 'Content-Type: application/json' -d'
{
  "description" : "CockroachDB Ingest Pipeline",
  "processors" : [
    {
      "set" : {
        "field": "crdb",
        "value": "22.1.6"
      }
    }
  ]
}
'


curl -X GET "http://192.168.86.30:9200/_ingest/pipeline/crdb-monitor?pretty"

```

Follow the steps in Elasticsearch to initialize the pipeline index.
