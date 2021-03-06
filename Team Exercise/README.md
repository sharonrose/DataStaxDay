# Team Exercise

For this exercise you should work as teams of 3-5 people.

## Background

Bestmart is a global retailer that was founded in St. Louis in 1900.  Since then, they've grown to over 8000 locations globally through organic growth as well as acquisition of brands in Western Europe and Southeast Asia.  Bestmart revenue is currently over $30B.

Bestmart is looking to refresh the database infrastructure in their Ashburn, VA datacenter which is hosted by AT&T.  They've heard about DataStax and believe they can improve on the availability of their current infrastructure while reducing the TCO.

The Ashburn datacenter has a 10 node Oracle Exadata X5-2 system.  A DR site in Reston hosts 15 Dell PowerEdge servers that are nearly five years old and running Oracle 10g.  Oracle GoldenGate and Oracle Data Guard are used to copy data to the DR site.  The SLA for data copy is 30 minutes.  In the event DR is invoked, the DR site must be live within 8 hours to meet its SLA.

In addition to hosting the database, Ashburn hosts bestmart.com, the web portal for Bestmart.  Bestmart.com is responsible for 30% of Bestmart's revenue, with 80% of that occurring during the holiday season.  The webportal also powers the Bestmart loyalty app, Best4U.  The application has dismal ratings on the Apple app store, mostly due to its long response times and frequent downtime.

Bestmart also has a 50TB Terradata instance for its datawarehouse.  BusinessObjects is used on top of that to provide monthly rollup reports that are presented to the board.

Another area of interest is the infrastructure behind their point of sale (POS) systems.  Stores are divided into three classes, A, B and C.  A stores are the largest, making up 2000 stores out of the 8000 total.  Each A store has 30 or more POS systems, all connected to an in-store Oracle 11g instance.  That 11g instance uses an nightly Informatica ETL job to copy its transactions to Ashburn.  ETL jobs also refresh the inventory data from the store.  Another ETL job downloads pricing and promotional data from the central DC to the store.

With the US refresh complete, Bestmart would like to replace similar infrastructure worldwide and consolidate its IT systems.

## Discovery

### Use Case Definition

What areas can DataStax and Azure assist with Bestmart's infrastructure refresh?

What systems outside the database could DataStax Enterprise improve.  Think of features we disussed in the labs, including:
* Solr
* Spark
* Graph

Bonus - What feature of DSE could improve the POS situation?

### Sizing

What questions would you ask Bestmart to help size a DataStax on Azure system to refresh their existing infrastructure?

Hint -- here are some numbers you'll need to estimate:
* Transactions per second
* Data volumes

You will want to come up with a proposed architecture, both for the initial system as well as potential expansion.  This would include information on machines, storage, network and datacenters.

It may be useful to consult the [Azure Deployment Guide](https://github.com/DSPN/azure-deployment-guide/blob/master/bestpractices.md).

### ROI

Bestmart is comtemplating a significant investment to refresh its infrastructure.  What questions do we need to answer to help them get a handle on:
* Business as Usual
    * Maintenance cost
    * Opportunity cost
* DataStax and Azure
    * Maintenance cost
    * Migration cost
    * Benefit

For this exercise, build out an ROI and check if the proposed infrastructure will benefit Bestmart.

## Presenting

Prepare a few slides or a whiteboard to present your results to the class.
