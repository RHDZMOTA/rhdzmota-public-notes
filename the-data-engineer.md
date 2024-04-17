
<div class="alert alert-warning" role="alert">
This blogpost is currently in-progress... consider that anything can change anytime! 
</div>

## Context

To better understand the profile of the data-engineer, we first need to assess the digital-evolution of the company. We usually see the following patterns:

**Phase 0**: The company operates outside the digital realm (paper books, lack of formal or integrated systems).

**Phase 1 (digitalization strategy)**: The end-goal of this phase is to represent the business operation as processes that are managed by a software or at least leave a digital paper trail in the system.
* **Stage 0**: Only accounting data is on digital form (e.g., payments, wire transfers, fund disbursement).
* **Stage 1**: The company is able to measure and capture the output and/or productivity  of their business units (e.g., digital spreadsheets).
* **Stage 2**: The company can model their business processes in software (e.g., flow diagrams, bizagi). Most processes already leave a reliable "papertrail" of their operations in the digital realm.
* **Stage 3**: The company builds and integrates proprietary software into their business operations. The integration is cross-company. At this stage, the software is usually the "source of truth" (OLTP).

**Phase 2 (data strategy)**: the end-goal of this streategy it to allow the company to derive value from data and incoporate a data-driven mindset into the decision making. 
* **Stage 0**: Data infrastructure groundwork by data-architects and data-engineers. The end-goal is to build a data platform (OLAP) to enable advanced reporting and analytics.
* **Stage 1**: The company can use the data platform to understand the current status of the business (descriptive analytics).
* **Stage 2**: The company is able to use the data platform to understand the future path of the company under different scenarios (predictive analytics).
* **Stage 3**: The company is able to take proactive action into shaping their desired future outcome (prescriptive analytics).


A data-engineer can get involved starting into the `Phase 1: Stage 2` all the way into the final stages of the data strategy (`Phase 2: Stage 3`). 

## Profile Specification

A data engineer takes the fundamentals of a software engineer and specializes them into the data-domain. These profiles are usually in charge of designing, implementing, and maintaining the data architecture of your company. The most common use cases are:
* Contribute to the optimization of the data models in the transactional environment.
* Design, implement, and maintain the data platform (OLPA infra).
* Build tailored data-models for analytical purposes.
* Support the data science and machine learning teams with model productivization or feature preprocessing pipelines.


For a complementary definition of a data engineer in relation with other data roles, I highly recommend taking a look into the "Data Roles" post by Wizeline (reference [here](https://www.wizeline.com/data-roles-friends-but-not-the-same/)).

[![](https://hackmd.io/_uploads/rkR1vR3xC.png)](https://www.wizeline.com/data-roles-friends-but-not-the-same/)

<img
src="/img/reference-data-roles-venn-diagram.png"
alt="Data Roles by Wizeline"
width="620" />


## Career Path

The data engineers usually follow a traditional software engineer career path. We commonly have a technical individual contributor path with at least 3 basic seniority levels (junior, mid, senior) and 2 advanced levels that can be:
* **Tech-oriented**: Tech lead, principal engineer, etc.
* **People-oriented**: Manager, director, etc.

![](https://hackmd.io/_uploads/HkDR7ChgR.png)

<img
src="/img/standard-career-path-data-engineer.png"
alt="Standard Carrer Path (Own)"
width="620" />



## Proeficiency Assessment

The seniority assessment evaluation is an evidence-based methodology that attempts to aproximate the corresponding seniority-level for a given candidate.

<div class="alert alert-info" role="alert">
This proeficiency evaluation is designed to assess the level of data engineers from junior to senior.
</div>

### `[TS-GSEE]`  Tech Skills - General Software Engineering Exposure


| Reference | Description |
| --------- | ----------- |
| `TS01`    | Advanced coding proficiency level in at least one programming language: Python, Scala, Rust, etc. |
| `TS02`    | Promoter of coding best practices: documentation, unit testing, types, etc. |
| `TS03`    | Working knowledge about packaging and distribution of source code with dependency management (e.g., code versioning, packaging, virtualenv, docker). |
| `TS04`    | Familiarity with version control (Git), development environments, and CI/CD tools (e.g., Github Actions, Jenkins). |
| `TS05`    | Deep working understanding of funuctional and object-oriented programming paradigms. |
| `TS06`    | Usage of coding design patterns to implement different abstraction levels on a technical solution. |
| `TS07`    | Relevant experience in at least one cloud computing provider: AWS, GCP, Azure, etc. |



### `[TS-DEDE]`  Tech Skills - Data Engineering Domain Expertese

| Reference | Description |
| --------- | ----------- |
| `TS08`    | Advanced SQL proficiency level. |
| `TS09`    | Working understanding about the different designs and needs of the OLTP & OLAP environments.|
| `TS10`    | Relevant experience desinging and implementing data pipelines in at least one paradigm: batch-oriented, streaming, or event-based.|
| `TS11`    | Thorough understanding and ability to implement best practices in ETL/ELT design.|
| `TS12`    | Ability to implement efficient solutions leveraging the following concepts when needed: concurrent, parallel, and/or distributed processing.|
| `TS13`    | Familiar with advanced orchestration software (e.g., Airflow, Prefect, Dagster, etc).|
| `TS14`    | Experience working with relational (e.g., MySQL, Postgresql, etc) and no-sql databases (e.g., MongoDB, Cassandra, ElasticSearch, etc).|
| `TS15`    | Experience working with other popular data-stores (e.g., Redis, Memcache, RabbitMQ)|
| `TS16`    | Experience working with at last one analytical databases/datastores such as Unity Catalog, Snowflake, PrestoDB, TrinoDB, etc.|
| `TS17`    | Experience designing and implementing a data lake or data lakehouse solution (e.g., bronze, silver, gold layers, data storage formats, etc).|
| `TS18`    | Experience designing and implementing efficient a data warehouse (e.g., data modeling for business needs).|
| `TS19`    | Proficiency on optimizing transactional data models to improve performance.|



### [SS-PEPS] Soft Skills - Planning, Execution, and Problem Solving

TBD

### [SS-IVBI] Soft Skills - Innovation, Value, and Business Impact

TBD


## Highly-Effective Team Composition

TBD
