# Managing Data Sources

On EnOS<sup>TM</sup> IoT platform, a Report DB is created by default for organizations with the BI & Report module enabled. The Report DB enables segregated storage of organization resources to ensure data security. You can use the Data Explorer tools to create data source tables in the Report DB, and then use the Data Integration tools to synchronize data from Hive to the target data source tables.

## Procedure

1. Add data sources.

   Log in the EnOS Console and select **Data Source** from the left navigation panel. Click the **Add Data Source** button to complete adding data sources. For information about supported data source types and how to configure data source connection, see [Managing Data Sources](managing_datasource).

2. Create target tables.

   Select **Data Explorer** from the left navigation panel and click the **New note** button to create target tables. For details, see [Creating a Hive Table](https://docs.envisioniot.com/docs/data-explorer/en/latest/creating_hivetable.html). If target tables already exist, you can skip this step.

3. Create data integration tasks.

   Select **Data Integration** from the left navigation panel and click **New data integration task** and complete the configuration of the task flow. Based on your business needs, you can use data filters to synchronize partial data from the data sources. For details, see [Data Integration](https://docs.envisioniot.com/docs/offline-data/en/latest/data_integration/index.html).

4. (Optional) Create data development tasks.

   If the data ETL development logic is complex, you can create data development tasks through **Data IDE** > **Task Designer** > **New Workflow**. For details about workflow configuration, see [Data IDE Overview](https://docs.envisioniot.com/docs/offline-data/en/latest/data_ide/dataide_overview.html).

5. Run and monitor the tasks.

   After the data development task is created, click the **Pre-run** button and specify the triggering time for the task. Then, select **Task Monitor** from the left navigation to view the running status of the workflow. For details, see [Task Monitor](https://docs.envisioniot.com/docs/offline-data/en/latest/task_monitor/index.html).

6. Check data synchronization results.

   After the tasks are running successfully, select **Data Explorer** from the left navigation panel to check the data that are synchronized to the Hive tables.

7. Create target tables in the Report DB.

   Select **Data Explorer** from the left navigation panel and create a note of "mysql_report" type for target tables in the Report DB. If target tables already exist, you can skip this step.

8. Synchronize table data to the Report DB.

   Select **Data Integration** from the left navigation panel and click **New data integration task** and complete the configuration of the task flow. Select **HIVE** as the data source type and **REPORTDB** as the target source type. Click the **Pre-run** button to test the task flow, then check the task running status in **Task Monitor**.

## Follow-up Operations

After data synchronization is completed, you can create datasets by single table model or SQL model. For details, see [Creating Datasets](creating_dataset).
