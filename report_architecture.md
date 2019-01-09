# System Architecture

The architecture of the BI & Report service is shown as follows.

.. image:: media/infrastructure.png
   :width: 500px


The major modules and their functions are described in the following sections.

## Data Processing Module

- **Data Source**

  By default, EnOS system creates a Report DB for organizations with the BI & Report module enabled. The feature of the Report DB is high real-time query efficiency, which meets the requirement of data analysis well. You can use the data integration function to synchronize data from Hive to the Report DB, thus completing data preparation.

- **Dataset Designer**

  Dataset Designer supports flexible dataset editing functions, such as creating, editing, copying, deleting, and transforming dimensions and measures. Meanwhile, the default aggregation of dimensions and measures can also be configured, including sum, count, max, min, and avg. The dataset can be referenced directly in the report design phase, so that you can focus on the report design instead of caring about the underlying logical processing of the source tables.

- **Dataset Manager**

  Dataset Manager supports the lifecycle management of datasets, including operations like creating, deleting, copying, and editing. After connecting to data sources, datasets can be created on the basis of one or more data source tables by creating single tables or multiple tables with SQL statements.

## Data Visulization Module

- **Report Designer**

  Report Designer applies flexible tiles layout to display the interaction of report data. Report content can be customized in a WYSIWYG way by dragging the charts to adjust the layout according to business needs, supporting various methods of data filtering and query, and also providing a rich set of charts and controls for data visualization. The reports can also be exported as PDF files.

- **Report Manager**

  Report Manager supports the lifecycle management of reports, including operations like creating, deleting, copying, and editing. Furthermore, created reports can be published, either open to all people in the organization, or visible only to the report owner.

- **Visulization Control Library**

  BI & Report provides a rich set of charts and controls to meet the needs of data visualization and analysis in most business scenarios. Charts include bar charts, polyline charts, pie charts, crosstabs, scatter charts, indicator blocks, dashboards, and highlight tables. Controls include query, IFrame, text box, pictures, and so on.

## Security Management Module

- **Data Security**

  By default, EnOS platform creates a Report DB for organizations with the BI & Report module enabled, which isolates the storage of organization resources. Besides, the BI & Report service is integrated with the EnOS IAM (indentity and access management) system. Access to published reports requires user account login and authentication.
