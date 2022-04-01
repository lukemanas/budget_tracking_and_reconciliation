# budget_tracking_and_reconciliation
 
 
Two beskoke solutions used to help run operations and implement a budget forecasting model accross two databases for a $12M portfolio (>1k requests to ~600 partners) split between 7 teams and ~20 individuals.

Leading to:
- Improve departmental KPIs for request lifecycle by 36% (47-30 days)
- Design budget forecasting model to keep variance < 1% MoM.
- Increase the # of requests processed in the 'goldilocks zone' by 40pp.
 
 ** Unfortunately, both pieces of code have been stripped of all identifing information for PII reasons. Eventually, I would like to provide random data for testing.**
 
The two notebooks in this repository consist of the following:

1. Legacy Database Reconciliation - Solution to reconcile two legacy databases without an accessable common key or api protocol. Two approaches were designed, one utilizing a manual key sheet to merge on and the later, skipping this step by using the fuzzy matches library. This is now defunct as a common key was eventually accessed to index on. The first was a tracking database and the second is a payments databse.

2.  Budget Tracking - Bespoke solution for reconciling projections accross different teams and reconciling them with actualls in the database. The projections sheets were condensed in power query before being imported here as one dataframe. Once payments are reconciled, the function then splits each team into its own tab and formats the excel sheet for consumption by non-technical teams.  
