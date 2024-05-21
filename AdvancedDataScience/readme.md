In some process models, Data Cleansing is a separate task, it is closely tied to Feature Creation but also draws findings from the Initial Data Exploration task. 

While tuning machine learning models, this deliverable asset is touched on a regular basis anyway because features need to be transformed to increase model performance. 

The following none exhaustive list gives you some guidelines:

·      Data types Are data types of columns matching their content? E.g. is age stored as integer and not as string?  

·      Ranges Does the value distribution of values in a column make sense? Use stats (e.g. min, max, mean, standard deviation) and visualizations (e.g. box-plot, histogram) for help  

·      Emptiness Are all values non-null where mandatory? E.g. client IDs  

·      Uniqueness Are duplicates present where undesired? E.g. client IDs  

·      Set memberships Are only allowed values chosen for categorical or ordinal fields? E.g. Female, Male, Unknown  

·      Foreign key set memberships Are only allowed values chosen as field? E.g. ZIP code  

·      Regular expressions Some files need to stick to a pattern expressed by a regular expression. E.g. a lower-case character followed by 6 digits  

·      Cross-field validation Some fields can impact validity of other fields. E.g. a male person can’t be pregnant   
