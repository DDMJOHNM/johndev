---
title: "Elastic Search"
date: 2022-10-18T16:56:59+13:00
draft: true
---

# Amazon Open Search 

AWS Cli

## Open Search Domain 
- Clusters with settings 
- Standard endpoint - load streaming data from s3, Dynamo DB etc 
- Lambda/Python
- Addtags 
- Blue/green deployment 
- Stats
- Indexing 
- Cognito Auth / Opensearch dashboards Access Control (JS Application)

## Upload data for Indexing 
- Signing and compressing http requests/gzip
 
##  Search Documenting 
- Async Search Settings (Plugin)
- Running Concurrent Searches
- Cross Cluster 
- Probabilistic ranking framework
- Amazon EC2 Instance 
- Cold/Ultrawarm storage 
- Index Rollups  
- Reindex Large Datasets - Scroll Request with the following default values
- Naming restrictions for indexes
- Reducing response size 
- TTL set by index / expiration by document 
- Php Non Blocking Async  

## Best practices
- Sizing Domains  
- Petabyte Scale
- Dedicated Master Nodes
- Recommended Cloud Watch Alarms 

Adding a document to an index - postman  
Update a document
Bulk actions - post/bulk  
Searching for dccuments 

```
Basic Search
GET veggies/_search?q=name:l*

Advanced Search
GET veggies/_search
{
  "query": {
    "term": {
      "name": "lettuce"
    }
  }
}
```

## Creating a search application
Create Api in the gateway console. 
```
First, you create a policy to describe when an index will be deleted

PUT http://localhost:9200/_ilm/policy/delete_log_after_2day <- Your policy name

{
  "policy": {
    "phases": {
      "hot": {
        "min_age": "0ms",
        "actions": {
          "set_priority": {
            "priority": 0
          }
        }
      },
      "delete": {
        "min_age": "2d", <-- Set your TTL here
        "actions": {
          "delete": {
            "delete_searchable_snapshot": true
          }
        }
      }
    }
  }
}

```

[References]

(https://docs.aws.amazon.com/opensearch-service/latest/developerguide/asynchronous-search.html)

(https://stackoverflow.com/questions/69302245/how-to-set-ttl-for-documents-in-elasticsearch-index)