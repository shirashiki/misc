## Business Intelligence Patterns and Practices


### Business Intelligence Practice


#### Concepts



* Drill Across *

When we retrieve measurements from different processes. It assumes each process is a fact, and we have common dimensions.


* Multipass SQL *


* Role-playing dimension *

Role-playing in a data warehouse occurs when a single dimension simultaneously
appears several times in the same fact table. The underlying dimension may exist as
a single physical table, but each of the roles should be presented to the data access
tools in a separately labeled view.


* Semiadditive Facts *

All measures that record a static level (inventory levels, financial account balances,
and measures of intensity such as room temperatures) are inherently nonadditive
across the date dimension and possibly other dimensions. In these cases, the measure
may be aggregated usefully across time, for example, by averaging over the
number of time periods.