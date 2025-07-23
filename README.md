# net-kusto-client

This package is used to query and ingest data into kusto

## To Install

```
py -m pip install net-kusto-client
Please create local.settings.json file in your home folder, you can also copy example.csv to home folder for testing.
~/
├── local.settings.json
├── example.csv
```

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
