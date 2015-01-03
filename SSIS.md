## SQL Server Integration Services



Gitignore

https://github.com/github/gitignore/blob/master/VisualStudio.gitignore







### Technical details

#### Pipeline Architecture



### Practices
- Use expressions instead of package configurations to make packages portable (need to test)
- Other idea is to use DTExecUI to generate arguments to set values
- Check how to create SSIS components


#### Implementing Integrations for Analysis Services

Implement one SSIS package for each dimension or fact. Manage the execution using parent packages.


#### Terms
- Business or Natural key: in a Dimension table, the key in the source database


#### Misc
- Use data viewers to see the result of data flow transformations
- tool: smtp4dev, to test e-mail sending
- SSIS scripts can fire events: FireCustomEvent, FireError, FireInformation
- Debug runs only in 32 runtime
- Event handlers are another way to have a conditional execution in SSIS packages.
- Checkpoint files saves state, saving variable values
- Executing: DTExecUI: graphical, generates also the arguments
- DTExec (the one I use most)
- Inferred members: need to get more info
- (Unit and Integration Testing of SSIS Packages)[http://msdn.microsoft.com/en-us/magazine/dn342874.aspx]
- https://ssisunit.codeplex.com/


#### Data Warehousing and SSIS
Use data profiling task to understand how the source data is organized. In the Data Profile Viewer we can get information to better structure a OLAP model.

- How to sync removed row from fact tables?

#### ETL Design Patterns
- Master Extract: uses Staging database
	- SQL Audit begin
	- Extract to Staging
	- Count rows
	- SQL Audit ends

- Master Transform-Load: need to load Dimensions first, then Facts

Microsoft Data Warehouse toolkit
http://tinyurl.com/qf84vl7


Using Star Join and Few-Outer Row Optimizations to improve DW http://msdn.microsoft.com/en-us/library/gg567299.aspx



