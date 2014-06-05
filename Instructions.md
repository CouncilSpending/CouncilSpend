User Guide
===========

Getting Started
---------------

The first step is to initialize your local authority model. This involves
creating a directory (named after the argument given), with two subdirectories:

-   **csv** - a folder to keep the raw files, downloaded from the website
-   **rds** - a folder to keep cleaned data files, in a compressed `.rds` format.

It also saves basic information in an `.rda` file in the local authority
directory.

If a model already exists in the working directory, this model is returned.

```
source('CouncilSpend.R')
ntm <- CouncilSpend('nottingham')
```

Downloading Files
-----------------

*Downloading manually*  
Once the csv directory has been created, the files can be added to this file 
manually, provided that they are named as follows:
name of council + year (4 digits) + month (2 digits) + .csv

So for Nottingham's January 2013 file, it would be:  
`nottingham201301.csv`

It is sometimes easier to do it this way, so I would suggest right-clicking on 
each link and then 'Save link as' according to the above naming system.

*Downloading from a csv file/data frame*  
Alternatively, you can provide a data frame with the columns **year** 
(4 digit number) and an integer for the **month**, then a url in the **link**
column.

For Example:
