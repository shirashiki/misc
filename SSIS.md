## SQL Server Integration Services


### Technical details

#### Pipeline Architecture



### Practices
- Use expressions instead of package configurations to make packages portable (need to test)
- Other idea is to use DTExecUI to generate arguments to set values
- Check how to create SSIS components


#### Implementing Integrations for Analysis Services

Implement one SSIS package for each dimension or fact. Manage the execution using parent packages.




#### Misc
- Use data viewers to see the result of data flow transformations
- tool: smtp4dev, to test e-mail sending
- SSIS scripts can fire events: FireCustomEvent, FireError, FireInformation
- Debug runs only in 32 runtime
- Event handlers are another way to have a conditional execution in SSIS packages.
- Checkpoint files saves state, saving variable values
- Executing: DTExecUI: graphical, generates also the arguments
- DTExec (the one I use most)


