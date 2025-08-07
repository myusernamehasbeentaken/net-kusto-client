# net-kusto-client

This package is used to query and ingest data into kusto

## To Install

Create a free kusto cluster following these instructions, https://learn.microsoft.com/en-us/azure/data-explorer/start-for-free-web-ui
```
py -m pip install net-kusto-client
```

Please create local.settings.json file in your home folder, you can also copy example.csv to home folder for testing.

```
~/
├── local.settings.json
├── example.csv
```

The client_id in local.settings.json can be either the aad application id or the user-assigned managed identity. The client_secret is used as the application key.

## Usage
```
import net_kusto_client
k_client = net_kusto_client.NetKustoClient()
k_client.create_sample_table()
k_client.ingest_sample_data()
k_client.execute_sample_query()
k_client.execute_stormevents_sample_query()
```

On the kusto database you can delete the table using 
.drop table DeviceInfo
