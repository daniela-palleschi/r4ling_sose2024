# r4ling_sose2024
Teaching materials for 'Angewandte Datenverarbeitung und Visualisierung: R für Linguistik und Sozialwissenschaften' (summer semester 2024)

## How to restore `renv` lockfile

To re-use these materials, you need to restore the lockfile which contains all package dependencies. To do so:

1. Download the .zip file of the project (or fork it, whatever you prefer)
2. Double-click on the RProject (`.Rproj`) in your file manager. RStudio should open.
3. The console should display some information about `renv`:

`- Project '~/yourfilepath/r4ling_sose2024-main' loaded. [renv 1.0.11]`
`- One or more packages recorded in the lockfile are not installed.`
`- Use renv::status() for more details.`

4. Follow these instructions: run `renv::status()` in the Console. You will likely get a list of files that need to be installed, type `Y` to install them.

5. If all is well, run `renv::status()`.
  - if you encountered problems, e.g., one package caused a problem, then try `renv::repair(exclude = "package")`, replacing `package` with the name of the problem package(s)
  - if `renv::status()` gives the message `The following package(s) are in an inconsistent state:` followed by a list of packages (and no other warnings about specific packages below), this means that you're ready to snapshot.

6. Run `renv::snapshot()`. You should get a message `The following package(s) will be updated in the lockfile:` with a list of packages. Type `Y` to proceed.

7. Again, run `renv::status()`. Hopefully you are told there are no problems. Otherwise, you can try simply installing the problematic packages individually and running `renv::snapshot()`, followed by `renv::status()`.



  