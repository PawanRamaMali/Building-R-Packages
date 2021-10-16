# Building-R-Packages

Guide to building packages in R

## Why build a package, and not just use source() function?

* source() references a specific .R file, reads it all in and executes it (which can include adding a function to the environment).

* source()-ing: 

* Doesn't "know" anything about versioning of the code, ie can be tied to a specific package version
* Doesn't have included testing
* Doesn't have included documentation
* Requires the .R file to be copied into every project that needs it
* Needs to be changed in every project that needs it
* Can be modified or deleted (accidentally) by the end-user
