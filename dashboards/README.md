# Grafana Dashboards

This directory contains Grafana dashboard JSON files for visualizing kube-burner metrics and performance data.

## Dashboards

### Virt-dv-scale-density.json

The `Virt-dv-scale-density.json` dashboard is designed to visualize the results of the **virt-dv-scale-density** workload, providing an overview of performance and metrics collected during its execution.

## Importing Dashboards

To import a dashboard into Grafana:

1. Navigate to your Grafana instance
2. Go to **Dashboards** → **Import**
3. Upload the JSON file or paste its contents
4. Click **Import**

## Datasource Configuration

All dashboards require either Elasticsearch or OpenSearch datasources to be configured in Grafana.

> [!NOTE]  
> Remember to use `timestamp` as Time field name in the datasource

