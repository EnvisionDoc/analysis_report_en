# Key Concepts

The key objects in a reporting platform include data sources, datasets, and reports, as described below.

.. image:: media/report_concepts.png

## Data Source

Before making a report, you need to prepare the data or specify the data source where raw data is located. By default, EnOS system creates a Report DB for organizations with the Data Report module enabled. You can use the data integration function to synchronize data from Hive to the Report DB.

## Dataset

Once a data source is connected, simple logical processing based on one or more data source tables can be performed to get a logic table that has a connection to the source tables. The logical table is a dataset. The dataset can be referenced directly in the report design phase. Therefore, you can focus on the report design instead of caring about the underlying logical processing of the source tables.

## Report

Your report contents can be customized in a WYSIWYG way by dragging the chart to adjust the layout according to your business needs. A report may contain a variety of analysis charts and controls. Filtering, multi-chart association, and other advanced operations are also supported.
