---
title: Data warehouse - Wikipedia
source: https://en.wikipedia.org/wiki/Data_warehouse
author:
published: 2001-04-06
created: 2025-11-13
description:
tags:
---

![Data warehouse and data marts overview](https://upload.wikimedia.org/wikipedia/commons/thumb/3/39/Data_Warehouse_%26_Data-Marts_overview.svg/600px-Data_Warehouse_%26_Data-Marts_overview.svg.png)

Data warehouse and data mart overview, with data marts shown in the top right.

In [computing](https://en.wikipedia.org/wiki/Computing "Computing"), a **data warehouse** (**DW** or **DWH**), also known as an **enterprise data warehouse** (**EDW**), is a system used for [reporting](https://en.wikipedia.org/wiki/Business_intelligence "Business intelligence") and [data analysis](https://en.wikipedia.org/wiki/Data_analysis "Data analysis") and is a core component of [business intelligence](https://en.wikipedia.org/wiki/Business_intelligence "Business intelligence").[^1] Data warehouses are central [repositories](https://en.wikipedia.org/wiki/Repository_\(version_control\) "Repository (version control)") of data integrated from disparate sources. They store current and historical data organized in a way that is optimized for data analysis, generation of reports, and developing insights across the integrated data.[^2] They are intended to be used by analysts and managers to help make organizational decisions.[^3]

![](https://upload.wikimedia.org/wikipedia/commons/8/8d/Data_warehouse_architecture.jpg)

The basic architecture of a data warehouse

The data stored in the warehouse is [uploaded](https://en.wikipedia.org/wiki/Upload "Upload") from [operational systems](https://en.wikipedia.org/wiki/Operational_system "Operational system") (such as marketing or sales). The data may pass through an [operational data store](https://en.wikipedia.org/wiki/Operational_data_store "Operational data store") and may require [data cleansing](https://en.wikipedia.org/wiki/Data_cleansing "Data cleansing") for additional operations to ensure [data quality](https://en.wikipedia.org/wiki/Data_quality "Data quality") before it is used in the data warehouse for reporting.

The two main workflows for building a data warehouse system are [extract, transform, load](https://en.wikipedia.org/wiki/Extract,_transform,_load "Extract, transform, load") (ETL) and [extract, load, transform](https://en.wikipedia.org/wiki/Extract,_load,_transform "Extract, load, transform") (ELT).

## Components

The environment for data warehouses and marts includes the following:

- Source systems of data (often, the company's operational databases, such as relational databases [^3]);
- Data integration technology and processes to extract data from source systems, transform them, and load them into a data mart or warehouse;[^3]
- Architectures to store data in the warehouse or marts;
- Tools and applications for varied users;
- Metadata, data quality, and governance processes. Metadata includes data sources (database, table, and column names), refresh schedules and data usage measures.[^3]

### Operational databases

Operational databases are optimized for the preservation of [data integrity](https://en.wikipedia.org/wiki/Data_integrity "Data integrity") and speed of recording of business transactions through use of [database normalization](https://en.wikipedia.org/wiki/Database_normalization "Database normalization") and an [entity–relationship model](https://en.wikipedia.org/wiki/Entity%E2%80%93relationship_model "Entity–relationship model"). Operational system designers generally follow [Codd's 12 rules](https://en.wikipedia.org/wiki/Codd%27s_12_rules "Codd's 12 rules") of [database normalization](https://en.wikipedia.org/wiki/Database_normalization "Database normalization") to ensure data integrity. Fully normalized database designs (that is, those satisfying all Codd rules) often result in information from a business transaction being stored in dozens to hundreds of tables. [Relational databases](https://en.wikipedia.org/wiki/Relational_database "Relational database") are efficient at managing the relationships between these tables. The databases have very fast insert/update performance because only a small amount of data in those tables is affected by each transaction. To improve performance, older data are periodically purged.

Data warehouses are optimized for analytic access patterns, which usually involve selecting specific fields rather than all fields as is common in operational databases. Because of these differences in access, operational databases (loosely, OLTP) benefit from the use of a row-oriented database management system (DBMS), whereas analytics databases (loosely, OLAP) benefit from the use of a [column-oriented DBMS](https://en.wikipedia.org/wiki/Column-oriented_DBMS "Column-oriented DBMS"). Operational systems maintain a snapshot of the business, while warehouses maintain historic data through ETL processes that periodically migrate data from the operational systems to the warehouse.

[Online analytical processing](https://en.wikipedia.org/wiki/Online_analytical_processing "Online analytical processing") (OLAP) is characterized by a low rate of transactions and complex queries that involve aggregations. Response time is an effective performance measure of OLAP systems. OLAP applications are widely used for [data mining](https://en.wikipedia.org/wiki/Data_Mining "Data Mining"). OLAP databases store aggregated, historical data in multi-dimensional schemas (usually [star schemas](https://en.wikipedia.org/wiki/Star_schema "Star schema")). OLAP systems typically have a data latency of a few hours, while data mart latency is closer to one day. The OLAP approach is used to analyze multidimensional data from multiple sources and perspectives. The three basic operations in OLAP are roll-up (consolidation), drill-down, and slicing & dicing.

[Online transaction processing](https://en.wikipedia.org/wiki/Online_transaction_processing "Online transaction processing") (OLTP) is characterized by a large numbers of short online transactions (INSERT, UPDATE, DELETE). OLTP systems emphasize fast query processing and maintaining [data integrity](https://en.wikipedia.org/wiki/Data_integrity "Data integrity") in multi-access environments. For OLTP systems, performance is the number of transactions per second. OLTP databases contain detailed and current data. The schema used to store transactional databases is the entity model (usually [3NF](https://en.wikipedia.org/wiki/Third_normal_form "Third normal form")). Normalization is the norm for data modeling techniques in this system.

[Predictive analytics](https://en.wikipedia.org/wiki/Predictive_analytics "Predictive analytics") is about [finding](https://en.wikipedia.org/wiki/Pattern_recognition "Pattern recognition") and quantifying hidden patterns in the data using complex mathematical models to prepare for different future outcomes, including demand for [products](https://en.wikipedia.org/wiki/Product_\(economics\) "Product (economics)"), and make better decisions. By contrast, OLAP focuses on historical data analysis and is reactive. Predictive systems are also used for [customer relationship management](https://en.wikipedia.org/wiki/Customer_relationship_management "Customer relationship management") (CRM).

### Data marts

A [data mart](https://en.wikipedia.org/wiki/Data_mart "Data mart") is a simple data warehouse focused on a single subject or functional area. Hence it draws data from a limited number of sources such as sales, finance or marketing. Data marts are often built and controlled by a single department in an organization. The sources could be internal operational systems, a central data warehouse, or external data.[^4]

| Attribute | Data warehouse | Data mart |
| --- | --- | --- |
| Scope of the data | enterprise | department |
| Number of subject areas | multiple | single |
| How difficult to build | difficult | easy |
| Memory required | larger | limited |

Types of data marts include [dependent](https://en.wikipedia.org/wiki/Data_mart#Dependent_data_mart "Data mart"), independent, and hybrid data marts.

## Variants

### ETL

The typical [extract, transform, load](https://en.wikipedia.org/wiki/Extract,_transform,_load "Extract, transform, load") (ETL)-based data warehouse uses [staging](https://en.wikipedia.org/wiki/Staging_\(data\) "Staging (data)"), [data integration](https://en.wikipedia.org/wiki/Data_integration "Data integration"), and access layers to house its key functions. The staging layer or staging database stores raw data extracted from each of the disparate source data systems. The integration layer integrates disparate data sets by transforming the data from the staging layer, often storing this transformed data in an [operational data store](https://en.wikipedia.org/wiki/Operational_data_store "Operational data store") (ODS) database. The integrated data are then moved to yet another database, often called the data warehouse database, where the data is arranged into hierarchical groups, often called dimensions, and into [facts](https://en.wikipedia.org/wiki/#Facts) and aggregate facts. The combination of facts and dimensions is sometimes called a [star schema](https://en.wikipedia.org/wiki/Star_schema "Star schema"). The access layer helps users retrieve data.[^5]

The main source of the data is [cleansed](https://en.wikipedia.org/wiki/Data_cleansing "Data cleansing"), transformed, catalogued, and made available for use by managers and other business professionals for [data mining](https://en.wikipedia.org/wiki/Data_mining "Data mining"), [online analytical processing](https://en.wikipedia.org/wiki/OLAP "OLAP"), [market research](https://en.wikipedia.org/wiki/Market_research "Market research") and [decision support](https://en.wikipedia.org/wiki/Decision_support "Decision support").[^6] However, the means to retrieve and analyze data, to extract, transform, and load data, and to manage the [data dictionary](https://en.wikipedia.org/wiki/Data_dictionary "Data dictionary") are also considered essential components of a data warehousing system. Many references to data warehousing use this broader context. Thus, an expanded definition of data warehousing includes [business intelligence tools](https://en.wikipedia.org/wiki/Business_intelligence_tools "Business intelligence tools"), tools to extract, transform, and load data into the repository, and tools to manage and retrieve [metadata](https://en.wikipedia.org/wiki/Metadata "Metadata").

### ELT

![](https://upload.wikimedia.org/wikipedia/commons/thumb/2/2a/ELT_Diagram.png/500px-ELT_Diagram.png)

ELT -based data warehouse architecture

[ELT](https://en.wikipedia.org/wiki/Extract,_load,_transform "Extract, load, transform") -based data warehousing gets rid of a separate [ETL](https://en.wikipedia.org/wiki/Extract,_transform,_load "Extract, transform, load") tool for data transformation. Instead, it maintains a staging area inside the data warehouse itself. In this approach, data gets extracted from heterogeneous source systems and are then directly loaded into the data warehouse, before any transformation occurs. All necessary transformations are then handled inside the data warehouse itself. Finally, the manipulated data gets loaded into target tables in the same data warehouse.

## Benefits

A data warehouse maintains a copy of information from the source transaction systems. This architectural complexity provides the opportunity to:

- Integrate data from multiple sources into a single database and data model. More congregation of data to single database so a single query engine can be used to present data in an [operational data store](https://en.wikipedia.org/wiki/Operational_Data_Store "Operational Data Store").
- Mitigate the problem of isolation-level lock contention in [transaction processing](https://en.wikipedia.org/wiki/Transaction_processing "Transaction processing") systems caused by long-running analysis queries in transaction processing databases.
- Maintain [data history](https://en.wikipedia.org/wiki/Provenance#Data_provenance "Provenance"), even if the source transaction systems do not.
- Integrate data from multiple source systems, enabling a central view across the enterprise. This benefit is always valuable, but particularly so when the organization grows via merging.
- Improve [data quality](https://en.wikipedia.org/wiki/Data_quality "Data quality"), by providing consistent codes and descriptions, flagging or even fixing bad data.
- Present the organization's information consistently.
- Provide a single [common data model](https://en.wikipedia.org/wiki/Common_data_model "Common data model") for all data of interest regardless of data source.
- Restructure the data so that it makes sense to the business users.
- Restructure the data so that it delivers excellent query performance, even for complex analytic queries, without impacting the [operational systems](https://en.wikipedia.org/wiki/Operational_system "Operational system").
- Add value to operational business applications, notably [customer relationship management](https://en.wikipedia.org/wiki/Customer_relationship_management "Customer relationship management") (CRM) systems.
- Make decision–support queries easier to write.
- Organize and disambiguate repetitive data.

## History

The concept of data warehousing dates back to the late 1980s [^7] when IBM researchers Barry Devlin and Paul Murphy developed the "business data warehouse". In essence, the data warehousing concept was intended to provide an architectural model for the flow of data from operational systems to [decision support environments](https://en.wikipedia.org/wiki/Decision_support_system "Decision support system"). The concept attempted to address the various problems associated with this flow, mainly the high costs associated with it. In the absence of a data warehousing architecture, an enormous amount of redundancy was required to support multiple decision support environments. In larger corporations, it was typical for multiple decision support environments to operate independently. Though each environment served different users, they often required much of the same stored data. The process of gathering, cleaning and integrating data from various sources, usually from long-term existing operational systems (usually referred to as [legacy systems](https://en.wikipedia.org/wiki/Legacy_system "Legacy system")), was typically in part replicated for each environment. Moreover, the operational systems were frequently reexamined as new decision support requirements emerged. Often new requirements necessitated gathering, cleaning and integrating new data from " [data marts](https://en.wikipedia.org/wiki/Data_mart "Data mart") " that was tailored for ready access by users.

Additionally, with the publication of The IRM Imperative (Wiley & Sons, 1991) by James M. Kerr, the idea of managing and putting a dollar value on an organization's data resources and then reporting that value as an asset on a balance sheet became popular. In the book, Kerr described a way to populate subject-area databases from data derived from transaction-driven systems to create a storage area where summary data could be further leveraged to inform executive decision-making. This concept served to promote further thinking of how a data warehouse could be developed and managed in a practical way within any enterprise.

Key developments in early years of data warehousing:

- 1960s – [General Mills](https://en.wikipedia.org/wiki/General_Mills "General Mills") and [Dartmouth College](https://en.wikipedia.org/wiki/Dartmouth_College "Dartmouth College"), in a joint research project, develop the terms *dimensions* and *facts*.[^8]
- 1970s – [ACNielsen](https://en.wikipedia.org/wiki/ACNielsen "ACNielsen") and IRI provide dimensional data marts for retail sales.[^8]
- 1970s – [Bill Inmon](https://en.wikipedia.org/wiki/Bill_Inmon "Bill Inmon") begins to define and discuss the term *data warehouse*.[^9] [^10] [^11]
- 1975 – [Sperry Univac](https://en.wikipedia.org/wiki/Sperry_Univac "Sperry Univac") introduces [MAPPER](https://en.wikipedia.org/wiki/MAPPER "MAPPER") (*maintain, prepare, and produce executive reports*), a database management and reporting system that includes the world's first [4GL](https://en.wikipedia.org/wiki/Fourth-generation_programming_language "Fourth-generation programming language"). It is the first platform designed for building information centers (a forerunner of contemporary data warehouse technology).
- 1983 – [Teradata](https://en.wikipedia.org/wiki/Teradata "Teradata") introduces the [DBC/1012](https://en.wikipedia.org/wiki/DBC_1012 "DBC 1012") database computer specifically designed for decision support.[^12]
- 1984 – [Metaphor Computer Systems](https://en.wikipedia.org/wiki/Metaphor_Computer_Systems "Metaphor Computer Systems"), founded by [David Liddle](https://en.wikipedia.org/wiki/David_Liddle "David Liddle") and Don Massaro, releases a hardware/software package and GUI for business users to create a database management and analytic system.
- 1988 – Barry Devlin and Paul Murphy publish the article "An architecture for a business and information system" where they introduce the term "business data warehouse".[^13]
- 1990 – Red Brick Systems, founded by [Ralph Kimball](https://en.wikipedia.org/wiki/Ralph_Kimball "Ralph Kimball"), introduces Red Brick Warehouse, a database management system specifically for data warehousing.
- 1991 – James M. Kerr authors "The IRM Imperative", which suggests data resources could be reported as an asset on a balance sheet, furthering commercial interest in the establishment of data warehouses.
- 1991 – Prism Solutions, founded by [Bill Inmon](https://en.wikipedia.org/wiki/Bill_Inmon "Bill Inmon"), introduces Prism Warehouse Manager, software for developing a data warehouse.
- 1992 – [Bill Inmon](https://en.wikipedia.org/wiki/Bill_Inmon "Bill Inmon") publishes the book *Building the Data Warehouse*.[^14]
- 1995 – The Data Warehousing Institute, a for-profit organization that promotes data warehousing, is founded.
- 1996 – [Ralph Kimball](https://en.wikipedia.org/wiki/Ralph_Kimball "Ralph Kimball") publishes the book *The Data Warehouse Toolkit*.[^15]
- 1998 – Focal modeling is implemented as an ensemble (hybrid) data warehouse modeling approach, with Patrik Lager as one of the main drivers.[^16] [^17]
- 2000 – [Dan Linstedt](https://en.wikipedia.org/wiki/Dan_Linstedt "Dan Linstedt") releases in the public domain the [data vault modeling](https://en.wikipedia.org/wiki/Data_vault_modeling "Data vault modeling"), conceived in 1990 as an alternative to Inmon and Kimball to provide long-term historical storage of data coming in from multiple operational systems, with emphasis on tracing, auditing and resilience to change of the source data model.
- 2008 – [Bill Inmon](https://en.wikipedia.org/wiki/Bill_Inmon "Bill Inmon"), along with Derek Strauss and Genia Neushloss, publishes "DW 2.0: The Architecture for the Next Generation of Data Warehousing", explaining his top-down approach to data warehousing and coining the term, data-warehousing 2.0.
- 2008 – [Anchor modeling](https://en.wikipedia.org/wiki/Anchor_modeling "Anchor modeling") was formalized in a paper presented at the International Conference on Conceptual Modeling, and won the best paper award [^18]
- 2012 – [Bill Inmon](https://en.wikipedia.org/wiki/Bill_Inmon "Bill Inmon") develops and makes public technology known as "textual disambiguation". Textual disambiguation applies context to raw text and reformats the raw text and context into a standard data base format. Once raw text is passed through textual disambiguation, it can easily and efficiently be accessed and analyzed by standard business intelligence technology. Textual disambiguation is accomplished through the execution of textual ETL. Textual disambiguation is useful wherever raw text is found, such as in documents, Hadoop, email, and so forth.
- 2013 – Data vault 2.0 was released,[^19] [^20] having some minor changes to the modeling method, as well as integration with best practices from other methodologies, architectures and implementations including agile and CMMI principles

## Data organization

### Facts

A fact is a value or measurement in the system being managed.

Raw facts are ones reported by the reporting entity. For example, in a mobile telephone system, if a [base transceiver station](https://en.wikipedia.org/wiki/Base_transceiver_station "Base transceiver station") (BTS) receives 1,000 requests for traffic channel allocation, allocates for 820, and rejects the rest, it could report three facts to a management system:

- `tch_req_total = 1000`
- `tch_req_success = 820`
- `tch_req_fail = 180`

Raw facts are aggregated to higher levels in various [dimensions](https://en.wikipedia.org/wiki/Dimension_\(data_warehouse\) "Dimension (data warehouse)") to extract information more relevant to the service or business. These are called aggregated facts or summaries.

For example, if there are three BTSs in a city, then the facts above can be aggregated to the city level in the network dimension. For example:

- `tch_req_success_city = tch_req_success_bts1 + tch_req_success_bts2 + tch_req_success_bts3`
- `avg_tch_req_success_city = (tch_req_success_bts1 + tch_req_success_bts2 + tch_req_success_bts3) / 3`

The two most important approaches to store data in a warehouse are dimensional and normalized. The dimensional approach uses a [star schema](https://en.wikipedia.org/wiki/Star_schema "Star schema") as proposed by [Ralph Kimball](https://en.wikipedia.org/wiki/Ralph_Kimball "Ralph Kimball"). The normalized approach, also called the [third normal form](https://en.wikipedia.org/wiki/Third_normal_form "Third normal form") (3NF) is an entity-relational normalized model proposed by Bill Inmon.[^21]

#### Dimensional approach

In a [dimensional approach](https://en.wikipedia.org/wiki/Star_schema "Star schema"), [transaction data](https://en.wikipedia.org/wiki/Transaction_data "Transaction data") is partitioned into "facts", which are usually numeric transaction data, and " [dimensions](https://en.wikipedia.org/wiki/Dimension_\(data_warehouse\) "Dimension (data warehouse)") ", which are the reference information that gives context to the facts. For example, a sales transaction can be broken up into facts such as the number of products ordered and the total price paid for the products, and into dimensions such as order date, customer name, product number, order ship-to and bill-to locations, and salesperson responsible for receiving the order.

This dimensional approach makes data easier to understand and speeds up data retrieval.[^15] Dimensional structures are easy for business users to understand because the structure is divided into measurements/facts and context/dimensions. Facts are related to the organization's business processes and operational system, and dimensions are the context about them (Kimball, Ralph 2008). Another advantage is that the dimensional model does not involve a relational database every time. Thus, this type of modeling technique is very useful for end-user queries in data warehouse.

The model of facts and dimensions can also be understood as a [data cube](https://en.wikipedia.org/wiki/Data_cube "Data cube"),[^22] where dimensions are the categorical coordinates in a multi-dimensional cube, the fact is a value corresponding to the coordinates.

The main disadvantages of the dimensional approach are:

1. It is complicated to maintain the integrity of facts and dimensions, loading the data warehouse with data from different operational systems
2. It is difficult to modify the warehouse structure if the organization changes the way it does business.

#### Normalized approach

In the normalized approach, the data in the warehouse are stored following, to a degree, [database normalization](https://en.wikipedia.org/wiki/Database_normalization "Database normalization") rules. Normalized relational database tables are grouped into *subject areas* (for example, customers, products and finance). When used in large enterprises, the result is dozens of tables linked by a web of joins.(Kimball, Ralph 2008).

The main advantage of this approach is that it is straightforward to add information into the database. Disadvantages include that, because of the large number of tables, it can be difficult for users to join data from different sources into meaningful information and access the information without a precise understanding of the date sources and the [data structure](https://en.wikipedia.org/wiki/Data_structure "Data structure") of the data warehouse.

Both normalized and dimensional models can be represented in entity–relationship diagrams because both contain joined relational tables. The difference between them is the degree of normalization. These approaches are not mutually exclusive, and there are other approaches. Dimensional approaches can involve normalizing data to a degree (Kimball, Ralph 2008).

In *Information-Driven Business*,[^23] [Robert Hillard](https://en.wikipedia.org/w/index.php?title=Robert_Hillard_\(writer\)&action=edit&redlink=1 "Robert Hillard (writer) (page does not exist)") compares the two approaches based on the information needs of the business problem. He concludes that normalized models hold far more information than their dimensional equivalents (even when the same fields are used in both models) but at the cost of usability. The technique measures information quantity in terms of [information entropy](https://en.wikipedia.org/wiki/Entropy_\(information_theory\) "Entropy (information theory)") and usability in terms of the Small Worlds data transformation measure.[^24]

## Design methods

### Bottom-up design

In the *bottom-up* approach, [data marts](https://en.wikipedia.org/wiki/Data_mart "Data mart") are first created to provide reporting and analytical capabilities for specific [business processes](https://en.wikipedia.org/wiki/Business_process "Business process"). These data marts can then be integrated to create a comprehensive data warehouse. The data warehouse bus architecture is primarily an implementation of "the bus", a collection of [conformed dimensions](https://en.wikipedia.org/wiki/Dimension_\(data_warehouse\)#Types "Dimension (data warehouse)") and [conformed facts](https://en.wikipedia.org/w/index.php?title=Facts_\(data_warehouse\)&action=edit&redlink=1 "Facts (data warehouse) (page does not exist)"), which are dimensions that are shared (in a specific way) between facts in two or more data marts.[^25]

### Top-down design

The *top-down* approach is designed using a normalized enterprise [data model](https://en.wikipedia.org/wiki/Data_model "Data model"). ["Atomic" data](https://en.wikipedia.org/wiki/Data_element "Data element"), that is, data at the greatest level of detail, are stored in the data warehouse. Dimensional data marts containing data needed for specific business processes or specific departments are created from the data warehouse.[^26]

### Hybrid design

Data warehouses often resemble the [hub and spokes architecture](https://en.wikipedia.org/wiki/Hub_and_spokes_architecture "Hub and spokes architecture"). [Legacy systems](https://en.wikipedia.org/wiki/Legacy_system "Legacy system") feeding the warehouse often include [customer relationship management](https://en.wikipedia.org/wiki/Customer_relationship_management "Customer relationship management") and [enterprise resource planning](https://en.wikipedia.org/wiki/Enterprise_resource_planning "Enterprise resource planning"), generating large amounts of data. To consolidate these various data models, and facilitate the [extract transform load](https://en.wikipedia.org/wiki/Extract_transform_load "Extract transform load") process, data warehouses often make use of an [operational data store](https://en.wikipedia.org/wiki/Operational_data_store "Operational data store"), the information from which is parsed into the actual data warehouse. To reduce data redundancy, larger systems often store the data in a normalized way. Data marts for specific reports can then be built on top of the data warehouse.

A hybrid (also called ensemble) data warehouse database is kept on [third normal form](https://en.wikipedia.org/wiki/Third_normal_form "Third normal form") to eliminate [data redundancy](https://en.wikipedia.org/wiki/Data_redundancy "Data redundancy"). A normal relational database, however, is not efficient for business intelligence reports where dimensional modelling is prevalent. Small data marts can shop for data from the consolidated warehouse and use the filtered, specific data for the fact tables and dimensions required. The data warehouse provides a single source of information from which the data marts can read, providing a wide range of business information. The hybrid architecture allows a data warehouse to be replaced with a [master data management](https://en.wikipedia.org/wiki/Master_data_management "Master data management") repository where operational (not static) information could reside.

The [data vault modeling](https://en.wikipedia.org/wiki/Data_vault_modeling "Data vault modeling") components follow hub and spokes architecture. This modeling style is a hybrid design, consisting of the best practices from both third normal form and [star schema](https://en.wikipedia.org/wiki/Star_schema "Star schema"). The data vault model is not a true third normal form, and breaks some of its rules, but it is a top-down architecture with a bottom up design. The data vault model is geared to be strictly a data warehouse. It is not geared to be end-user accessible, which, when built, still requires the use of a data mart or star schema-based release area for business purposes.

## Characteristics

There are basic features that define the data in the data warehouse that include subject orientation, data integration, time-variant, nonvolatile data, and data granularity.

### Subject-oriented

Unlike the operational systems, the data in the data warehouse revolves around the subjects of the enterprise. Subject orientation is not [database normalization](https://en.wikipedia.org/wiki/Database_normalization "Database normalization"). Subject orientation can be really useful for decision-making. Gathering the required objects is called subject-oriented.

### Integrated

The data found within the data warehouse is integrated. Since it comes from several operational systems, all inconsistencies must be removed. Consistencies include naming conventions, measurement of variables, encoding structures, physical attributes of data, and so forth.

### Time-variant

While operational systems reflect current values as they support day-to-day operations, data warehouse data represents a long time horizon (up to 10 years) which means it stores mostly historical data. It is mainly meant for data mining and forecasting. (E.g. if a user is searching for a buying pattern of a specific customer, the user needs to look at data on the current and past purchases.) [^27]

### Nonvolatile

The data in the data warehouse is read-only, which means it cannot be updated, created, or deleted (unless there is a regulatory or statutory obligation to do so).[^28]

## Options

### Aggregation

In the data warehouse process, data can be aggregated in data marts at different levels of abstraction. The user may start looking at the total sale units of a product in an entire region. Then the user looks at the states in that region. Finally, they may examine the individual stores in a certain state. Therefore, typically, the analysis starts at a higher level and drills down to lower levels of details.[^27]

### Virtualization

With [data virtualization](https://en.wikipedia.org/wiki/Data_virtualization "Data virtualization"), the data used remains in its original locations and real-time access is established to allow analytics across multiple sources creating a virtual data warehouse. This can aid in resolving some technical difficulties such as compatibility problems when combining data from various platforms, lowering the risk of error caused by faulty data, and guaranteeing that the newest data is used. Furthermore, avoiding the creation of a new database containing personal information can make it easier to comply with privacy regulations. However, with data virtualization, the connection to all necessary data sources must be operational as there is no local copy of the data, which is one of the main drawbacks of the approach.[^29]

## Architecture

The different methods used to construct/organize a data warehouse specified by an organization are numerous. The hardware utilized, software created and data resources specifically required for the correct functionality of a data warehouse are the main components of the data warehouse architecture. All data warehouses have multiple phases in which the requirements of the organization are modified and fine-tuned.[^30]

These terms refer to the level of sophistication of a data warehouse:

Offline operational data warehouse

Data warehouses in this stage of evolution are updated on a regular time cycle (usually daily, weekly or monthly) from the operational systems and the data is stored in an integrated reporting-oriented database.

Offline data warehouse

Data warehouses at this stage are updated from data in the operational systems on a regular basis and the data warehouse data are stored in a data structure designed to facilitate reporting.

On-time data warehouse

Online Integrated Data Warehousing represent the real-time Data warehouses stage data in the warehouse is updated for every transaction performed on the source data

Integrated data warehouse

These data warehouses assemble data from different areas of business, so users can look up the information they need across other systems.[^31]

## In healthcare

In the [healthcare](https://en.wikipedia.org/wiki/Healthcare "Healthcare") sector, data warehouses are critical components of [health informatics](https://en.wikipedia.org/wiki/Health_informatics "Health informatics"), enabling the integration, storage, and analysis of large volumes of clinical, administrative, and operational data. These systems consolidate information from disparate sources such as [electronic health records](https://en.wikipedia.org/wiki/Electronic_health_record "Electronic health record") (EHRs), [laboratory information systems](https://en.wikipedia.org/wiki/Laboratory_information_system "Laboratory information system"), [picture archiving and communication systems](https://en.wikipedia.org/wiki/Picture_archiving_and_communication_system "Picture archiving and communication system") (PACS), and [medical billing](https://en.wikipedia.org/wiki/Medical_billing "Medical billing") platforms. By centralizing data, healthcare data warehouses support a range of functions including [population health](https://en.wikipedia.org/wiki/Population_health "Population health"), [clinical decision support](https://en.wikipedia.org/wiki/Clinical_decision_support_system "Clinical decision support system"), quality improvement, [public health surveillance](https://en.wikipedia.org/wiki/Public_health_surveillance "Public health surveillance"), and [medical research](https://en.wikipedia.org/wiki/Medical_research "Medical research").

Healthcare data warehouses often incorporate specialized data models that account for the complexity and sensitivity of medical data, such as temporal information (e.g., longitudinal patient histories), coded terminologies (e.g., [ICD-10](https://en.wikipedia.org/wiki/ICD-10 "ICD-10"), [SNOMED CT](https://en.wikipedia.org/wiki/SNOMED_CT "SNOMED CT")), and compliance with privacy regulations (e.g., [HIPAA](https://en.wikipedia.org/wiki/Health_Insurance_Portability_and_Accountability_Act "Health Insurance Portability and Accountability Act") in the United States or [GDPR](https://en.wikipedia.org/wiki/General_Data_Protection_Regulation "General Data Protection Regulation") in the European Union).

Following is a list of major patient data warehouses with broad scope (not disease- or [specialty](https://en.wikipedia.org/wiki/Medical_specialty "Medical specialty") -specific), with variables including laboratory results, pharmacy, age, race, socioeconomic status, comorbidities and longitudinal changes:

| Warehouse | Sponsor | Main location | Extent | Access |
| --- | --- | --- | --- | --- |
| [Epic](https://en.wikipedia.org/wiki/Epic_Systems "Epic Systems") **Cosmos** [^32] | [Epic Systems](https://en.wikipedia.org/wiki/Epic_Systems "Epic Systems") | [United States](https://en.wikipedia.org/wiki/United_States "United States") | 296 [^33] million patients | Free for participating organizations |
| **[PCORnet](https://en.wikipedia.org/wiki/Patient-Centered_Outcomes_Research_Institute "Patient-Centered Outcomes Research Institute")** [^32] | [Patient-Centered Outcomes Research Institute](https://en.wikipedia.org/wiki/Patient-Centered_Outcomes_Research_Institute "Patient-Centered Outcomes Research Institute") (PCORI) | United States | 140 million patients | Free for participating organizations |
| **OLDW** (OptumLabs Data Warehouse) | [Optum](https://en.wikipedia.org/wiki/Optum "Optum") | United States | 160 [^34] million patients | For a fee, or for free through certain academic institutions [^35] |
| **EHDEN** [^36] (European Health Data Evidence Network) | Innovative Health Initiative of the [European Union](https://en.wikipedia.org/wiki/European_Union "European Union") | [Europe](https://en.wikipedia.org/wiki/Europe "Europe") | 133 million patients | Free for discovery. May have fees for secondary use.[^37] |

These warehouses enable data-driven healthcare by supporting retrospective studies, [comparative effectiveness research](https://en.wikipedia.org/wiki/Comparative_effectiveness_research "Comparative effectiveness research"), and [predictive analytics](https://en.wikipedia.org/wiki/Predictive_analytics "Predictive analytics"), often with the use of [healthcare-applied artificial intelligence](https://en.wikipedia.org/wiki/Artificial_intelligence_in_healthcare "Artificial intelligence in healthcare").

## See also

- [List of business intelligence software](https://en.wikipedia.org/wiki/Business_intelligence_software "Business intelligence software")
- [Data lake](https://en.wikipedia.org/wiki/Data_lake "Data lake") – Repository of data stored in a raw format
- [Data mesh](https://en.wikipedia.org/wiki/Data_mesh "Data mesh") – Distributed architecture framework for data management

## References

## Further reading

- [Davenport, Thomas H.](https://en.wikipedia.org/wiki/Thomas_H._Davenport "Thomas H. Davenport") and Harris, Jeanne G. *Competing on Analytics: The New Science of Winning* (2007) Harvard Business School Press. [ISBN](https://en.wikipedia.org/wiki/ISBN_\(identifier\) "ISBN (identifier)") [978-1-4221-0332-6](https://en.wikipedia.org/wiki/Special:BookSources/978-1-4221-0332-6 "Special:BookSources/978-1-4221-0332-6")
- Ganczarski, Joe. *Data Warehouse Implementations: Critical Implementation Factors Study* (2009) [VDM Verlag](https://en.wikipedia.org/wiki/VDM_Verlag "VDM Verlag") [ISBN](https://en.wikipedia.org/wiki/ISBN_\(identifier\) "ISBN (identifier)") [3-639-18589-7](https://en.wikipedia.org/wiki/Special:BookSources/3-639-18589-7 "Special:BookSources/3-639-18589-7") [ISBN](https://en.wikipedia.org/wiki/ISBN_\(identifier\) "ISBN (identifier)") [978-3-639-18589-8](https://en.wikipedia.org/wiki/Special:BookSources/978-3-639-18589-8 "Special:BookSources/978-3-639-18589-8")
- Kimball, Ralph and Ross, Margy. *The Data Warehouse Toolkit* Third Edition (2013) Wiley, [ISBN](https://en.wikipedia.org/wiki/ISBN_\(identifier\) "ISBN (identifier)") [978-1-118-53080-1](https://en.wikipedia.org/wiki/Special:BookSources/978-1-118-53080-1 "Special:BookSources/978-1-118-53080-1")
- Linstedt, Graziano, Hultgren. *The Business of Data Vault Modeling* Second Edition (2010) Dan linstedt, [ISBN](https://en.wikipedia.org/wiki/ISBN_\(identifier\) "ISBN (identifier)") [978-1-4357-1914-9](https://en.wikipedia.org/wiki/Special:BookSources/978-1-4357-1914-9 "Special:BookSources/978-1-4357-1914-9")
- William Inmon. *Building the Data Warehouse* (2005) John Wiley and Sons, [ISBN](https://en.wikipedia.org/wiki/ISBN_\(identifier\) "ISBN (identifier)") [978-81-265-0645-3](https://en.wikipedia.org/wiki/Special:BookSources/978-81-265-0645-3 "Special:BookSources/978-81-265-0645-3")
- Watson, H. (2002). Recent Developments in Data Warehousing. Communications of the Association for Information Systems, 8, pp-pp. [https://doi.org/10.17705/1CAIS.00801](https://doi.org/10.17705/1CAIS.00801)

[^1]: Dedić, Nedim; Stanier, Clare (2016). Hammoudi, Slimane; Maciaszek, Leszek; Missikoff, Michele M. Missikoff; Camp, Olivier; Cordeiro, José (eds.). [*An Evaluation of the Challenges of Multilingualism in Data Warehouse Development*](http://eprints.staffs.ac.uk/2770/). [International Conference on Enterprise Information Systems, 25–28 April 2016, Rome, Italy](https://eprints.staffs.ac.uk/2770/1/ICEIS_2016_Volume_1.pdf) (PDF). *Proceedings of the 18th International Conference on Enterprise Information Systems (ICEIS 2016)*. Vol. 1. SciTePress. pp. 196– 206. [doi](https://en.wikipedia.org/wiki/Doi_\(identifier\) "Doi (identifier)"):[10.5220/0005858401960206](https://doi.org/10.5220%2F0005858401960206). [ISBN](https://en.wikipedia.org/wiki/ISBN_\(identifier\) "ISBN (identifier)") [978-989-758-187-8](https://en.wikipedia.org/wiki/Special:BookSources/978-989-758-187-8 "Special:BookSources/978-989-758-187-8"). [Archived](https://web.archive.org/web/20180522180940/https://eprints.staffs.ac.uk/2770/1/ICEIS_2016_Volume_1.pdf) (PDF) from the original on 2018-05-22.

[^2]: ["What is a Data Warehouse? | Key Concepts | Amazon Web Services"](https://aws.amazon.com/data-warehouse/). *Amazon Web Services, Inc*. Retrieved 2023-02-13.

[^3]: Rainer, R. Kelly; Cegielski, Casey G. (2012-05-01). [*Introduction to Information Systems: Enabling and Transforming Business, 4th Edition*](https://archive.org/details/introductiontoin00rain_274) (Kindle ed.). Wiley. pp. [127](https://archive.org/details/introductiontoin00rain_274/page/n138), 128, 130, 131, 133. [ISBN](https://en.wikipedia.org/wiki/ISBN_\(identifier\) "ISBN (identifier)") [978-1118129401](https://en.wikipedia.org/wiki/Special:BookSources/978-1118129401 "Special:BookSources/978-1118129401").

[^4]: ["Data Mart Concepts"](http://docs.oracle.com/html/E10312_01/dm_concepts.htm). Oracle. 2007.

[^5]: Patil, Preeti S.; Srikantha Rao; Suryakant B. Patil (2011). ["Optimization of Data Warehousing System: Simplification in Reporting and Analysis"](http://www.ijcaonline.org/proceedings/icwet/number9/2131-db195). *IJCA Proceedings on International Conference and Workshop on Emerging Trends in Technology*. **9** (6). Foundation of Computer Science: 33– 37.

[^6]: Marakas & O'Brien 2009

[^7]: ["The Story So Far"](https://web.archive.org/web/20080708182105/http://www.computerworld.com/databasetopics/data/story/0%2C10801%2C70102%2C00.html). 2002-04-15. Archived from [the original](http://www.computerworld.com/databasetopics/data/story/0,10801,70102,00.html) on 2008-07-08. Retrieved 2008-09-21.

[^8]: Kimball 2013, pg. 15

[^9]: ["The audit of the Data Warehouse Framework"](http://ceur-ws.org/Vol-19/paper14.pdf) (PDF). [Archived](https://web.archive.org/web/20120512064024/http://ceur-ws.org/Vol-19/paper14.pdf) (PDF) from the original on 2012-05-12.

[^10]: Kempe, Shannon (2012-08-23). ["A Short History of Data Warehousing"](https://www.dataversity.net/a-short-history-of-data-warehousing/). *DATAVERSITY*. Retrieved 2024-05-10.

[^11]: ["Data Warehouse – What It Is & Why It Matters"](https://www.sas.com/en_gb/insights/data-management/data-warehouse.html). *www.sas.com*. Retrieved 2024-05-10.

[^12]: Paul Gillin (February 20, 1984). ["Will Teradata revive a market?"](https://books.google.com/books?id=5pw6ePUC8YYC&pg=PA48). *Computer World*. pp. 43, 48. Retrieved 2017-03-13.

[^13]: Devlin, B. A.; Murphy, P. T. (1988). "An architecture for a business and information system". *IBM Systems Journal*. **27**: 60– 80. [doi](https://en.wikipedia.org/wiki/Doi_\(identifier\) "Doi (identifier)"):[10.1147/sj.271.0060](https://doi.org/10.1147%2Fsj.271.0060).

[^14]: Inmon, Bill (1992). [*Building the Data Warehouse*](https://archive.org/details/buildingdataware00inmo_1). Wiley. [ISBN](https://en.wikipedia.org/wiki/ISBN_\(identifier\) "ISBN (identifier)") [0-471-56960-7](https://en.wikipedia.org/wiki/Special:BookSources/0-471-56960-7 "Special:BookSources/0-471-56960-7").

[^15]: Kimball, Ralph (2011). *The Data Warehouse Toolkit*. Wiley. p. 237. [ISBN](https://en.wikipedia.org/wiki/ISBN_\(identifier\) "ISBN (identifier)") [978-0-470-14977-5](https://en.wikipedia.org/wiki/Special:BookSources/978-0-470-14977-5 "Special:BookSources/978-0-470-14977-5").

[^16]: [Introduction to the focal framework](https://topofminds.se/wp/wp-content/uploads/Focal-Introduction-to-Focal-implementation.pdf)

[^17]: [Data Modeling Meetup Munich: An Introduction to Focal with Patrik Lager - YouTube](https://www.youtube.com/watch?v=C2y92n0sPok)

[^18]: Regardt, Olle; Rönnbäck, Lars; Bergholtz, Maria; Johannesson, Paul; Wohed, Petia (2009). "Anchor Modeling". *Conceptual Modeling - ER 2009*. ER '09. Vol. 5829. Gramado, Brazil: Springer-Verlag. pp. 234– 250. [Bibcode](https://en.wikipedia.org/wiki/Bibcode_\(identifier\) "Bibcode (identifier)"):[2009LNCS.5829..234R](https://ui.adsabs.harvard.edu/abs/2009LNCS.5829..234R). [doi](https://en.wikipedia.org/wiki/Doi_\(identifier\) "Doi (identifier)"):[10.1007/978-3-642-04840-1\_19](https://doi.org/10.1007%2F978-3-642-04840-1_19). [ISBN](https://en.wikipedia.org/wiki/ISBN_\(identifier\) "ISBN (identifier)") [978-3-642-04839-5](https://en.wikipedia.org/wiki/Special:BookSources/978-3-642-04839-5 "Special:BookSources/978-3-642-04839-5").

[^19]: [A short intro to #datavault 2.0](https://en.wikipedia.org/wiki/#dvos2)

[^20]: [Data Vault 2.0 Being Announced](https://en.wikipedia.org/wiki/#dvspec2)

[^21]: Golfarelli, Matteo; Maio, Dario; Rizzi, Stefano (1998-06-01). ["The dimensional fact model: a conceptual model for data warehouses"](https://www.worldscientific.com/doi/abs/10.1142/S0218843098000118). *International Journal of Cooperative Information Systems*. **07** (2n03): 215– 247. [doi](https://en.wikipedia.org/wiki/Doi_\(identifier\) "Doi (identifier)"):[10.1142/S0218843098000118](https://doi.org/10.1142%2FS0218843098000118). [ISSN](https://en.wikipedia.org/wiki/ISSN_\(identifier\) "ISSN (identifier)") [0218-8430](https://search.worldcat.org/issn/0218-8430).

[^22]: ["Introduction to Data Cubes"](http://www2.cs.uregina.ca/~dbd/cs831/notes/dcubes/dcubes.html).

[^23]: Hillard, Robert (2010). *Information-Driven Business*. Wiley. [ISBN](https://en.wikipedia.org/wiki/ISBN_\(identifier\) "ISBN (identifier)") [978-0-470-62577-4](https://en.wikipedia.org/wiki/Special:BookSources/978-0-470-62577-4 "Special:BookSources/978-0-470-62577-4").

[^24]: ["Information Theory & Business Intelligence Strategy - Small Worlds Data Transformation Measure - MIKE2.0, the open source methodology for Information Development"](http://mike2.openmethodology.org/wiki/Small_Worlds_Data_Transformation_Measure). Mike2.openmethodology.org. Retrieved 2013-06-14.

[^25]: ["The Bottom-Up Misnomer - DecisionWorks Consulting"](http://decisionworks.com/2003/09/the-bottom-up-misnomer/). *DecisionWorks Consulting*. 17 September 2003. Retrieved 2016-03-06.

[^26]: Gartner, Of Data Warehouses, Operational Data Stores, Data Marts and Data Outhouses, Dec 2005

[^27]: Paulraj., Ponniah (2010). *Data warehousing fundamentals for IT professionals*. Ponniah, Paulraj. (2nd ed.). Hoboken, N.J.: John Wiley & Sons. [ISBN](https://en.wikipedia.org/wiki/ISBN_\(identifier\) "ISBN (identifier)") [9780470462072](https://en.wikipedia.org/wiki/Special:BookSources/9780470462072 "Special:BookSources/9780470462072"). [OCLC](https://en.wikipedia.org/wiki/OCLC_\(identifier\) "OCLC (identifier)") [662453070](https://search.worldcat.org/oclc/662453070).

[^28]: Inmon, William H. (2005). *Building the data warehouse* (4th ed.). Indianapolis, IN: Wiley Pub. [ISBN](https://en.wikipedia.org/wiki/ISBN_\(identifier\) "ISBN (identifier)") [9780764599446](https://en.wikipedia.org/wiki/Special:BookSources/9780764599446 "Special:BookSources/9780764599446"). [OCLC](https://en.wikipedia.org/wiki/OCLC_\(identifier\) "OCLC (identifier)") [61762085](https://search.worldcat.org/oclc/61762085).

[^29]: Paiho, Satu; Tuominen, Pekka; Rökman, Jyri; Ylikerälä, Markus; Pajula, Juha; Siikavirta, Hanne (2022). ["Opportunities of collected city data for smart cities"](https://doi.org/10.1049%2Fsmc2.12044). *IET Smart Cities*. **4** (4): 275– 291. [doi](https://en.wikipedia.org/wiki/Doi_\(identifier\) "Doi (identifier)"):[10.1049/smc2.12044](https://doi.org/10.1049%2Fsmc2.12044). [S2CID](https://en.wikipedia.org/wiki/S2CID_\(identifier\) "S2CID (identifier)") [253467923](https://api.semanticscholar.org/CorpusID:253467923).

[^30]: Gupta, Satinder Bal; Mittal, Aditya (2009). [*Introduction to Database Management System*](https://books.google.com/books?id=fyQTae6c9l4C). Laxmi Publications. [ISBN](https://en.wikipedia.org/wiki/ISBN_\(identifier\) "ISBN (identifier)") [9788131807248](https://en.wikipedia.org/wiki/Special:BookSources/9788131807248 "Special:BookSources/9788131807248").

[^31]: ["Data Warehouse"](http://www.tech-faq.com/data-warehouse.html). 6 April 2019.

[^32]: Fayanju OM, Haut ER, Itani K (March 2025). ["Practical Guide to Clinical Big Data Sources"](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC12230764). *JAMA Surg*. **160** (3): 344– 346. [doi](https://en.wikipedia.org/wiki/Doi_\(identifier\) "Doi (identifier)"):[10.1001/jamasurg.2024.6006](https://doi.org/10.1001%2Fjamasurg.2024.6006). [PMC](https://en.wikipedia.org/wiki/PMC_\(identifier\) "PMC (identifier)") [12230764](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC12230764). [PMID](https://en.wikipedia.org/wiki/PMID_\(identifier\) "PMID (identifier)") [39775674](https://pubmed.ncbi.nlm.nih.gov/39775674).

[^33]: ["Epic Cosmos"](https://cosmos.epic.com/). *Epic Systems website*. Retrieved 2025-04-13.

[^34]: ["OptumLabs Data Warehouse (OLDW)"](https://data.ucsf.edu/research/oldw). *University of California San Francisco*. Retrieved 2025-04-13.

[^35]: ["Optum Labs"](https://www.medschool.umaryland.edu/cibr/core/optumlabs/?utm_source=chatgpt.com). *University of Maryland*. Retrieved 2025-04-13.

[^36]: Voss EA, Blacketer C, van Sandijk S, Moinat M, Kallfelz M, van Speybroeck M, Prieto-Alhambra D, Schuemie MJ, Rijnbeek PR (December 2023). ["European Health Data & Evidence Network-learnings from building out a standardized international health data network"](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC10746315). *J Am Med Inform Assoc*. **31** (1): 209– 219. [doi](https://en.wikipedia.org/wiki/Doi_\(identifier\) "Doi (identifier)"):[10.1093/jamia/ocad214](https://doi.org/10.1093%2Fjamia%2Focad214). [PMC](https://en.wikipedia.org/wiki/PMC_\(identifier\) "PMC (identifier)") [10746315](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC10746315). [PMID](https://en.wikipedia.org/wiki/PMID_\(identifier\) "PMID (identifier)") [37952118](https://pubmed.ncbi.nlm.nih.gov/37952118).

[^37]: ["Articles of the European Health Data Space (EHDS), Article 42, Fees"](https://www.european-health-data-space.com/European_Health_Data_Space_Article_42_%28Proposal_3.5.2022%29.html). *The European Health Data Space (EHDS)*. Retrieved 2025-04-13.

normalized schemas