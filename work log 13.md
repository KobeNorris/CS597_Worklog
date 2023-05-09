#  Work Report

## Time Period

* Apr 24th 2023 - Apr 30th 2023

## Worklog (11 hours)

* Summary

* Project Details:

    * Task 1: Generate `enum` reports from all projects on `REST_Go` (7 Hours):
        * Install `codeql` and generate the `codeql database` for all of the existing 20 projects within `REST_Go`
        * Install `codeql agent` and `codeql starter` codebase to run `codeql query` under `vs code codeql workspace` environment.
        * Found that the `codeql` mircservice code plugin **only works on Mac**, the compiler will report `Java` dependency missing while running on linux and windows platform
        * By reading the [documentation](https://docs.github.com/en/code-security/codeql-cli/using-the-codeql-cli/getting-started-with-the-codeql-cli), try to manually set up dependency environment by developing a configuration file named `qlpack.yml`, the file content will be
            ```
            name: rest-go/codeql-extra-queries-java
            version: 0.0.0
            dependencies:
                codeql/java-all: "*"
            ```
        * Run the `codeql packing` command using commmand line `codeql pack`, and then run the query using the query command in `vs code codeql agent` plugin under the `codeql workspace` (The entire debugging process cost for about 4 hours)
        * Generate the `Enum` reports using the query functionality of the `vs code codeql agent` workspace.

    * Offline Meeting with Professors (2 Hours):

        * Description: Review last week progress this week task.
            * Give a demo of the `codeql` query process to Professor Darko
            * Professor Darko helped developed the bash scripts to obtain `Enum` report and compared the result
            * Set up task to verify the report, and regenerate reports if necessary.

    * Task 2: Regenerate the `Enum` reports (2 Hours):
        * Regenerate the `Enum` reports using Professor Darko's scripts and `codeql query` under the `cs` folder