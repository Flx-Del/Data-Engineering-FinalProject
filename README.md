# Airbnb Listings Data Warehouse

Repository name suggestion: `airbnb-listings-data-warehouse`

Final project for building an Airbnb listings data warehouse with Pentaho Data Integration and presenting the results in Power BI.

## Project Structure

```text
dashboard/
  DATENG project.pbix
docs/
  Laporan Data Engineering.pdf
etl/
  pentaho/
    Job.kjb
    fact.ktr
    hostDim.ktr
    neighborhoodDim.ktr
```

## Data Pipeline

The Pentaho job runs the host dimension, neighborhood dimension, and listing fact transformations in sequence. The transformations read from `oltp_airbnb.mytable` and write to the `projectdataeng_olap` schema.

## Requirements

- Pentaho Data Integration (Spoon)
- MySQL source and target databases
- Power BI Desktop to open the dashboard

Configure the database connections named `DataEngineeringOltp` and `DataEngineeringOlap` in Pentaho before running the job. Open `etl/pentaho/Job.kjb` in Spoon to run the pipeline. Database credentials and source data are not included in this repository.

## Project Files

- [Pentaho ETL](etl/pentaho/Job.kjb)
- [Power BI dashboard](dashboard/DATENG%20project.pbix)
- [Project report](docs/Laporan%20Data%20Engineering.pdf)
