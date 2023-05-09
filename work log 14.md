#  Work Report

## Time Period

* May 1st 2023 - May 7th 2023

## Worklog (8.5 hours)

* Summary

* Project Details:

    * Task 1: Figure out the way to use command line to query `codeql database` on linux and generate corresponding documentation (6 Hours):
        * Set up  `codeql` environment and install `Java` dependency on GCP VM following the steps previously mentioned
        * Read [`codeql query documation`](https://docs.github.com/en/code-security/codeql-cli/using-the-codeql-cli/using-custom-queries-with-the-codeql-cli), and run the `codeql run query` command, and get the `Error` report from the compiler
        * Debugged and rewrote the `enum-extract.ql` query file
            ```
            /**
            * @name Java Project Enum collection query
            * @kind problem
            * @problem.severity warning
            * @id java/example/empty-block
            */

            import java

            from EnumType e

            where 
            e.getFile().getAbsolutePath().matches("%src/main/java%")

            select 
            e.getName(),
            e.getAnEnumConstant(),
            e.getFile().getAbsolutePath(),
            e.getLocation()
            ```
        * Testified and verified the command line script with several Java projects.
        * Generate full documentation of `querying codeql database` using command line purely on linux.

    * Task 2: Generate documentation for `swagger` file generation on fly (2 Hours):
        * Taken `LakesideMutual` and `ftgo-application` as samples to generate the `swagger` files generation documentation.

    * Task 3: Regenerate `swagger` file for `day-trader` (30 Mins)