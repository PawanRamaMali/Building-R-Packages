# Building-R-Packages

Guide to building packages in R

## Why build a package, and not just use source() function?

* source() references a specific .R file, reads it all in and executes it (which can include adding a function to the environment).

### source()-ing: 

* Doesn't "know" anything about versioning of the code, ie can be tied to a specific package version
* Doesn't have included testing
* Doesn't have included documentation
* Requires the .R file to be copied into every project that needs it
* Needs to be changed in every project that needs it
* Can be modified or deleted (accidentally) by the end-user


## Anatomy of a package

* **Metadata** via the DESCRIPTION, including the name of the package, description of the package, the version of the package, and any package dependencies

* **Source code** via .R files, that live in the R/ directory.

* Special roxygen comments inside the .R files that describe how the function operates and its arguments, dependencies, and other metadata

* The **namespace** for the exported functions you have written, and the imported functions you bring in

* Tests that confirm your function "works as intended"

* Other things (installed files, compiled code, data, tutorials, vignettes)


### Writing packages, but easier

While creating a package can seem intimidating, the tidyverse team has spent years crafting meta-packages to make life easier to create packages. These are used everyday by 1000s of package developers, and really do make the complicated things easier... with functions!

* devtools:
The aim of devtools is to make package development easier by providing R functions that simplify and expedite common tasks.

* usethis:
usethis is a workflow package: it automates repetitive tasks that arise during project setup and development, both for R packages and non-package projects.


