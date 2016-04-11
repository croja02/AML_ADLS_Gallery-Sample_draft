# Integrating Azure Machine Learning with Azure Data Lake Store #

An Azure Data Lake is a data repository capable of holding an unlimited amount of data in its native, raw format, including structured, semi-structured, and unstructured data. Ant data structure required for for analysis of the data is not defined until the data is needed.

There are multiple benefits associated with storing data in its native format including maintaining data provenance as well as no loss of information content associated with the extraction, transformation and loading (ETL) of the raw data necessary to persist the data in an alternate store. Industries are starting to extract and place data for analytics into a data lake repository without first transforming the data the way they would need to for a relational data warehouse or key-value store. 
Previous approaches forced all data into a common predetermined schema, or data model. Unlike this monolithic view of a single enterprise-wide data model, the data lake relaxes standardization and defers declaration of a schema, resulting in a nearly unlimited potential for analysis and data discovery. As data volumes, data variety, and metadata richness grow, so does the benefit. It is this diversity and its ability to provide such contextually rich analysis with an imposed 'schema on demand,' that makes an Azure Data Lake such a valuable resource.

Figure 1 and figure 2 below illustrates 

<br/>
![](media/non_ADLS_Analysis.png)
<br/>
Figure 1: Traditional Data Management and Analysis
<br/>
![](media/ADLS_Analysis.png)
<br/>
Figure 2: Data Management and Analysis in an Azure Data Lake Environment. 


**why not use a relational database management system?**
<br/>

Relational data warehouses and their big price tags have long dominated complex analytics, reporting, and operations. (The hospital described earlier, for example, first tried a relational data warehouse.) However, their slow-changing data models and rigid field-to-field integration mappings are too brittle to support big data volume and variety. The vast majority of these systems also leave business users dependent on IT for even the smallest enhancements, due mostly to inelastic design, unmanageable system complexity, and low system tolerance for human error. The data lake approach circumvents these problems.


**How about HBase, etc?**
<br/>

HBase is a column-oriented database management system that runs on top of HDFS. 
An HBase system comprises a set of tables. Each table contains rows and columns, much like a traditional database. Each table must have an element defined as a Primary Key, and all access attempts to HBase tables must use this Primary Key.
Think it as a key value store, where the PK is the 'key' and 'value' is all of the columns.
 
Access with Hive or Impala.

**Differences with Azure Storage**
<br/>
What are the differences between Azure Data Lake and Azure Storage?  In summary, this includes petabyte file sizes, high throughput, and built-in Hadoop integration.  Azure Storage is a generic store for many use cases whereas Azure Data Lake is optimized for doing big data analytics.

Currently there is no direct path between a Data Lake Store and an Azure Machine Learning Model. Azure Machine Learning models can consume data from a number of sources, such as a blob Store, table store, Azure SQL Database, and HDInsight (hive query).


The cost of innovation....
